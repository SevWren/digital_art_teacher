# Stage 05 — Perspective & Construction

**Status:** Work in progress.

Stage 05 is the structural scaffolding pass. Before any surface detail, texture, or colour exists, you build the major masses of your scene as simple geometric shapes — boxes, tubes, balls — and confirm that they all sit in the same consistent space. This stage answers the question: *do the forms sit convincingly in space?* A construction drawing that passes this check becomes a primary reference for every later stage; changing the perspective after rendering has begun is one of the most costly errors in the pipeline.

---

## What You Do at This Stage

- Place a horizon line (eye-level line) across the canvas and decide how many convergence dots you need for your viewpoint.
- On a dedicated layer, rough in each major mass using simple box or cylinder shapes. Do not draw the final surface yet — draw the underlying skeleton first.
- Check that all edges on the same object aim at the same convergence dot. Any edge that travels away from the viewer must point to the correct dot; edges that run straight across or straight up-and-down do not converge.
- Confirm that every object sits on a shared ground. Nothing should float or lean unless deliberately designed to do so.
- Preserve the gesture and silhouette approved in Stage 04 — the construction should reinforce the big shapes, not contradict them.
- Keep the construction layer visible and locked; later stages paint on top of it, not instead of it.

---

## Stage Sign-off Condition

All major masses are constructed as simple geometric shapes on a dedicated layer, with consistent perspective throughout the scene. Every grounded object has a visible contact point with the surface it rests on, and the implied viewer position has not shifted between objects. The gesture from Stage 04 still reads beneath the construction.

---

## Common Failure Modes

- **Mixed convergence dots.** Different edges of the same box aim at slightly different dots because each edge was drawn by eye at a different moment. The object looks twisted or bent even though every individual line looks plausible. Fix by placing dot guides first and snapping all edges to them.
- **No horizon line established.** Objects are placed without agreeing on a single eye-level line, so different objects imply different viewer heights. Figures look like they are standing on different floors; objects look pasted in from separate scenes.
- **Skipping to surface detail.** Drawing the face of a figure before the head volume is a stable box. The surface looks correct until shading is applied, at which point the underlying volume is missing and the form collapses.
- **Floating objects.** An object has no contact shadow and no ground line connecting it to the surface below, so it reads as hovering in mid-air. Adding a dark contact area at the base is a quick fix, but the real solution is to construct the ground plane and the object together from the start.
- **Moving the perspective during rendering.** A shading pass that re-draws an edge slightly off-angle from the construction drawing quietly shifts the implied viewpoint. By Stage 08 the image feels subtly wrong and the source is almost impossible to find. The construction drawing exists specifically to prevent this.

---

## Connections to Other Stages

| Stage | Relationship |
|---|---|
| 04 — Gesture / Silhouette | Construction must preserve the gesture approved here. If the boxes and cylinders kill the life of the pose, revisit Stage 04 before moving on. |
| 06 — Value / Lighting | Light direction is applied to the constructed surfaces. A stable construction drawing makes the value pass straightforward; an unstable one makes the value pass contradictory. |
| 08 — Form & Materials | Surface detail and material response are painted over the construction skeleton. The skeleton is the authority if a rendered surface starts to drift in space. |
| 10 — Atmosphere & Polish | Atmospheric perspective (distance fade) reinforces the depth relationships established here. Both linear and atmospheric depth must point in the same direction. |

---

## Plain-English Guide

> **Who this is for:** A hobbyist digital artist, no formal training, working in any app — Procreate, Krita, Photoshop, Photopea, or similar.

### What is the Perspective & Construction stage?

Think about flat-pack furniture. Before you tighten any screws, you lay out every piece, match the slots, and check that the frame is square. If you skip that check and go straight to tightening, you can end up with a warped cabinet that looks fine panel by panel but leans when you stand back. Perspective and construction is that squareness check for a painting. You build rough versions of all your major objects using simple geometric shapes — boxes and cylinders — and confirm they all sit convincingly on the same floor, pointing in the same direction, at a consistent distance from the viewer. Once that check passes, everything you paint on top will automatically look like it belongs in the same world.

---

### Key ideas, without the jargon

**Building with boxes and tubes before adding surface.**
Start every major object — a figure, a chair, a building — as the simplest solid shape it resembles. A head is roughly a box or a ball. An arm is a tube. A torso is a wider box. Draw those rough shapes first, check their sizes and angles, and only then paint the real surface on top. Think of a sculptor who starts with a rough clay block before carving the face: the block tells the sculptor where the nose can go before the nose exists. If you skip the block and go straight to the nose, you have no way of knowing whether it is in the right place.

**One dot on the horizon for a straight-on view, two dots for a corner view, three for a steep up-or-down view.**
Whenever you draw a box-shaped object, the edges that travel away from the viewer all need to aim at the same target dot on the eye-level line. If you are looking straight at the front face of an object — like looking down a corridor — everything converges to one dot. If you can see two faces of an object at once — like looking at the corner of a building — edges on the left face aim at a dot to the left and edges on the right face aim at a dot to the right. If the view is so steep (looking straight up at a tall building, or straight down from a high window) that even the upright edges visibly lean, you add a third dot above or below the canvas. Pick the right setup for your scene before drawing any edges, and stick to it.

