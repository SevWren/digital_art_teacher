# Colour

**Status:** Work in progress.

Colour is organised along three perceptual axes: hue, value (lightness), and saturation (chroma). Value remains the dominant carrier of form; colour modulates mood, hierarchy, and spatial relationships on top of that structure.

## The Three Axes

- **Hue** — the named colour family (red, yellow, green, blue, etc.).
- **Value** — relative lightness or darkness (shared with the value system).
- **Saturation / Chroma** — intensity or purity of the hue.

## Key Relationships

- **Complementary pairs** — hues opposite on the colour wheel; produce strong contrast and vibration when placed adjacent at high saturation.
- **Analogous groups** — neighbouring hues; produce harmony and cohesion.
- **Temperature** — warm (reds, oranges, yellows) versus cool (blues, greens, violets). Temperature shifts can push forms forward or back and affect emotional reading.
- **Simultaneous contrast** — a colour’s appearance is altered by its surroundings; a grey next to a strong hue will take on the complementary cast.
- **Extension / Area** — a small area of intense colour can balance a large area of muted colour.

## Practical Decision Criteria for Digital Work

1. Establish the value structure first. Colour choices that ignore value hierarchy produce flat or confused results.
2. Limit the palette deliberately. A restricted set of hues and a clear dominant temperature usually produce stronger hierarchy than an unrestricted spectrum.
3. Assign roles: dominant hue family, supporting hues, and controlled accents.
4. Control saturation hierarchy. Highest saturation is usually reserved for the focal area or for accents that must attract attention.
5. Account for atmospheric effects: distant forms typically lose saturation and shift toward the colour of the intervening atmosphere.
6. Work in a defined colour space (commonly sRGB for screen delivery) and be aware of the difference between display-referred and scene-referred workflows when precision matters.

## Common Failure Modes

- Applying colour before the value design is locked.
- Equal saturation across the entire image, eliminating hierarchy.
- Uncontrolled temperature shifts that fight the intended spatial reading.
- Ignoring simultaneous contrast, so that colours “fight” their neighbours unexpectedly.

## Relationship to Pipeline

Colour is the primary concern of stage 07 and continues to be refined through stages 09–10. The colour study should be evaluated against the earlier value study; if the colour version destroys the value hierarchy, the colour must be adjusted or the value structure revisited.

## Plain-English Guide

> **Who this is for:** Someone opening a digital painting app for the first time with no formal art training.

### What is colour (in painting)?

Colour in a painting is not just "which colour is this object." It is a set of decisions about three separate things at once: which colour family an area belongs to (is it red, blue, green?) — that is called hue, which means "what colour it actually is, like sorting a bag of mixed M&Ms by colour"; how light or dark that area is — the same idea as a black-and-white photo; and how vivid or faded that colour looks — called saturation or chroma, which means "how punchy versus how dusty the colour is, like a neon plastic cup versus a sun-bleached garden chair of the same red." These three dials work independently, and most beginner mistakes come from adjusting one while forgetting the other two. The most important thing to understand is that the light-and-dark pattern in your painting has to tell a clear story before colour even enters the picture — if you squint at your image until the colour nearly disappears, the light-and-dark blobs that remain must still make sense on their own.

### The key ideas, without the jargon

**Which colour it is:** The basic identity of a colour — red, orange, yellow, green, blue, violet — completely separate from how bright or dark or vivid it is. Think of sorting a bag of mixed M&Ms: picking out all the red ones and all the blue ones is sorting by this. In a painting, two things can share the same colour family (both blue) while one is much darker and duller than the other.

**How vivid or faded a colour looks:** How much pure, intense colour is in an area versus how much grey has crept in. A neon-red plastic cup and a sun-bleached red garden chair are both red, but the cup is almost glowing and the chair looks dusty. Turning down this "vividness dial" on background areas makes them feel farther away and less important; turning it up on one focal area makes that area jump out for attention.

**How light or dark something is:** The brightness of an area independent of its colour. A black-and-white photo shows this alone. In a painting, getting this right matters more than any colour choice — if the light-and-dark pattern is confused, no amount of colour adjustment will fix it.

**Opposite colours that make each other pop:** Two colours that sit directly across from each other on the colour circle — red and green, orange and blue, yellow and violet — make each other look more vivid and intense when placed side by side. A stop sign against green trees looks almost electric: neither the red nor the green would look as vivid against a beige wall. A small patch of orange in a mainly blue scene will grab attention powerfully for exactly this reason.

**Neighbouring colours that feel calm together:** A cluster of colours that sit next to each other on the colour circle — yellow, yellow-green, and green, for example — look naturally peaceful together because they share common ingredients, the way a forest photograph in late summer (yellow-green through blue-green leaves) feels unified and restful. One berry of a very different colour immediately stands out because it does not belong to the neighbourhood.

