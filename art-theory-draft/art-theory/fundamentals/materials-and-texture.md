# Materials and Texture

**Status:** Work in progress.

Every surface you paint — cloth, skin, metal, stone, wood — is governed by the same underlying value and lighting system. What changes between materials is not the light rules, but how each surface responds to those rules: how spread-out or concentrated the bright spot is, how sharp or soft its edges are, and what visual marks suggest the surface character underneath. Understanding these variables lets you paint convincing materials without memorising a separate method for each one.

---

## Core Components

### Diffuse reflection
When light hits a rough surface (raw wood, matte paint, fabric, unpolished stone), it bounces away in all directions at once. No single direction gets an especially bright return. The result is a broad, even distribution of light across the surface: the bright area is wide, gradual, and has soft edges. This is called diffuse reflection. Nearly all the light you see on a matte surface is diffuse.

### Specular reflection
When light hits a smooth surface (polished metal, glass, wet skin, lacquered wood), it bounces back in a concentrated beam — mostly toward the eye when the surface angle is just right. The result is a small, intense bright spot with hard edges. This is called specular reflection. The smoother the surface, the smaller, brighter, and sharper that spot becomes. At the extreme — a mirror — the "spot" becomes a perfect reflection of the light source itself.

### Roughness as the primary variable
Roughness is the single knob that controls everything about how a surface reads. Moving from rough to smooth:

- The highlight (the brightest point on the surface) shrinks and sharpens.
- The transition between the bright spot and the surrounding surface becomes harder-edged.
- The surface begins to reflect the environment around it, not just the light source.

| Surface type | Highlight size | Highlight edge | Typical examples |
| :--- | :--- | :--- | :--- |
| Very rough / matte | Very large, almost no distinct spot | Very soft, blends into surrounding value | Rough stone, chalk, raw fabric |
| Semi-matte | Moderate, visible | Soft to medium | Skin, painted wall, unfinished wood |
| Semi-gloss | Smaller, distinct | Medium to firm | Polished leather, glazed ceramic |
| Glossy / shiny | Small, bright, intense | Sharp | Lacquered furniture, wet surface |
| Mirror / metallic | Near-point, extremely bright | Very hard | Polished chrome, glass |

### The value and lighting system applies to all materials
The same rules from the light-and-value system — light family, shadow family, core shadow, reflected light, cast shadow — apply to every material without exception. A polished metal sphere and a matte clay sphere share the same form and the same light direction. What differs is only the highlight shape and edge sharpness. Never abandon the underlying value structure when painting a shiny or textured surface.

### Texture follows form
Texture is not a flat pattern applied over a surface — it is information about a surface that must curve and bend with the form underneath. On a flat surface, parallel wood-grain lines run parallel. On a curved surface — a barrel, an arm, a rounded stone — those same lines spread, compress, and arc with the curve. Texture that does not follow form looks like a sticker applied to the outside of a shape rather than a quality of the shape itself.

### Visual texture via mark-making
In digital painting, physical surface texture (the actual bumpiness of a material) is usually conveyed through directional marks, not through a scanned texture stamp. The direction, length, opacity variation, and spacing of your brushstrokes collectively suggest what the surface is made of. Strokes that follow the form's contours describe a soft, rounded surface. Short, irregular marks describe roughness. Long, smooth, parallel strokes describe something flat and consistent. Varying the marks — changing direction at plane breaks, shortening them where the surface turns away — carries more information than stamped texture.

### Micro-structure vs. macro-form
Texture is micro-structure. The value structure (light side, shadow side, core shadow, reflected light) is macro-form. These operate at different scales and must not interfere with each other:

- Macro-form (the value structure) tells the viewer that a shape is a sphere, a cylinder, or a box.
- Micro-structure (texture marks) tells the viewer what the surface of that shape is made of.

Texture marks must be lighter on the light side of the form and darker on the shadow side, following the same value logic as the macro-form. Texture that ignores value and runs at uniform opacity across both the light and shadow side flattens the form.

---

## Practical Decision Criteria

1. **Decide the roughness level before you start rendering.** Is this surface matte, semi-gloss, or highly polished? That decision tells you how large and how sharp your highlights will be, and whether the surface will pick up any reflection from the environment.

2. **Build the macro-form (value structure) first.** Establish the full light-side-to-shadow-side value range as you would for any other surface. Do not begin adding texture marks until the form already reads convincingly in your value pass.

