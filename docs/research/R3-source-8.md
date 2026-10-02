# Source: https://80.lv/articles/suppressing-noise-without-sacrificing-lighting-quality-when-using-unreal-engine-s-lumen
# Original target: https://80.lv/articles/breakdown-of-environment-concept-art-workflow/ (closest available environment art article)
# Method: 8 (Domain homepage scan - found this environment art article on 80.lv)
# Retrieved: 2026-10-02
---
Suppressing Noise Without Sacrificing Lighting Quality With Lumen

80 Level - Articles and tutorials for 2D/3D Artists

## Suppressing Noise Without Sacrificing Lighting Quality When Using Unreal Engine's Lumen

#Environment Art #Interviews #Unreal Engine #Lighting

Author: Aleksander Goryachev, Level Designer
Interviewed by: Emma Collins
Date: 01 October 2026

Aleksander Goryachev talks us through his Unreal Engine lighting setup to show how to reduce unnecessary noise in complex scenes with numerous lighting sources.

## Introduction

I dedicated the past year to the development of my first major solo project, Post-Soviet Hospital. This is a realistic environment that conveys the atmosphere of an Eastern European hospital of the early 2010s. The first floor is designed as a massive complex of five thematic quarters. At the moment, four have been implemented: Laboratory, Laundry, Cabinets, and Hallway. Development of the Kitchen will begin soon to fully complete the level.

The project is being created as a game asset pack for the Fab digital marketplace. The target audience expects to get a clean picture 'out of the box.' The integration of third-party content (for example, Megascans) or plugins is excluded. Implementing this volume of content required self-completion of the entire development pipeline. I set a critical task for myself – saving working hours to ensure profitability.

Here you can read my breakdown of the project I did for 80 Level earlier this year.

One of the main technical challenges was solving problems with Lumen artifacts and noise. You cannot solve the noise problem with excessively high rendering quality settings or deep intervention in the engine itself. In this article, we will look into practical ways to combat rendering artifacts using standard Unreal Engine 5 tools.

## Lumen Noise Suppression Pipeline

## Light Structure and Fake Windows of a Closed Level

For the main level of the Post-Soviet Hospital project, a fundamental decision was made: I went for a complete rejection of Directional Light and Sky Light. In a closed interior, standard outdoor light forces you to build blind outer boxes of technical cubes (Lumen blockers) around rooms to avoid light leaks at the joints of modules. Disabling global sources solves this problem systematically and reduces the overall rendering load.

Natural light from windows is simulated by a local group of sources:

- Self-illuminating plane: a plane with an emissive material in the window opening that simulates the sky. The Affect Indirect Lighting parameter is disabled on it so that the glowing material does not generate uncontrollable Lumen noise.
- Rect Light: a rectangular light source in front of the glass inside the room. It is responsible for soft fill lighting (ambient bounce) deep into the room.
- Spot Light: a directional light source located in the scene as a separate object. A mask material (Light Function) is assigned to it to project sharp shadows from the window frame onto the floor of the offices.

It is worth noting that area sources (Rect Light) place a high load on the GPU. In-game scenarios, they should be used with extreme caution and, if possible, only without shadows. With a tight performance budget or when working in Software Ray Tracing mode, they are replaced with a Spot Light with a wide cone and a light mask (Light Function) of the window frame. Visually, the soft, physically correct scattering of light across the area (area light bounce) is lost – fill lighting becomes harder, flatter, and more directional.

## Emissive Materials Noise

When using self-illuminating materials (emissive materials), the key factors in noise generation are their brightness and surface area. This applies to any type of object: window planes, lampshades, instrument screens, etc.

If the Affect Indirect Lighting parameter is enabled on a Static Mesh, Lumen calculates its geometry as a physical light source for Lumen global illumination (Surface Cache). A detailed calculation of soft indirect light from complex glowing objects requires a massive number of rays. With a lack of computing power in the scene, chaotic, boiling noise occurs in global illumination.

In most cases, it is better to disable Affect Indirect Lighting in the Static Mesh settings. This completely excludes the object's geometry from the global calculation of Lumen GI. In the example below, I opted out of adding the true glow of the X-Ray screens in favor of a Rect Light.

But even with this parameter disabled, bright objects continue to generate strong local noise where they meet other surfaces. Glowing mesh is still rendered on the screen, and its bright pixels end up in the frame buffer (Scene Color), from which they are read by the Screen Space Traces algorithm.