**How the colours around something change how that thing looks:** The same grey square looks slightly bluish when glued onto orange paper and slightly orangish when glued onto blue paper — the grey itself did not change, but your eyes compare it to its surroundings. In a painting, a skin tone that looks perfect in isolation might look too warm or too cool once it is surrounded by other colours, for exactly this reason.

**Whether a colour feels like fire or like ice:** Colours associated with sun, fire, and heat (reds, oranges, yellows) feel warm; colours associated with sky, water, and shadow (blues, greens, violets) feel cool. Hold a lit candle in a dim room: the surfaces the flame touches glow orange-yellow, while the shadowed areas away from the flame shift toward a cooler, bluer grey. A painting that puts warm colours on lit surfaces and cool colours in shadows instantly reads as more believable and three-dimensional than one where every area is the same temperature.

**Small-but-punchy — a tiny patch of strong colour outweighs a large area of quiet colour:** A plain grey suit with a single bright red pocket square shows this perfectly — the grey covers almost the entire suit, the red covers only a tiny rectangle, yet your eye goes straight to the red. The red does not need to be bigger to compete; its intensity compensates for its small size. In a painting, a tiny accent of vivid colour placed near the focal point can balance large areas of quieter colour without the image feeling overwhelming.

**Colour that tells your eye where to look (colour pecking order):** Deliberately giving the most vivid, intense colour to the most important part of the image and using quieter, more muted colour everywhere else. Think of a magazine advertisement with a plain grey background and one product photographed in vivid gold and amber tones — the grey occupies most of the page but your eye goes directly to the product. If every area of a painting has the same level of vividness, the eye does not know where to go.

**The feeling that all the colours belong together:** When the colours in a painting feel naturally coordinated — not because every colour is the same, but because they share a common underlying thread. A forest at dawn has golden light falling on leaves ranging from yellow-green to deep green, with cool blue-green shadows and warm brown trunks — everything feels like it belongs together because all the colours share the same underlying warmth from the dawn light.

**Distance fade:** Objects in the far background look paler, less vivid, and shifted toward a cool blue-grey. On a clear day, the hills in the far distance look hazier and bluer than the trees right in front of you, because air itself has a slight blue tint that accumulates over distance. Painting distant objects with less vividness and a cooler tint automatically makes them feel farther away.

### What to actually do in your software

1. **Check your light-and-dark structure before touching colour.** In your app (Procreate, Krita, Photopea, Photoshop), desaturate a duplicate of your image — use the Hue/Saturation slider pulled all the way to the left, or add a Black and White adjustment layer. Squint at what remains. If the dark-and-light blobs don't tell a clear story (main subject clearly separated from background), fix that first before any colour decisions.

2. **Use the Hue/Saturation sliders to build a colour pecking order.** Add a Hue/Saturation adjustment layer (or use the Hue/Saturation tool on a merged copy). Pull the Saturation down on your background areas — not to grey, but far enough that they feel quieter. Keep the Saturation high only on the one area where you want the viewer's eye to land. The contrast between the vivid focal area and the quieter surroundings will do the work.

3. **Check warm-vs-cool in your shadows.** Create a new layer above your painting set to a blending mode of "Color" (or "Colour") at low opacity (10–20%). Paint a warm orange-yellow over the areas directly lit by your light source, and a cool blue-violet over the shadow areas. Toggle the layer on and off — if the painting looks more three-dimensional with it on, keep it; reduce opacity until it feels subtle.

4. **Add a tiny accent to guide the eye.** Near your focal point, create a new layer and paint a small touch of the colour that sits opposite your dominant colour on the colour circle (if your painting is mainly blue-grey, try a small warm orange-red accent). Keep it small — a few brushstrokes. Its job is not to cover area; its job is to be different enough from everything else that the eye arrives there first.

### Common traps to avoid

- **Putting colours down before the light-and-dark structure is sorted.** Adding colour to a painting whose light-and-dark pattern is already confused makes it harder, not easier, to see what is wrong — colour is vivid and distracting, and it hides weak structure. Lock in the dark-and-light pattern first.

- **Making everything equally vivid, so nothing stands out.** When every colour in the image is pushed to full intensity — background, midground, and focal point all shouting at the same volume — the eye doesn't know where to go. Vivid colour only has impact when it is surrounded by quieter, more muted areas. Think of one neon-lit carousel in an otherwise softly lit fairground versus every ride blazing at full brightness simultaneously.

- **Letting warm and cool colours fight each other with no clear winner.** When the overall image has no dominant temperature — some areas feel warm, others feel cool, with no clear leader — the whole image feels unsettled and hard to read. Decide whether this painting should feel predominantly warm or cool, then let the opposite temperature appear only as a small contrast, not as an equal partner.

- **Not accounting for how surrounding colours change what you see.** If an area looks wrong after you paint it, the problem may not be that area itself — it may be what is surrounding it. Your eyes automatically compare every colour to its neighbours. Before repainting an area, try covering the surrounding colours temporarily (a flat grey rectangle on a new layer works well) to see the area in isolation. Often the "problem" colour looks completely fine on its own.
