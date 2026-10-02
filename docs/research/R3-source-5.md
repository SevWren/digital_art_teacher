# Source: https://80.lv/articles/setting-up-game-level-inspired-by-alien-dead-space
# Original target: https://80.lv/articles/breakdown-of-environment-concept-art-workflow/
# Method: 8 (Domain homepage scan - found this environment concept art article on 80.lv)
# Retrieved: 2026-10-02
---
How to Set Up Game Level Inspired by Alien & Dead Space

80 Level - Articles and tutorials for 2D/3D Artists

## Setting Up Game Level Inspired by Alien & Dead Space

#Environment Art #Feature #3ds Max #Unreal Engine

Author: Volodymyr Donchenko, Environment Concept Director
Interviewed by: 80 Level
Date: 18 December 2024

Volodymyr Donchenko talked about his ALIEN MOON project, a sci-fi game level inspired by Alien and Dead Space, explaining how he achieved a cohesive look and handled technical optimization in Unreal Engine.

## Introduction

My name is Volodymyr Donchenko, and I'm the Environment Concept Director at YHKT Entertainment. I've spent many years in the game industry, working with companies like S-Game, NetEase Games, and more.

My latest project, "ALIEN MOON," explores the concept of an interactive art experience where users don't just view images or watch videos but can actively explore and walk within the environment. Inspired by iconic sci-fi films and games, this project allows players to recognize familiar references while experiencing something new.

## ALIEN MOON

"ALIEN MOON" draws inspiration from the "Alien" film series, the "Dead Space" games, and other sci-fi media, creating an atmosphere of loneliness aboard an abandoned space station. This piece is a snapshot within a larger narrative, inviting players to uncover fragments of a mysterious backstory.

At the earliest stages, after assembling the initial mood board, I began collaborating with music producer Terence Junhong She. Sound design is a critical element in game and interactive art, and Terence's music plays a vital role in "ALIEN MOON," shaping the emotional landscape.

With each new Unreal Engine (UE) build scene improvement, Terence refined the soundtrack to perfectly complement the visuals and gameplay, reinforcing the immersive atmosphere. Terence believes the importance of an immersive experience of video games is made by quality music. You can ask any gamers: when they finish a good game and say what's on their minds, usually, the first thing they will say is the feelings they have, their emotions, moods, and, "Wow, that was intense!"

After consolidating references, the next step was to gather assets for level design. For this project, I used a combination of custom 3ds Max models, Megascans, and various high-quality assets sourced from the Unreal Engine Marketplace. Special thanks to asset creators Sergey Tyapkin for the "NOVA – Modular Sci-Fi Kit", Rag-STUDIO (Tarock) for the "Industrial Megapack V.2", BMS Assets for "Astronova", and Vasiliy Poryagin for Sci-fi props.

To ensure stylistic consistency, I spent considerable time adjusting materials, geometry, colors, and other details within UE. The engine offers powerful tools for in-editor modifications, but for more complex adjustments, I used external software like 3ds Max and Photoshop.

The white box stage wasn't necessary for every part of this project; for small interiors, I worked from a simple 2D top-down sketch. In the picture, you can see the final result for the top view.

However, I kept the composition in mind to ensure a cohesive look both for static shots and during gameplay, which can be challenging in some areas. A small testing room with core settings also served as a useful template for scene assembly.

Each environment was constructed layer-by-layer, much like a real interior, starting from the foundation – floors and walls – to the finer details like lighting, fog, and atmospheric effects. For landscape elements viewed from windows, I used static meshes, creating small compositions that enhance the background without overburdening the system.

Some window views lead to fully developed areas that, while accessible in theory, remain off-limits in this version to control player movement.

Particles, smoke, cloth simulation – interactive moving objects always bring extra life to the scene.

For light animation, I used material function materials (flickering), fun rotating was achieved by a simple blueprint function – "rotating movement." Decals, extra imported (3ds Max) small props objects help complete some mini areas.

## Technical Optimization & Interaction

A significant technical challenge was optimizing the project to maintain 60 FPS with the highest visual quality possible on my hardware. This included optimizing textures, adjusting volumetric lighting, controlling shadow settings, and limiting static meshes. I leveraged UE 5.4.4 features like Nanite, Virtual Texturing, and Lumen for enhanced performance.

Performance constraints influenced the scale of the level, especially with heavy simulations like cloth and Niagara particles, which I used sparingly. These effects add life to the scene, but they come with a performance cost – hopefully, future UE versions will allow for greater flexibility.

## Polishing the Project

I focused heavily on UE's lighting tools and post-process effects to achieve the desired mood. Color schemes, depth of field, and various other settings allowed me to create the right atmosphere.

Since the environment is set on a planet's surface, balancing interior fog with a dark, starry sky outside was crucial. The "Ultra Dynamic Sky" plugin helped set the appropriate mood for both interior and exterior spaces.

Interior lighting was further enhanced with volumetric light settings, adding local fog effects around light sources. As the project neared completion, I paused to review, making notes and simple overpaints to identify potential improvements.

This approach often sparked new ideas and led to the addition of new areas or modifications to existing ones.

As the final stages approached, I created a series of short video clips highlighting key scenes, many of which make for ideal backdrops in ambient music videos.

## Conclusion

As concept art continues evolving toward immersive, interactive experiences, tools like Unreal Engine are transforming the workflow. Compared to traditional 3ds Max and Photoshop renders, UE enables faster, more dynamic creation processes.

However, balancing development time with a healthy lifestyle is essential – especially when working on personal projects alongside a primary job. I make it a point to travel, exercise, visit museums, and explore new experiences, all of which bring fresh inspiration to my work.

In summary, projects like "ALIEN MOON" are valuable for honing level design, technical, and artistic skills. With additional time, this could easily become part of a larger, fully-fledged game.

Thank you for following along with this journey.

## Volodymyr Donchenko, Environment Concept Director

---

80 Level - Built for the Game & Digital Art Industry

© 2026. 80 level. All rights reserved.
- About & Contact us
- Privacy Policy
- Republishing policy
- Terms of use
- Disclaimer
