# Workflow Strategies

**Status:** Work in progress.

Digital media allow non-destructive iteration and the separation of concerns (value before colour, construction before detail). Professional workflows exploit these properties deliberately.

## Common High-Level Strategies

1. **Thumbnail → Value study → Colour study → Construction/Render**  
   Large compositional and value decisions are locked early; colour and detail follow.

2. **Grayscale-first (value-to-colour)**  
   The entire image is resolved in value before any hue is introduced. Colour is then applied via layers or blending modes that preserve the value structure.

3. **Shape-first / Painterly block-in**  
   Large opaque shapes establish composition and value simultaneously; edges and detail are refined later.

4. **Line-first (illustration)**  
   A clean construction or line drawing is established, then filled and rendered. Common in character and narrative illustration.

5. **Hybrid 2D/3D**  
   Perspective, camera, and major forms are blocked in 3D; the result is painted over or used as a precise underlay. The 3D pass is treated as a construction aid, not the final surface.

## Decision Criteria

- Choose the strategy that best matches the problem (strong narrative line work vs atmospheric environment vs precise product design).
- Keep primary sources (approved thumbnail, value study, construction) accessible and do not silently override them.
- Prefer non-destructive methods (layers, adjustment layers, smart objects or equivalent) until a decision is final.
- Separate exploration from commitment: early stages should be cheap to discard or revise.

## Relationship to Other Files

Load this file together with the relevant pipeline stage and the governing fundamental when advising on process choices.

---

## Plain-English Guide

> **Who this is for:** Someone opening a digital painting app for the first time with no formal art training.

### What are workflow strategies?

A workflow strategy is simply the order in which you do things when making a digital painting. Digital apps let you make changes without ever permanently destroying your earlier work — that means you can work on separate layers, undo freely, and save earlier versions as checkpoints. A good strategy takes advantage of this by making big decisions first (like where everything sits and how light and dark the scene is) before smaller decisions (like exact colours and tiny details). Doing it the other way around — adding fine detail before the big picture is sorted — is the most common reason paintings get stuck or have to be restarted.

### The key ideas, without the jargon

**Tiny rough sketches before anything detailed:** Before drawing anything properly, fill a small corner of your canvas with coin-sized rough scribbles — each one a different arrangement of the main shapes in your scene. Keep them messy and fast; the goal is only to find out which layout looks interesting. Think of a film director sketching tiny stick-figure panels on a notepad before a shoot. Those scraps of paper settle the question of where everyone stands before the cameras roll. The coin-sized sketches in your painting do the same thing: settle the layout question cheaply, before you spend hours on anything.

**Light-and-dark plan before colour:** Paint a small, rough version of your image using only grey tones — no colour at all — to check whether the bright areas and dark areas make a clear, readable picture on their own. Squint at any black-and-white photograph until your eyes almost close. What you see is a pattern of bright blobs and dark blobs. If that blurry pattern still makes an interesting picture, the image has a solid foundation. Your grey-only rough does the same test on purpose: if the dark and light shapes look interesting and clear in grey, you can add colour confidently.

**Big shapes before small shapes:** Fill each major area of your scene with a rough flat patch of colour before adding any shading, texture, or fine lines. Think of a sculptor who first builds a rough lump of clay into a head-sized ball, a torso-sized block, and two leg-sized columns before carving any facial features. All the fine carving comes after the big shapes are the right size. Blocking in the big areas of your painting first — sky, ground, character, background, each as a single flat patch — works the same way: it confirms the overall picture is working before you invest time in anything small.

**All-grey first, then colour on top:** One specific approach is to finish the entire painting in shades of grey before adding any colour at all. Colour is then added using layer blend modes — settings in the layers panel that let colour tint the grey image without erasing the light-and-dark information underneath. Imagine a black-and-white photograph of a street scene. If you lay a sheet of coloured acetate over it, the street picks up the colour tint while keeping all its shadows and highlights intact. The all-grey-first approach does the same thing digitally: the layer of grey paint carries all the light-and-shadow information, and a colour layer on top tints it without disturbing that information.

