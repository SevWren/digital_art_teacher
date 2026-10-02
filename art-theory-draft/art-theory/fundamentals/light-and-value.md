# Light and Value

**Status:** Work in progress.

Value (relative lightness or darkness) is the primary carrier of form, depth, and hierarchy. Colour is applied on top of a value structure; a weak value design cannot be rescued by colour alone.

## Value Families

Most professional work organises the image into a small number of value families (commonly two or three):

- Light family (areas receiving direct or strong light)
- Shadow family (areas in form shadow or cast shadow)
- Optional mid-tone or accent family

Keeping the light family and shadow family clearly separated is the single most reliable way to maintain readable form.

## Components of Light on Form

For a simple lit form (sphere, cylinder, box):

- **Highlight** — specular reflection of the light source (small, high value).
- **Light** — surface facing the light source.
- **Halftone / Mid-tone** — transitional planes.
- **Core shadow** — the darkest part of the form shadow, where the surface turns away from the light and receives little or no reflected light.
- **Reflected light** — light bouncing from surrounding surfaces into the shadow side (usually lower in value than the light family).
- **Cast shadow** — shadow projected onto another surface; its edge hardness depends on the size and distance of the light source.
- **Occlusion / Contact shadow** — the darkest value where two surfaces meet and ambient light is blocked.

## Light Types and Roles

- **Key light** — primary, directional light that defines the main form modelling.
- **Fill light** — softer, lower-intensity light that lifts shadow values without erasing the key.
- **Rim / Back light** — light from behind that separates the subject from the background.
- **Ambient / Environment light** — diffuse illumination from the surroundings.

Describe light direction with clock position (viewer’s perspective) and elevation in degrees when precision is required.

## Decision Criteria

1. Decide the light direction and quality (hard vs soft) before detailed rendering.
2. Establish the value hierarchy of the whole image (which areas are lightest and darkest) before local form modelling.
3. Keep the light-family values and shadow-family values from mixing indiscriminately.
4. Use cast-shadow shape and edge quality as additional information about light direction and surface distance.

## Common Failure Modes

- “Muddy” values: light and shadow families intermixed so that form reading collapses.
- Over-reliance on local colour without a clear value structure.
- Ignoring reflected light or occlusion, producing floating or cut-out forms.
- Changing the light direction midway without updating all dependent shadows and highlights.

## Relationship to Pipeline

_Pipeline step relationships pending #36 validation. This section will be updated once the confirmed pipeline structure exists._
## Plain-English Guide

> **Who this is for:** Someone opening a digital painting app for the first time with no formal art training.

### What is light and value?

Before colour even enters the picture, every painting is built on one simple foundation: how light or dark each area is. Take any colour photograph and drag the Saturation slider to zero — you get a grey version. That grey version is the whole skeleton of the image. The bright areas, the dark areas, and the in-between areas all have to tell a clear story on their own before colour can help. "Value" — that means how light or dark something is, completely separate from what colour it is — is what makes objects look round, heavy, far away, or glowing with light. Colour without a strong light-and-dark foundation looks muddy and flat no matter how pretty the colours are.

### The key ideas, without the jargon

**How light or dark something is (value):** The simple measure of whether a patch in your image is closer to white, closer to black, or somewhere in between. Convert your image to black and white: what you see is purely this. Everything else in the painting sits on top of this layer.

**The bright team and the dark team (value families):** Keep all the lit areas in one brightness club and all the shadowed areas in a separate, darker club — and do not let the clubs bleed into each other. Think of a black-and-white photo: you can usually see bright blobs and dark blobs. The moment every part of your image drifts to the same in-between grey, the image looks flat and hard to read. Pick a team for each area and stick with it.

**The tiny bright glint (highlight — that means the very brightest spot on a shiny surface):** The small, almost-white dot you see on a grape, a wet eye, or a polished surface under a lamp. It sits exactly where the light source bounces most directly toward your eye. Move it to the wrong side of an object and the lighting immediately looks broken. Matte surfaces have no sharp dot at all.

**The turning surface (halftone — that means the in-between brightness zone):** Think of a cardboard box in sunlight: the top face is bright, the front face is medium, the side face is dark. Rounded things — arms, faces, mugs — follow the same logic. The medium-brightness zone is the surface that is starting to turn away from the light but has not gone fully dark yet. Without this middle zone, round things look flat.

**The belt of darkness (core shadow — that means the darkest stripe on a rounded object):** Roll a white soup can under a single desk lamp in a dim room. Look at the shadow side carefully. The very back edge picks up a little glow from light bouncing off the table, so it lightens slightly. But there is a stripe in between — getting neither the direct lamp nor the bounced glow — that is the darkest stripe on the whole can. That belt is what makes a cylinder look round rather than flat. Place your darkest values there, not at the outermost edge.

**Light bouncing back into the shadow (reflected light):** Hold your hand under your chin in a dim room with one lamp overhead. The underside of your chin is in shadow — but look closely. A faint glow from your shirt is bouncing up and lighting the shadow side slightly. That soft secondary brightness is what keeps shadows from looking like black holes cut in the paper and makes objects look like they are sitting inside a real room.

