# Perspective

**Status:** Work in progress.

Perspective is the set of conventions that create the illusion of three-dimensional space on a two-dimensional surface. It governs the relative size, position, and convergence of forms and is solved most cleanly during construction.

## Linear Perspective

- **One-point** — a single vanishing point on the horizon; frontal planes remain parallel to the picture plane.
- **Two-point** — two vanishing points on the horizon; the dominant edges of boxes converge to these points; no plane is parallel to the picture plane except verticals (in standard setups).
- **Three-point** — a third vanishing point above or below the horizon for strong upward or downward views; verticals converge.

Key terms:
- **Horizon line** — eye-level line; vanishing points for horizontal edges lie on it.
- **Vanishing point** — point toward which a set of parallel edges appears to converge.
- **Station point / camera position** — the implied location of the viewer.
- **Cone of vision** — the angular field that remains relatively free of extreme distortion; typically kept within roughly 60 degrees for naturalistic results.

## Atmospheric (Aerial) Perspective

Distant forms exhibit:
- Reduced contrast
- Reduced saturation
- Shift toward the colour of the intervening atmosphere (often cooler and lighter in outdoor daylight)
- Softened edges and loss of fine detail

Atmospheric perspective operates independently of linear perspective and can be used even in images that lack strong linear construction.

## Foreshortening

When a form is oriented toward or away from the viewer, its projected length shortens. Accurate foreshortening requires understanding the underlying construction (box, cylinder, or anatomical masses) rather than simply scaling the familiar view.

## Decision Criteria

1. Establish the horizon and vanishing points early when the image contains architectural or geometric forms.
2. Keep the major forms consistent with the same set of vanishing points unless a deliberate multi-space effect is intended.
3. Use atmospheric perspective to reinforce depth even when linear perspective is subtle.
4. Check foreshortened limbs or objects against the construction of the underlying volumes.

## Common Failure Modes

- Mixed vanishing points that place forms in inconsistent spaces.
- Ignoring the horizon when placing figures or objects of known relative height.
- Over-distortion outside a reasonable cone of vision without stylistic justification.
- Treating atmospheric perspective as optional decoration rather than a spatial cue.

## Relationship to Pipeline

_Pipeline step relationships pending #36 validation. This section will be updated once the confirmed pipeline structure exists._
---

## Plain-English Guide

> **Who this is for:** Someone opening a digital painting app for the first time with no formal art training.

### What is perspective?

Perspective is a set of rules that tricks the eye into seeing depth on a flat screen. When you look down a long straight road, the two edges of the road appear to get closer together until they seem to meet in the distance — even though the road is the same width the whole way. Perspective drawing uses that natural optical behavior on purpose. Instead of guessing where to put lines, you place a dot (or a few dots) on an invisible horizontal line that sits at the viewer's eye height, and then you make all the edges that travel away from the viewer aim at those dots. Do that consistently, and a flat digital canvas reads as a three-dimensional space. Get it inconsistent — some edges aiming at one dot, others aiming at a different dot — and the scene looks subtly wrong even if the viewer cannot name why.

### The key ideas, without the jargon

**The eye-level line — the invisible horizontal line at the viewer's eye height:** In a painting, there is no actual sky-meets-water horizon, but the same invisible horizontal line exists at the height of the viewer's eyes, and all the depth-dots live on it. Stand at a beach and look out at the water: the line where the water meets the sky is exactly at your eye height. Crouch down and it drops; stand on a wall and it rises. That line is what the term "horizon line" means. Place it high in your canvas for a view looking down over a scene; place it low for a view where things tower over the viewer.

**The convergence dot — the single point where parallel lines that go into the distance appear to meet:** Stand between two parallel train rails and look down the track. The rails are always the same distance apart, but to your eyes they appear to touch at a single point far ahead. That meeting point is what the term "vanishing point" means. In your painting, you place a dot on the eye-level line and make all the lines that travel away from the viewer in the same direction aim at that single dot.

**Single-dot depth — when you look straight at the front face of something:** Stand in the middle of a long hallway and look straight ahead. Every line going away from you — the top edge of the wall, the bottom edge, the ceiling, the floor — all slope toward one single dot at the far end. That is what "one-point perspective" means. Use it when the viewer is looking straight at the front of a wall, a corridor, or a road.

**Two-dot depth — when you see a corner of something:** Stand at a street corner and look at the building corner in front of you. The left face of the building has its horizontal edges running away to the far left; the right face has its horizontal edges running away to the far right. Two sets of lines, two separate dots, both sitting on the same eye-level line. That is "two-point perspective" — use it whenever you can see two faces of an object at once.

**Three-dot depth — used for steep up-or-down views:** Stand at the base of a very tall building and look straight up. The vertical corners of the building, which you know are perfectly straight up-and-down, appear to lean toward each other as they rise and seem to meet far above your head. That meeting point above (or below, if you are looking down) is the third dot. Use this when the view is so steep that even the upright edges of things visibly tilt.

