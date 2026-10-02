# Form and Construction

**Status:** Work in progress.

Form is the three-dimensional volume of an object. Construction is the process of building that volume from simple, controllable primitives so that perspective, light, and proportion remain consistent.

## Primary Forms

Most complex objects can be reduced to combinations of:

- Box (or rectangular prism)
- Cylinder
- Sphere (or ellipsoid)
- Cone / pyramid

These primitives have known behaviours under perspective and under light, making them reliable starting points.

## Construction Process

1. Establish the overall proportion and orientation of the major mass using a simple primitive.
2. Subdivide or attach secondary forms while maintaining the same perspective system.
3. Refine planar orientation (which way each surface faces relative to the light and to the viewer).
4. Only after the construction is stable introduce surface detail or anatomical landmarks.

## Planar Analysis

Every curved surface can be approximated by a set of planes. Understanding the major planes of a form (front, side, top, bottom) clarifies both perspective and the pattern of light and shadow.

## Proportion Systems

- Relative measurement (comparing lengths and angles to a unit already established in the drawing).
- Known canons (for the human figure or other standardised subjects) used as starting references that are then adjusted for the specific pose and individual.
- Envelope or silhouette first, then internal structure.

## Decision Criteria

1. Prefer construction from simple volumes over copying contours.
2. Keep the same perspective system across all related forms.
3. Resolve major proportions and planar orientation before surface detail.
4. Use the construction as a primary source; later rendering should not silently alter the underlying volumes.

## Common Failure Modes

- Contour-chasing without an underlying volume, producing flat or inconsistent forms.
- Changing the implied light direction or perspective mid-construction.
- Adding detail to a construction that still has unresolved proportion or orientation errors.

## Relationship to Pipeline

_Pipeline step relationships pending #36 validation. This section will be updated once the confirmed pipeline structure exists._
## Plain-English Guide

> **Who this is for:** Someone opening a digital painting app for the first time with no formal art training.

### What is form and construction?

When you look at a photograph of a person or an object, it looks solid — you can tell it has depth, weight, and takes up real space. Getting that same "filled-in, you-could-pick-it-up" feeling in a painting is what this topic is about. The basic idea is: before you worry about texture, colour, or fine detail, first rough in the object using the simplest possible solid shapes — a box, a tube, a ball, a cone. Once those rough shapes are in the right position, at the right size, and at the right angle, everything you paint on top will automatically look correct. If you skip that step and just trace the outline of the thing, you end up with a flat silhouette that has no weight or depth to it.

### The key ideas, without the jargon

**The four starter shapes — the building blocks everything gets made from first:** A box, a tube, a ball, and a pointed cone are the only rough shapes you need at the start. Walk through a hardware store and look at the objects on the shelves: a paint bucket is a cylinder; a brick is a box; a ball valve is a sphere with tubes attached. Everything in the store, and everything in a painting, can be roughed in with some combination of those four shapes. Getting those rough shapes right first — in terms of size, angle, and position — means light and proportion will look correct once you add the real surface on top.

**Building in depth — starting with a three-dimensional skeleton of simple shapes before adding surface:** Think about how a house is built. The crew does not start by installing door handles. They pour a foundation, frame the walls and roof in lumber, and only then add siding, windows, and hardware. The framing stage is where all the important decisions are made — room sizes, wall angles, roof pitch. If the framing is wrong, no amount of nice door handles will fix it. Building a painting works identically: rough in the big solid shapes first, get their size and angle correct, then refine the surface on top of that skeleton.

**Flat-face thinking — reading any curved surface as a set of flat faces like a cut gemstone:** Even though a nose or a shoulder is curved, your brain reads it the way it reads a cardboard box: bright side (facing the light), medium side (facing partly away), dark side (facing away). Think of a cardboard box sitting in sunlight — the top face is bright, the front face is medium, the side face is dark. Before you blend anything, ask which "face of the box" each part of your curved surface belongs to. Set those three light levels first; then soften the edges between them.