## Screen Space Traces Noise

As seen in the example with the emissive materials, the complete elimination of noise in the interior is achieved by disabling the Screen Space Traces function in the Post Process Volume settings. This same algorithm becomes a source of noise when using rectangular light sources (Rect Light).

Stochastic sampling: area sources (Rect Light) and emissive materials are calculated by stochastic jittering. Due to frame-by-frame changes in tracing directions, flickering occurs, which the denoiser turns into slowly floating spots under the TV and near the glass blocks.

Subpixel jitter (TAA/TSR Jitter): temporal anti-aliasing shifts the camera projection by fractions of a pixel each frame. This causes microscopic changes in the coordinates of bright pixels in the frame buffer at geometry joints, causing corners and gaps to boil even with a stationary camera.

Scene Color dynamics: if a self-illuminating object is animated (for example, video on a TV screen), its brightness in Scene Color constantly changes. The algorithm instantly recalculates reflections for new frame buffer values, creating chaotic noise on the floor and walls.

Hidden geometry (Occlusion in dynamics): when moving the camera, glowing objects are occluded by other meshes or go off-screen. The algorithm instantly loses source information from the Scene Color buffer, causing sharp flashes and dips in brightness that the denoiser does not have time to compensate for.

As a result, I decided to abandon Screen Space Traces, disabling it in the Post Process Volume settings of the current level. At the same time, a minor loss of contrast in shadowed areas is easily compensated for by the Post Process Volume settings.

On the alternative, modular level with outdoor Directional Light illumination, disabling Screen Traces is critical: the scene loses a large amount of indirect light, and shadowed walls become flat. A comparison of these two pipelines is provided in a separate section.

If you need to preserve indirect light from the screen space with a lower noise level, change the tracing method. In the Project Settings → Rendering → Lumen menu, switch the Screen Tracing Source parameter from Scene Color to Antialiased Scene Color. This will reduce the noise level, but it will not completely solve the noise problem.

## Fake Indirect Light Sources (Light Fakes)

Attempting to rely entirely on Lumen for indirect light propagation often leads to an unsatisfactory visual result. The higher the value of the Indirect Lighting Intensity parameter of light sources, the stronger the noisiness of the scene and the more noticeable the loss of contrast between light and shadow. This problem becomes critical when attempting to illuminate deep nested rooms (room-within-a-room layouts).

Increasing the indirect lighting multiplier proportionally increases the mathematical error (variance) in Lumen's stochastic sampling. The denoiser cannot cope with the increased difference between bright and dark samples, causing pixel boiling. In addition, excessive indirect light floods deep corners and geometry joints, depriving the scene of natural contact shadows.

To create a clean and artistic look without Lumen noise, I used manual placement of fake local light sources:

Light passage through glass blocks: when transferring light from a bright outer room with windows to a dark inner one through a glass block wall, Lumen cannot correctly calculate transmission in real time. Close to the wall on the side of the dark room, an additional Rect Light source with disabled shadows (Cast Shadows) is installed for performance optimization. It simulates a soft stream of light that has supposedly passed through the glass blocks, providing stable fill lighting without maxing out indirect lighting on the main sources in the outer room.

Background illumination of deep corridors: illuminating long, shadowed corridors via natural re-reflection of light from open doorways generates strong high-frequency noise. In the depths of the dark corridor, a dim auxiliary Point Light source with a high Source Radius is installed. Settings are optimized for maximum rendering efficiency: the Cast Shadows function is completely disabled, the Indirect Lighting Intensity parameter is set to 0, and the Affect Indirect Lighting parameter is fully turned off. This creates cheap direct lighting that mimics deep light bounces from adjacent rooms.

Setting up ceiling fixtures and artificial lighting: ceiling fixtures with self-illuminating materials (emissive materials) require fine-tuning so that the glowing plastic of the lampshade does not generate noise on the ceiling. Depending on the performance budget, one of three approaches can be applied:

1. Combined method (main): the Affect Indirect Lighting parameter on the lampshade remains enabled. Local noise from the emissive material is completely masked by a bright physical Point Light source installed immediately below the lampshade. Direct light from the Point Light simply burns out and masks the Lumen noise, making it invisible to the player.