3. **Place the highlight according to roughness.** For matte surfaces, broaden the highlight area into a wide, soft transition toward the top of the light side — there is no distinct "dot." For glossy surfaces, shrink the highlight to a small, hard-edged point and place it precisely where the surface geometry would bounce the light source directly toward the viewer.

4. **Add texture marks following the form, not against it.** Orient strokes to follow the surface contour. At a plane break (where the surface changes direction), change the stroke direction to match. On a curved surface, let strokes arc with the curve.

5. **Vary mark opacity and length with the value zone.** In the light area, marks can be brighter or lower-opacity against the lighter ground. In the shadow area, they should be darker. Marks at full uniform opacity across the whole form will kill the form reading.

6. **Check the result in greyscale.** Temporarily desaturate and check that the form still reads clearly. If texture marks have disrupted the value structure, the form will look flat or confused at this stage. Correct the macro-form before continuing.

---

## Common Failure Modes

| What you notice | Likely cause | What to try |
| :--- | :--- | :--- |
| Texture looks like a decal or sticker on the surface | Marks are not following the form's contour; they run flat regardless of the form's curvature | Re-draw marks so they arc with the curve; change direction at plane breaks |
| Shiny object does not look shiny | Highlight is too large, too soft, or too low-contrast | Shrink the highlight area, harden its edge, and increase its brightness relative to the surrounding surface |
| Matte surface accidentally looks shiny | Highlight area is too small and too sharp | Broaden the bright region into a wide, gradual transition; soften the edge until it blends smoothly into the surrounding value |
| Texture detail flattens the form | Marks run at uniform brightness across both light and shadow sides | Reduce mark brightness/opacity on the shadow side so marks follow the macro-value structure |
| Surface has no surface character at all | Marks too uniform in length, direction, and spacing | Introduce controlled variation: vary mark length, occasional direction changes, slight opacity differences — match the variation to what the real material looks and behaves like |
| Two different materials look identical | Highlight size and edge quality are the same for both | Identify which is rougher; give it a larger, softer highlight; give the smoother one a smaller, sharper highlight |

---

## Relationship to Pipeline

_Pipeline step relationships pending #36 validation. This section will be updated once the confirmed pipeline structure exists._
---

## Plain-English Guide

> **Who this is for:** Someone opening a digital painting app for the first time with no formal art training.

### What are materials and texture?

When you paint something, you are not just painting a shape — you are painting what it is made of. A wooden table, a metal spoon, and a cloth napkin sitting in the same patch of sunlight all have the same light direction, but they look completely different because each surface handles light differently. The spoon bounces the light back at you in a tight, bright glint. The cloth spreads the light in a wide, soft glow with no distinct bright dot. The wood sits somewhere in between. Learning to control this difference is what makes painted objects look like they are actually made of something, rather than like flat shapes painted with colours.

Texture is closely related: it is the visual information that tells you how a surface feels — rough stone, smooth glass, soft fabric — conveyed through the direction and character of the marks you make.

### The key ideas, without the jargon

**How rough the surface is (roughness — that means how bumpy or smooth the material is at the microscopic level):** Think of spreading peanut butter on toast. If you spread it evenly and smoothly, light hitting the surface spreads out in all directions and there is no bright spot you can point to — that is a matte surface. Now think of a spoon: its surface is so smooth that when light hits it, almost all of it bounces back in one concentrated beam. That beam is what creates the tiny, intense glint you see on the spoon. Roughness controls whether your painted surface looks like the peanut butter (spread, dull, no spot) or the spoon (tight, bright glint).

**The size and sharpness of the bright spot (highlight — that means the brightest point on a surface):** Hold a white ceramic mug in front of a window. On the mug you see a bright patch somewhere on its curved side — wide, soft-edged, fading gently into the surrounding colour. Now look at a metal teaspoon instead. The bright spot on the spoon is tiny, intensely bright, and has a hard, sharp edge. Same window light. Same angle. Different material. The mug scatters the light; the spoon concentrates it. Making this one change — size and sharpness of the bright spot — is the most direct way to switch a surface from matte to shiny in a painting.