**The sense of solid three-dimensional space an object takes up — the "filled-in" feeling:** Draw a circle on paper — it looks flat, like a sticker. Now shade one side darker and put a small bright spot on the opposite side. Suddenly that same circle looks like a ball you could pick up. Nothing about the paper changed; the shading communicated that the surface wraps around a solid, space-filling ball rather than lying flat. That pickable-up quality is what you are aiming for in every object you paint.

**Wrap-around lines — lines that circle around the surface of a shape like latitude lines on a globe:** Look at a peeled orange. The segments run from top to bottom over the surface, curving over the rounded front and disappearing around the back. Those segment lines tell you exactly where the surface curves and how steeply. If you draw a circle on paper and then draw a set of horizontal lines across it that curve upward in the middle — like the latitude lines on a globe — the flat circle suddenly looks like a ball. Even if you erase those lines afterward, drawing them first will show you whether your surface is curving in the right direction.

**The rough block-in — reducing a complex object to its simplest possible version first:** If you wanted to sculpt a realistic face in clay, you would not start with the nostril. You would start with a rough egg shape the right size, then add a rough nose bump, then refine that into a nose, and only then worry about the nostril. Starting at the nostril level means you have no way of knowing whether it is in the right place or the right size. The rough block-in is that first egg — get the big shape right before going smaller.

**Comparing sizes within the drawing — using one part to measure another:** If you have already drawn a head that looks the right size, use it as a portable ruler. Hold a pencil at arm's length, use your thumb to mark the height of the head on the pencil, then swing it down to see how many of those head-heights fit in the torso. If the torso is three head-heights long when it should be two and a half, you will see the discrepancy immediately — by measuring against your own drawing, no external ruler needed.

**The outer box first — drawing the overall bounding shape before the internal details:** Think of how an experienced jigsaw-puzzle solver starts: they find all the flat-edged border pieces and build the outer frame before touching the middle. The outer frame tells you the total size and shape of the picture; then you fill in the interior. Lightly sketching the outermost boundary of your whole object — as if drawing the box it came shipped in — does the same thing: it locks in the total space before you commit to any line inside it.

### What to actually do in your software

1. **Rough in the basic shapes first using your shape tool.** In Procreate, Krita, Photoshop, or Photopea, use the basic shape tool (rectangle, ellipse) on a new layer to place a rough box or oval where the main mass of your object sits. Do not draw the details yet — just the big overall shape at the right size and angle.
2. **Add secondary shapes on separate layers.** For each major part of the object (a head, a limb, a large attached piece), add another rough oval or box on its own layer. Adjust sizes and positions until the proportions look right compared to each other. Use the head or the largest shape as a measuring guide — does the torso look about two and a half times as tall?
3. **Check the shading before you add any surface detail.** On a layer above your rough shapes, pick one direction for the light source. Use a large, soft brush to darken the side of each shape that faces away from the light, and leave the side facing the light lighter. At this point it should already look somewhat solid. If it does not, fix the shape sizes and angles before moving on.
4. **Only then start refining detail on top.** Add a new layer above everything and begin drawing the real edges and surface features. Keep the rough shape layers visible underneath as a guide — they will stop you from accidentally shrinking or stretching parts of the object as you add detail.

### Common traps to avoid

- **Drawing the outline first and filling it in.** If you trace the outer edge of an object and then colour inside the line, you get a flat shape with no depth. Instead, build inward from rough solid shapes — the outline is the last thing to refine, not the first.
- **Changing where the light is coming from halfway through.** If the left side of a shape is dark (light coming from the right), every attached shape must follow the same rule. Switching the light direction mid-painting — even slightly — makes the object look pasted together from pieces that do not belong to the same scene.
- **Adding fine detail before the big shapes are correct.** Drawing wrinkles, texture, or small features on top of a shape that is the wrong size or pointing the wrong direction does not fix the underlying problem — it hides it until the painting is almost finished and very hard to repair.
- **Blending before the three light levels are set.** On any rounded surface — a cheek, a shoulder, a rounded rock — trying to blend before you have committed to a bright side, a medium side, and a dark side results in a uniform grey smear with no sense of depth. Lock in the three levels with a flat brush first, then blend the edges between them.