**Why perspective must be solved now, not later.**
Perspective is the skeleton. Rendering, colour, and texture are all skin and clothing laid over the skeleton. If the skeleton is correct, the clothing fits. If the skeleton has a twisted shoulder or a leg pointing the wrong direction, no amount of careful stitching will make the clothing look right — it will just drape strangely and you will not know why. Changing the skeleton after the clothing is on means re-doing the clothing. Catching a crooked edge at Stage 05, before any rendering exists, is a one-minute fix on a separate layer. Catching the same problem at Stage 08 can mean hours of rework.

**How construction drawing keeps everything in the same space.**
When you build each object as a box or cylinder guided by the same set of dots and the same eye-level line, all the objects automatically share the same floor and the same implied distance from the viewer. They feel like they belong together. Without that shared system, objects drawn separately and pasted into a scene often look like they came from different photographs: one object implies the viewer is standing, another implies the viewer is crouching, and the scene never quite coheres.

**The "does it float or lean?" check.**
Once your rough shapes are in place, ask two questions about each grounded object. First: does it touch the ground? An object with no contact point — no shadow under it, no ground line connecting it to the floor — reads as floating. Second: does it lean? A box that is perfectly level in the real world should sit level in the drawing; if it tilts, it looks like it is about to fall over. Both of these checks take about thirty seconds per object and catch the most common space-placement errors before any surface work begins. If an object floats or leans in the rough construction, fix it now.

---

### What to do in your software

1. **Create a new layer and draw your eye-level line.** This is a single horizontal line across the full width of the canvas at the height where your imaginary viewer's eyes are. In Procreate, use Canvas > Drawing Guide > Perspective to place this line as a guide. In Krita, drag a horizontal guide from the ruler. In Photopea or Photoshop, drag a guide from the top ruler bar. Everything else in this stage follows from this one line.

2. **Place your convergence dots on that line.** For a straight-on scene (a corridor, a road going away from you): one dot, roughly centered. For a scene where you see the corners of objects: two dots, one far left and one far right. For a steep upward or downward view: two dots on the line plus a third dot far above or far below the canvas. Mark these dots clearly — they are the targets every receding edge must aim at.

3. **On a new dedicated layer, rough in each major mass as a simple shape.** Use the Rectangle or Ellipse tool to drop a rough box or oval where each main object sits. Do not draw the final surface yet. For a figure: a box for the torso, an oval or box for the head, tubes for the limbs. For a vehicle: a box for the body. For a building: stacked boxes. These shapes are a scaffold, not a finished drawing — keep them rough and fast.

4. **Check every receding edge against your dots.** Use the ruler, the Line tool, or the perspective grid overlay to extend any edge that travels away from the viewer. It should point exactly at one of your convergence dots. If it does not, correct it now. In Procreate with a Perspective Drawing Guide active, the app shows grid lines automatically — draw edges along those grid lines. In Krita, use the Perspective Grid tool from the toolbox to snap lines to the correct angles.

5. **Check the ground contact for every object.** Every object that is supposed to be resting on a surface should have a visible base where it touches that surface. Add a small dark contact mark or a ground shadow under each object. If an object floats, lower it until the base of its rough box shape sits on the ground plane.

6. **Keep this layer locked and visible for all later stages.** The construction drawing is a primary reference. If a later shading or rendering pass starts to feel spatially wrong, compare it back to this layer. The error is almost always a painted surface that has drifted from where the construction placed it.

---

### Common traps

**Skipping straight to the face, the logo, or the interesting part.**
Drawing the interesting details before the underlying shape is correct is the single most common source of rework. The detail will look right close up and wrong in the full image because the foundation under it was never established. Rough in the whole structure first — boring as it is — and the interesting parts will follow quickly and correctly.

**Drawing every edge by eye and hoping they converge.**
Even experienced artists cannot reliably draw convergent lines by eye across a full canvas. The edges end up aiming at slightly different points, and the object looks structurally broken. Place the dots first and aim every edge at the correct dot deliberately. Use the ruler or grid overlay — this is what it is there for.

**Treating the construction layer as optional or throwaway.**
Once the perspective and construction pass is solid, keep that layer. It is not a sketch you are done with — it is the structural authority for the entire remaining pipeline. Hiding or deleting it before the painting is finished removes your ability to check whether later stages have drifted from it.

**Adding rendering to fix a construction problem.**
If something looks wrong in the rough shapes — if an object looks twisted, or two objects look like they are in different spaces — adding highlight and shadow will not fix it. It will make the surface look more finished while the structural problem underneath becomes harder to see and harder to fix. If something is wrong in Stage 05, fix it in Stage 05.