2. Non-emissive method: the Affect Indirect Lighting parameter is completely disabled in the Static Mesh settings of the lampshade. The role of environmental illumination is 100% transferred to the Point Light below it. This method guarantees a complete absence of Lumen GI noise around the fixture.

3. Budget method (for performance savings): if the scene is overloaded with point sources, a cheap Spot Light with a wide cone directed downwards is placed under the fixture as the main fill light. At the same time, a Point Light with a minimal attenuation radius is retained directly inside the lampshade. It does not illuminate the scene, but performs a single task: it highlights the lampshade itself and suppresses noise at the contact point of the fixture with the ceiling.

Local illumination of dark areas and frames: narrow openings (like door glazing) and internal frames of objects (like the plastic bezel of a TV) go into deep shadow when using a Rect Light or generate strong noise at geometry joints. Installing a weak compensating Point Light close to the frame or screen illuminates the elements of the TV's own housing or the wall around the door opening. This simulates soft scattering of light and masks local noise without the need to calculate complex reflections in narrow gaps.

## Configuration via Console Variables

Attempts to remove noise by simply increasing the number of samples and rays (final gather, ray directions) critically reduce performance and are inapplicable in real projects. It is more effective to configure temporal accumulation, forcing the algorithm to take data from previous frames instead of brute-force calculation in the current one. A detailed breakdown of stability is described in the Epic Games guide.

The main tool for suppressing residual noise that could not be eliminated by local placement of light sources is changing the frame accumulation limit:

r.Lumen.ScreenProbeGather.Temporal.MaxFramesAccumulated 16 (default value: 10)

Practical parameter selection: the variable specifies to the Screen Probe Gather algorithm the maximum number of previous history frames, data from which can be used to filter noise in the current frame. Based on practical tests, the ideal balance of temporal anti-aliasing and image stability for a closed hospital level with paced gameplay is achieved precisely at a value of 16.

Further increasing the parameter does not bring a noticeable improvement in the image and does not yield the desired result in suppressing residual noise, but it can lead to excessive video memory (VRAM) consumption. The setting is applied by the developer with an understanding of the trade-offs – the risk of ghosting in dynamics.

## Comparison of Two Pipelines in One Project

Within the framework of developing the Post-Soviet Hospital project, two fundamentally different approaches to geometry modeling and lighting calculation were implemented. The first approach is used on the main closed level of the hospital. It is based on the concept of single seamless rooms (one office is a single mesh) and manual placement of local light fakes. The Screen Space Traces function is completely disabled here.

The second approach is implemented in the demonstration level of the modular constructor (Modular Kit). This kit was developed in response to numerous requests from Fab users who do not specialize in level art but need a quick assembly of their own unique layouts.

To ensure smooth out-of-the-box assembly, the following architectural decisions were made:

- Precise snapping and geometry thickness: all modular wall blocks are created with high physical thickness. This is done specifically for Lumen to prevent light leaks at block joints and ensure correct Lumen mesh card generation.
- Default environment: the modular level scene is designed to work in the standard Epic Games template with a base set of global illumination (Directional Light, Sky Light, skybox) without altering any internal parameters.
- Ease of setup: the user does not need to use console variables or construct complex chains of light fakes. It is enough to assemble a room, install a Point Light under the ceiling fixture, and get a ready out-of-the-box result.
- Penalty for simplicity: the cost of using the default pipeline without fine manual tuning is an increased level of Lumen noise in deep areas of indirect illumination.

A comparison of the technical parameters of the two pipelines is given in the table.

## Conclusion

The Lumen noise suppression pipeline is built on understanding the hardware limitations of the engine. Instead of a straightforward increase in rendering settings, which inevitably reduces the frame rate, a clean result is achieved through three components: the correct topology of room geometry, fine-tuning of the temporal filter, and manual placement of fake light sources. This hybrid approach makes it possible to get a predictable, artistic, and high-quality render out of the box, even in complex closed interiors.

You can get the assets from the scene on Fab if you want to experiment with it yourself.

## Aleksandr Goryachev, Environment & Level Designer
Interview conducted by Emma Collins

---

80 Level - Built for the Game & Digital Art Industry

© 2026. 80 level. All rights reserved.
- About & Contact us
- Privacy Policy
- Republishing policy
- Terms of use
- Disclaimer