**The same brightness rules apply to every material (value structure — that means the map of light and dark areas on a form):** A rough stone ball and a chrome ball follow exactly the same rules: the side facing the light is brighter, the side facing away is darker, there is a darkest band in between where neither the direct light nor the light bouncing off the floor reaches. What changes is only the size and edge quality of the bright spot at the top. Never throw away your dark-and-light structure when you start adding material detail.

**Texture bending with the shape (texture follows form — that means the surface pattern bends wherever the underlying shape bends):** Think of wearing a striped shirt. When your arm hangs straight down at your side, the stripes run parallel. When you bend your elbow, the stripes on the inside of the elbow bunch together and the stripes on the outside spread apart. The stripes follow the shape of your arm — they do not stay flat and parallel across the bend. Paint texture the same way: marks that describe the surface of a curved object should curve with the object, not run straight across it as if the object were flat.

**Surface character through mark direction (visual texture — that means the look and feel of a surface created by the way you make marks, not by stamping a pattern onto it):** A rough stone wall is not rough because you applied a photo of a stone wall on top of your painting. It is rough because many short, irregular, slightly varied marks in slightly varied directions together convince the eye that the surface is irregular. Smooth glass looks smooth because the marks describing it are long, even, and consistent. The character of your brushstroke is how the viewer reads the surface. Rough surface: varied, irregular marks. Smooth surface: long, consistent, even marks.

**Surface detail sitting on top of the light structure, not replacing it (micro-structure vs. macro-form — that means texture detail is a second layer of information that rides on top of the bigger light-and-dark structure):** Think of the difference between the overall shape of a mountain range seen from far away, and the rough individual rocks that make up one cliff face when you stand close to it. The mountain range has its own big areas of light and shadow — that is the macro-form. The individual rocks add bumpy detail on top — that is the micro-structure. Your painted surface works the same way. The big light-side/shadow-side structure is the mountain range. The texture marks are the individual rocks. The texture marks must be lighter in the lit areas and darker in the shadow areas of the big structure — they must ride on top of it, not ignore it.

### What to actually do in your software

1. **Decide how shiny the surface is before you paint anything.** Ask yourself: is this more like a piece of chalk (no bright spot at all, just a broad glow), more like a ceramic mug (moderate bright patch, soft edge), or more like a metal spoon (tiny, intense, hard-edged glint)? Write that decision down next to your canvas so you do not forget halfway through.

2. **Build the full light-to-dark structure first, ignoring all surface detail.** Paint the lit side lighter, the shadow side darker, and the darkest band (the stripe that gets neither direct light nor reflected bounce light) darkest of all. Make this look convincing on its own before adding any texture. If the shape already reads as round or flat in this stage, you are ready to continue.

3. **Place and size the bright spot based on your roughness decision.** For a matte surface, take a large, very soft brush, pick a colour slightly lighter than your lit-side colour, and gently brush the top of the lit area — creating a wide, barely-visible brightening with no distinct edge. For a shiny surface, take a small, hard brush, pick near-white, and place a small, tight dot exactly where the surface geometry faces the light source directly. For something in between, use a medium-sized brush with a moderate edge softness.

4. **Add texture marks following the shape.** On a new layer at low opacity, use a medium brush to add short marks that follow the curve of the surface — if the surface curves away from you at the right side, your marks should arc that direction too. In the lit areas, make the marks slightly lighter or just slightly visible. In the shadow areas, make them slightly darker or nearly invisible. The marks should enhance the surface without flattening the big light-and-dark structure you already built.

### Common traps to avoid

- **Making everything equally shiny.** If your cloth, your wood, and your metal all have the same small, sharp highlight, everything looks like it is made of the same plastic. Give each surface its own highlight size and edge quality. The differences between materials mostly live in that one detail.

- **Adding texture before the form is solid.** Texture on top of a flat, unconvincing form does not fix the flatness — it hides the problem and makes it harder to fix later. Get the big light-and-dark structure working first, then add surface marks on top.

- **Texture marks that run flat across the whole surface.** If you paint wood grain or fabric weave in straight parallel lines across a rounded shape, the surface will look like a label wrapped around an object rather than an object made of wood or fabric. Curve and arc your marks to match wherever the surface curves.

- **Uniform texture opacity across light and shadow.** If your texture marks are the same brightness everywhere — same opacity in the bright area and the shadow area — the texture will visually fight the light-and-dark structure and flatten the form. Reduce the marks in the shadow zone to stay below the shadow value, and let them brighten gently in the lit zone.