**The shadow an object throws onto another surface (cast shadow — that means the dark patch thrown by one object onto another surface):** Set a coffee mug on a table near a sunny window. The dark patch on the table extending away from the mug's base is the cast shadow. Its direction tells you where the light is coming from. Its edge sharpness tells you whether the light is harsh (crisp edge) or soft (blurry edge). Missing cast shadows make objects look like they are hovering in mid-air.

**The darkest dark where two surfaces touch (occlusion shadow — that means the tiny near-black line right where two things press together):** Put a book flat on a table and look at the thin line where the book's bottom edge meets the table. That thin strip is darker than everything else nearby because almost no light can reach down into that narrow crack. Adding this thin dark line is the single cheapest trick to make an object look like it is truly resting on a surface rather than floating above it.

**The main lamp (key light — that means the primary, directional light that does most of the work):** Think of a stage with a single powerful spotlight aimed at a performer from the upper left. That spotlight decides everything: which side of the face is bright, where the shadow falls, where the cast shadow hits the floor. Everything else is secondary. Pick one direction for your main lamp and keep it consistent across the whole painting.

**The soft fill (fill light — that means a weaker secondary light that lifts the shadows slightly):** In a dim room with one desk lamp, have someone hold a white sheet of paper near the shadow side of your hand. The paper bounces a soft, dim glow back onto the shadow side, lifting it from near-black to a deep grey. That paper-bounce is fill light. It keeps shadows from looking like voids while still keeping the lit and shadow sides clearly different.

**The glow around the edges (rim light — that means a light from behind that traces the subject's outline):** Watch a person standing in front of a bright window. Their face is in shadow, but the edges of their hair and shoulders glow because the window light is catching those back edges. That bright edge halo is what separates a subject from a similarly dark background.

**The line where light stops (terminator — that means the boundary where the lit side ends and the shadow side begins):** Stand outside on a sunny day and look at the edge on your forearm where sunlit skin ends and shadow skin begins. On a bright sunny day, that line is fairly sharp. On an overcast day, it is a wide, soft gradient. The type of light source — small and hard vs. large and soft — controls how sharp or soft that boundary is, and making it match your intended light source is what makes the lighting feel believable.

**The mirror-like glint on shiny surfaces (specular reflection — that means a direct reflection of the light source itself):** Look at a metal spoon under a kitchen light. You can see a distorted image of the light bulb reflected in the spoon's bowl. That is specular reflection — the surface is smooth enough to show you the light source directly. Matte surfaces like paper do not do this. The shinier the material, the smaller and crisper the glint; the rougher the material, the broader and softer it becomes until it disappears.

### What to actually do in your software

1. **Start in greyscale.** Before touching colour, create a new layer set to greyscale (or just work in a grey palette). Fill your subject's lit areas with a light grey and your shadow areas with a dark grey. Squint hard at the result — if the main shapes are still readable when blurry, your brightness plan is strong enough to continue.
2. **Separate your bright team from your dark team.** On your greyscale layer, use the Levels panel (Ctrl/Cmd + L in Photoshop, Photopea, or Krita) to push your darkest darks further down and your lightest lights further up. Aim for a genuine near-black somewhere and a genuine near-white somewhere — do not leave everything sitting in the middle grey range.
3. **Add the contact dark line.** On a new layer above everything, pick a very dark colour (near-black) and use a hard, small brush at full opacity to paint a thin line right at the base of every object where it meets the surface below. Set this layer's blend mode to Multiply if you want it to blend naturally with the colour underneath.
4. **Check your light consistency.** Temporarily hide all layers except your base value layer and squint. Every surface that faces your chosen light direction should be lighter; every surface turned away should be darker. If any surface is the wrong brightness for its facing direction, fix it on its own layer using Hue/Saturation (drag Lightness) or a Curves adjustment clipped to that layer.

### Common traps to avoid

- **Everything drifts to the same medium grey.** If you keep blending the bright areas into the dark areas without committing to which is which, the whole image becomes a flat grey mush — like pouring a little black ink into clean water over and over until the water is neither clear nor black. Fix it with a Levels or Curves adjustment: drag the darks darker and the lights lighter until the two groups are clearly separate again.
- **The colour looks fine but something is still wrong.** Often the real problem is that the light-and-dark structure underneath the colour is too flat. Desaturate your image (drag Saturation to -100 in Hue/Saturation) and look at the grey version. If the subject blends into the background or the shapes are hard to read in grey, adding more colour will not fix it — the brightness structure needs work first.
- **Objects look like they are floating.** This almost always means two things are missing: the thin near-black line where the object meets the surface (the contact dark), and the dark patch extending away from the object's base in the direction opposite your light source. Add both and the object will immediately look like it is resting on something solid.
- **The light direction keeps shifting across the painting.** Pick a clock position for your main lamp (e.g., "light comes from the upper-left, roughly 10 o'clock") and write it down or pin a note to your canvas. Every shadow, every bright face, every cast patch must be consistent with that one direction. Changing it halfway through — even slightly — forces every shadow and glint to be repainted, which is much harder than locking the direction at the start.
