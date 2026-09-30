# Validated Response Examples
**Status:** Authoritative. These are the two owner-approved examples that define the target output format for the art teaching assistant. They are the required source for Section 5 of `docs/specs/response-format.md`.

---

## Example 1 — Single image, depth advice

**Scenario:** User provides an image of their existing drawing and says: "Give me advice on how to give the background elements more depth."

**Response:**

To push the background far into the distance and make the scene feel huge, focus on these four techniques:

---

### 1. Add a Layer of Soft Haze along the Horizon
The easiest way to show distance is the air itself:
* On a new layer between your water and your clouds, use a large, soft airbrush with a low-opacity gray or soft white.
* Lightly brush across the horizon line.
* This knocks back the contrast, blurs the hard boundary between water and sky, and instantly makes the horizon feel miles away.

---

### 2. Give the Clouds 3D Form and Softness
Right now, the cloud band looks like a flat cutout strip:
* **Light the tops, shadow the bases:** Pick a gentle top light (from the moon or stars) so the puffy tops are light gray, and let the bottom edges sit in soft, dark shadow.
* **Soften the edges:** Cloud silhouettes shouldn't be crisp in the distance. Take a blur tool or soft brush and melt the distant cloud edges so they feel vaporous rather than solid.

---

### 3. Create a Sky Dome Gradient
Space feels deeper when the sky isn't a single flat shade of black:
* Keep the very top of your canvas deep pitch-black.
* Introduce a very subtle, dark-gray glow as the sky approaches the clouds and horizon. This creates a dome-like curve overhead instead of a flat backdrop.

---

### 4. Layer the Distant Ripples Beneath the Fog
* Where the water meets the clouds at the back, let the ripples fade out almost completely.
* Lower their opacity and soften their edges so they dissolve into the horizon haze. If ripples in the far distance are as sharp as the ones in front, the depth collapses.

**Quick exercise to try:** Create a blank layer just above your background clouds, grab a big soft brush set to 15% opacity, and gently spray along the bottom of the clouds where they meet the water. Watch how quickly that pushes them backward!

---

## Example 2 — Two images, style matching

**Scenario:** User provides their current drawing and a reference image, and says: "In my current image, I want to draw the water and background in the style as seen in the example image. Please assist."

**Response:**

Here is how you can bring that dark, glowing water style from your reference into your spaceship piece:

### 1. Darken the Water Base
In your reference, the water is as dark as the night sky — it acts like dark glass.
Right now, your water is a light flat gray.
Lay down a deep, near-black tone across the entire water surface. This dark base is what makes highlights and glows really pop.

### 2. Paint Highlights Instead of Inking Outlines
The reference doesn't use ink outlines for ripples; it uses light and shadow:
* **Wave Crests (The Tops):** Paint sharp, bright white-to-light-gray slivers where the wave ridges catch the light.
* **Wave Troughs (The Dips):** Softly blend the back side of each ripple into the dark water.

Soften or paint over the black contour lines you currently have on the water so the ripples look like moving liquid rather than drawn rings.

### 3. Light Up the Thruster Impact Points
Your reference only has starlight, but your ship has four massive rocket engines firing straight down:
* Treat each thruster like a downward spotlight.
* Paint a bright pool of glowing light directly on the water under each blast.
* The ripple edges facing toward the thrusters should catch intense, bright highlights, while the edges facing away fall into shadow.

### 4. Push Distance with Softer Edges
To get that vast, open ocean feeling:
* **Foreground (Near you):** Keep ripple rings wider, contrasts punchy, and highlight edges crisp.
* **Horizon (Far away):** Squish the ripple ellipses flatter, pack them closer together, and lower the contrast so they fade softly into the haze beneath the clouds.

**Next step to try:** Start by filling your water layer with a dark tone, then use a light brush on a new layer to trace out the bright side of the rings right under the thrusters.

---

## What these examples confirm

**No citations appear anywhere** — not inline, not at the end. The corpus is the reasoning engine behind every technique block; it never surfaces in the response. This resolves the #27 vs #30 conflict: the corpus-as-engine principle governs. End-of-response citations are not part of the output format.

**No academic or corpus terminology appears** — "atmospheric perspective" becomes "haze along the horizon." "Value contrast" becomes "dark base makes highlights pop." The PTM handles all translation internally.

**The authorship line is held throughout** — every step tells the user HOW to do something (tool, layer, action). No step decides WHAT the image should look like beyond the user's stated goal.