**Big shapes and lights-and-darks at the same time:** Another approach skips the all-grey stage and uses large, opaque brush strokes to establish the layout and the light-and-dark pattern simultaneously. Think of a house painter rolling large areas of wall colour on first, then coming back with a smaller brush for the trim. Nothing detailed happens until the wall is covered. In painting, this means using a large brush and bold, flat strokes to fill in rough shapes — deciding their size, position, and tone all at once — before switching to a smaller brush for any refinement.

**Clean outlines first, then fill and shade:** For illustration work — characters, objects, scenes with defined edges — some people prefer to draw clean, confident outlines first and add colour and shading inside them afterward. This is like the way a colouring book works: the outlines define what everything is, and the colour fills in the spaces. It works especially well when the shapes in your image have clear, hard edges that need to be precise.

**Using a 3D programme as a drawing guide:** Some artists rough out a scene in a 3D programme first — placing simple box-shaped stand-ins for objects to get the perspective and proportions correct — then paint directly over the top of that 3D image. The 3D image is only a guide, like tracing paper with correct perspective lines on it. The final painting replaces or covers the 3D surface entirely.

**Making changes you can always undo:** Throughout all of these approaches, keep your work on separate layers and use tools like adjustment layers and layer masks — settings that change how your painting looks without permanently altering the paint underneath. Think of writing notes on sticky notes placed over a book page rather than writing directly in the margin with a permanent pen. The sticky notes can be peeled off at any time; the original page is untouched. Keeping your edits this way means no decision is ever permanent until you decide it is.

**Keep earlier decisions visible:** Once you have settled on a thumbnail or a grey rough that you are happy with, keep it visible in a second window or on your phone while you work on later stages. If the painting starts to feel off — the shapes look muddy, the scene feels crowded — compare what is on your canvas to that earlier decision. Imagine you spent an hour arranging furniture in a room until it felt right, then took a photograph. If a mover accidentally shifts a chair, you hold up the photograph and put it back. Your thumbnail or grey rough is that photograph: it records the decision so later stages do not accidentally undo it.

### What to actually do in your software

1. **Start with coin-sized rough sketches.** On a small area of your canvas, use a hard round brush at full opacity to scribble three or four tiny arrangements of your scene — each the size of a large postage stamp. Do not draw any detail; just dark and light shapes. Pick the one that looks most interesting and use it as your guide for the rest of the painting.

2. **Do a grey-only rough before adding colour.** Create a new canvas or a new layer group. Using only black, white, and grey, paint a rough version of your scene — rough shapes, no fine detail. Squint at it. If the bright and dark areas make a clear picture even when blurry, move on to colour. If not, adjust the grey rough until they do.

3. **Work on separate layers and name them.** In your layers panel, keep your rough sketch on one layer, your flat colours on another, and your shading on another above that. Give each layer a name (e.g. "flat colour", "shading", "line"). This lets you change or discard any single stage without affecting the others.

4. **Use adjustment layers for colour changes.** Instead of repainting areas to change the colour, add a Hue/Saturation or Color Balance adjustment layer above your painting layer. Move the sliders to test colour changes. Because the adjustment layer is separate, you can delete it or modify it at any time without touching the paint underneath.

### Common traps to avoid

- **Adding detail before the big picture is sorted.** If the layout of your scene is not working, adding detailed textures and fine lines will not fix it — those details will just have to be repainted when you correct the layout. Get the overall arrangement of shapes and the light-and-dark pattern working at a small, rough scale before zooming in on anything.

- **Painting over your earlier decisions without realising it.** If you flatten all your layers into one and keep painting, you lose the ability to go back to any earlier stage. Keep your layers separate until the very end, and save a copy of the file before any major merge.

- **Changing the colour before the grey-only rough is working.** If you skip the grey-only stage and jump straight to colour, you will often find that the painting looks flat or muddy because the light-and-dark structure underneath the colour is not solid. Colour cannot fix a weak light-and-dark plan — it will just make the weakness harder to see.

- **Treating the 3D guide as the finished painting.** If you use a 3D programme to set up your perspective, the result is a construction guide, not the final surface. The paint you apply over the top should cover, replace, and improve on the 3D image — not just lightly trace it. If the 3D output is still visible through your paint, you have not painted enough on top of it yet.