**Camera position — where you decide the viewer is standing:** Think of placing a camera on a tripod in a room. Where you put the tripod — how far from the objects, how far to the left or right, and at what height — determines every perspective line in the drawing. Decide this clearly and stick to it. When a painting looks subtly wrong in ways that are hard to name, it is often because this implied camera position has shifted partway through the drawing.

**The safe drawing zone — how wide an angle you can draw before things look stretched:** Hold both arms out to your sides and look straight ahead. You can sense your fingertips at the extreme edges of your vision, but they look blurry and distorted out there. Bring your hands in to a comfortable reading distance in front of you — that narrower zone is where things look natural. Objects drawn too close to the edges of a very wide scene start to look stretched or leaning for the same reason. Keep most of the action in the comfortable central zone.

**Distance fade — how objects get hazier, lighter, and less colorful the further away they are:** Look out a window at a mountain range on a hazy day. The nearest hills are dark and show individual trees with sharp edges. The hills behind them are lighter and greyer. The furthest hills are barely-there pale blue-grey shapes with no detail, almost the same tone as the sky. That is what air does when you look through miles of it — it scatters light, reduces contrast, and pushes color toward grey-blue. This works completely independently of the dot system described above, and you can use it even in scenes that have no straight-edged objects at all.

**The squishing of depth — how distances compress as they go away from the viewer:** Look down a long street with evenly spaced telephone poles. The gap between the first and second pole looks wide. The gap between the tenth and eleventh pole looks tiny, even though every gap is the same actual size. Any distance that goes away from you appears compressed. The far end of a long table is not drawn the same size as the near end — it is drawn noticeably smaller, and that compression is correct, not a mistake.

### What to actually do in your software

1. **Place your eye-level line first.** Create a new layer and draw a single horizontal guide line across the full width of the canvas at the height where your imaginary viewer's eyes are. Everything else follows from this line. In Krita, Photopea, and Photoshop, you can drag a ruler guide from the top ruler bar; in Procreate, draw a straight horizontal line using the QuickShape hold gesture and then lock that layer.

2. **Place your convergence dots on that line.** On the same guide layer, mark one dot (for a straight-on view), two dots (for a corner view), or two dots plus one far above or below the canvas (for a steep up/down view). In Procreate, use the Drawing Guide (Canvas > Drawing Guide > Perspective) to set these dots directly — the app will then show grid lines automatically. In Krita, use the Perspective Grid tool in the toolbox. In Photopea or Photoshop, place dots manually as small marks on your guide layer and use the Line tool or ruler to check edges.

3. **Draw or check all your edges against the dots.** Every edge that travels away from the viewer should, if extended, point exactly at one of your dots. Use a ruler, the Line tool with Shift held, or the perspective grid overlay to confirm this. Edges that run straight across the canvas (left-to-right) or straight up-and-down do not need to aim at any dot — only edges traveling into the distance do.

4. **Add distance fade to push backgrounds back.** On a new layer set to Normal blend mode, paint a pale, slightly blue-grey color over your background and reduce the layer's opacity until the background shapes look hazier and lower in contrast than the foreground. Alternatively, select background elements and use the Hue/Saturation adjustment to reduce saturation, then use Levels or Curves to pull the darkest darks to a lighter value, flattening the contrast range.

### Common traps to avoid

- **Edges aiming at different dots.** The most common mistake is having some edges of the same object aim at one dot and other edges of the same object aim at a slightly different dot — maybe because each edge was drawn by eye at a different moment. The result is that the object looks twisted or structurally broken. Use ruler guides or the perspective grid overlay to make every edge on the same face aim at exactly the same dot.

- **Forgetting to decide where the viewer's eyes are.** If you start placing objects and adding detail before you have committed to an eye-level line, each object ends up implying a slightly different viewer height. Figures feel like they are standing on different floors. Objects feel like they are floating. Fix the eye-level line first, then place everything else.

- **Drawing distant things too dark, too sharp, or too colorful.** A distant mountain painted the same dark green and sharp-edged as the foreground tree looks like it is sitting right next to the viewer. Distant things should be lighter, lower in contrast, and shifted toward a pale grey-blue. Forgetting this makes the scene look flat even when all the dot-and-line perspective is correct.

- **Stretching things at the edges of a wide scene.** Objects placed very far to the left or right edge of a wide composition — and drawn with all their edges correctly aimed at dots — can start to look bent or stretched. If an object at the edge of your canvas looks distorted even though the lines are correct, it is sitting outside the comfortable viewing zone. Either move the object closer to the center, or pull the imaginary viewer further back from the scene so the whole composition fits within a narrower angle of view.
