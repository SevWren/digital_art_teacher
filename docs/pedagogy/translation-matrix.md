# Pedagogical Translation Matrix (PTM)

**Status:** Accepted  
**Source:** ADR-0005 (Output Register and Pedagogical Translation), GitHub issue #28  
**Canonical reference for:** All plain-English term translations in user-facing output  
**Used by:** Agents formulating coaching responses, knowledge base file authors  

---

## How to use this file

When formulating a user-facing response, look up every art-theory or technical term you intend to introduce. Use the **Plain name** in headings and references. Use the **Plain definition** when introducing the concept for the first time. Use the **Example** when the user needs a concrete anchor. Use the **Use in output** sentence as the template for how to introduce the concept in a coaching context.

Every entry has been verified against the three mandatory quality tests from ADR-0005:
- **Test 1:** Zero art vocabulary in the example
- **Test 2:** Physically accurate analogy
- **Test 3:** No abstract nouns without a physical anchor

---

## Sections

1. [Composition](#composition)
2. [Light and Value](#light-and-value)
3. [Colour](#colour)
4. [Anatomy and Gesture](#anatomy-and-gesture)
5. [Form and Construction](#form-and-construction)
6. [Perspective](#perspective)
7. [Software Tools](#software-tools)
8. [Pipeline and Workflow](#pipeline-and-workflow)

---

## Composition

---

### Notan
**Plain name:** Dark-and-light skeleton
**Plain definition:** A quick two- or three-tone version of your image that lets you check whether the big dark blobs and big bright blobs make a strong picture before you spend time on any details.
**Example:** Squint hard at any photograph until everything blurs into a handful of dark blobs and bright blobs. If the blobs make an interesting pattern even when blurred beyond recognition, the photo has a strong skeleton. If the blobs all seem the same size and scattered evenly, the photo looks restless and crowded. A painting works the same way — before adding colour or detail, reduce it to dark patches and bright patches and ask whether those patches alone tell a story.
**Use in output:** Before we go further with colour or detail, let's check your dark-and-light skeleton. Squint at your image until it blurs into just a few patches. Right now those patches are [describe what is observed]. We want the biggest, boldest patch to be where you want the viewer to look first.

---

### Gestalt grouping
**Plain name:** How your eyes automatically clump things together
**Plain definition:** Your eyes automatically lump nearby or similar-looking objects into one blob before you consciously look at any of them individually.
**Example:** A flock of birds looks like one moving smudge, not 500 separate birds — your eyes automatically lump nearby things into one blob before you see the details. In a painting, three characters standing close together will read as "a group of people" before the viewer looks closely enough to count them.
**Use in output:** Your eyes are doing something useful here — they're treating those [objects/figures/shapes] as one group because they're close together. That's automatic and you can use it: if you want something to read as one big thing rather than several small things, keep the pieces near each other and give them a similar brightness level.

---

### Figure–ground
**Plain name:** Object-versus-background pop
**Plain definition:** How clearly the thing you want to show (the "figure") stands out against everything behind it (the "ground"), which is just the background.
**Example:** Think of a black chess piece sitting on a white table. The chess piece pops instantly — your eye goes straight to it because it is a different brightness from the surface it sits on. Now imagine a dark grey chess piece on a dark grey table. The piece disappears; it melts into the table. In a painting, your main subject needs enough difference in brightness or colour from what is behind it to "pop" the same way the black piece pops off the white table.
**Use in output:** Right now your [subject] is blending into the background behind it — the difference in brightness between the two is too small for the eye to separate them easily. Let's push the background slightly darker (or lighter) behind your [subject] so it pops off the page the way a black chess piece pops off a white table.

---

### Visual weight
**Plain name:** How heavy something looks on the page
**Plain definition:** How much a shape, colour, or patch of darkness pulls your eye toward it — darker, larger, or more detailed things feel "heavier" and harder to ignore.
**Example:** Put a golf ball and a bowling ball side by side on a table. Even in a photograph, your eye skips past the golf ball and lands on the bowling ball — it just feels more substantial, more present. In a painting, a large dark shape in one corner feels like a bowling ball sitting there; the eye is pulled toward it. A tiny bright dot somewhere else is like the golf ball — it exists, but it does not drag your attention the same way.
**Use in output:** The large dark patch in the [corner/area] of your image is pulling almost all the visual weight to that side. The rest of the image feels light and empty by comparison. We can rebalance by [adding weight to the opposite side / lightening that dark patch / placing a smaller accent on the other side].

---

### Hierarchy / Emphasis
**Plain name:** What the viewer should look at first, second, and third
**Plain definition:** The order in which things in your image grab the viewer's eye — you get to decide what gets noticed first, what second, and what is just background.
**Example:** Look at any newspaper front page. The biggest headline, printed boldly at the top, is what your eye lands on first. The photo below it is second. The smaller article text is third. The tiny page-number footer at the bottom is last. Nobody decided to read it in that order consciously — the sizes and boldness made the decision for them. A painting works identically: the brightest thing, or the sharpest thing, or the most isolated thing, gets looked at first.
**Use in output:** Right now your image has [two/several] things competing for first attention — your eye doesn't know where to land. Let's decide: what should the viewer notice first? Once we know that, we'll make that thing the brightest or sharpest, and quietly lower everything else one notch.

---

### Negative space
**Plain name:** The breathing room around your subject
**Plain definition:** The empty-looking areas around and between your main subjects — these areas are not wasted space; they are shapes too, and they affect how comfortable and balanced the image feels.
**Example:** Look at a silhouette of a person's profile cut from black paper and glued to a white card. Most people notice the black profile immediately. But the white shape that wraps around the profile — the white areas between the head and the edge of the card — are also shapes with their own outlines. If those white shapes are interesting and varied, the whole card looks designed. If the face is shoved into one corner and all the white clumps awkwardly on one side, the card feels lopsided. In a painting, the open space around your subject is always a shape you are actively designing, whether you think about it or not.
**Use in output:** Look at the open areas around your [subject] — the [sky/background/floor/etc.]. Right now that breathing room is [very unequal on both sides / cramped on the left / too evenly split, which makes both sides feel the same]. Adjusting the position of your subject slightly [left/right/up/down] will make those open areas more interesting shapes on their own.

---

### Tangent (compositional error)
**Plain name:** Accidental touching or kissing edges
**Plain definition:** When two separate objects in your image accidentally line up so that their edges just barely touch or one edge exactly lines up with another, which makes the image look flat and awkward.
**Example:** Imagine a photo of a friend standing in a park and a lamppost appears directly behind their head, its top edge perfectly meeting the top of their head. It looks like the lamppost is growing out of their skull. Nothing is wrong with the photo technically, but the accidental line-up is distracting and makes the photo look amateurish. The same thing happens in a painting when a sword tip just barely touches a frame edge, or a horizon line runs exactly through a character's shoulder: the eye snags on the accidental alignment and the image feels flat.
**Use in output:** There's an accidental touching edge happening between your [object A] and [object B/frame edge] — their edges are just barely meeting, which makes the eye snag there. The fix is usually small: nudge [object A] a few pixels so the edges either clearly overlap or clearly have space between them. Either overlap or clear gap — never a graze.

---

### Value massing
**Plain name:** Grouping darks together and lights together into big blobs
**Plain definition:** Keeping all the dark parts of your image connected into a few large patches, and all the bright parts connected into a few large patches, instead of scattering little dark and bright spots all over the place.
**Example:** Think about how a window at night looks from outside: the dark sky above, the dark ground below, and a rectangle of warm light in the middle. Three big blobs — two dark, one light. That window reads instantly. Now imagine someone had punched 50 tiny holes in a wall with light leaking through every hole randomly: the same amount of light is in the scene, but it is chaotic and hard to read. Value massing means treating your darks and lights the same way the window does — keeping them in a few confident blobs rather than scattering them everywhere.
**Use in output:** Right now your darks are scattered across the image in many small patches rather than gathered into a few large ones. This is making the image feel busy and hard to read from a distance. Try mentally grouping all the dark patches into two or three connected blobs, then push anything in between either into the dark blob or the light blob.

---

### Rule of thirds
**Plain name:** Off-center sweet spots
**Plain definition:** A simple placement guide that says putting your main subject at one of the four points where imaginary lines divide the image into thirds (rather than dead centre) tends to make the image feel more alive and dynamic.
**Example:** Think of any well-composed photograph of a landscape — the horizon is rarely cut exactly in half. It usually sits a third of the way down from the top, with two-thirds of sky, or a third of the way up from the bottom, with two-thirds of land. The main subject — a tree, a person, a lighthouse — usually sits near one of the crossing points of those dividing lines, not dead centre. Dead centre feels like a passport photo. A third of the way in feels like the subject belongs in a scene.
**Use in output:** Your [subject] is currently sitting right in the centre of the canvas, which gives it a passport-photo feeling — correct but static. Try shifting it toward one of the off-centre crossing points — about a third of the way in from the [left/right] edge and a third of the way down from the [top] — and see if the composition feels more alive.

---

### Golden ratio / Golden spiral
**Plain name:** Nature's off-center curve
**Plain definition:** A specific curve and proportional division found in shells, flower petals, and architectural columns, which artists and designers use as a guide for placing the main subject in a visually satisfying spot.
**Example:** Hold a nautilus shell (or look up a photo of one). Slice it open and look at the chambers inside — they grow outward in a widening spiral, each chamber about 1.6 times the size of the one before it. That same ratio appears in the way sunflower seeds are packed, in the proportions of the Parthenon's columns, and in many celebrated paintings. Artists use a version of this spiral to find a placement spot for their main subject — somewhere near the tight inner curl of the spiral — that tends to feel "just right" to human eyes without being as rigid as dead centre.
**Use in output:** The rule-of-thirds grid is a quick shortcut to a similar idea — nature tends to favour proportions close to 1 to 1.6 rather than exactly 1 to 1. If you want a more organic feel than a strict grid gives you, imagine a snail shell curling inward from one corner of your canvas. The tight inner curl of that spiral is often a great home for your focal point.

---

### Cropping
**Plain name:** Deciding what the frame cuts off
**Plain definition:** Choosing how close to zoom in and where to position the four edges of your canvas, which controls what the viewer sees and what disappears beyond the borders.
**Example:** Hold your two hands up to make a rectangular viewfinder and look through it at any room. Move your hands closer to your face and the "frame" grows — more of the room fits in. Move them farther away and the frame tightens — only a small patch of the room shows. Now tilt the frame so the window is cut in half by the right edge. The partial window looks intentional and dynamic; it implies there is more room beyond the frame. A painting frame works identically: where you cut the edges changes what feels implied, what feels complete, and what the eye finds first.
**Use in output:** The current framing is cutting off your [subject's arm/the bottom of the scene/etc.] at an awkward point — it reads as accidental rather than intentional. Try [cropping tighter so the cut is clearly deliberate / pulling the frame back so the full [object] is visible / shifting the crop so the subject sits away from the centre].

---

### Framing
**Plain name:** Using things inside the image to create a natural border around your subject
**Plain definition:** Placing objects like doorways, trees, arches, or windows inside your image so they form a natural border that draws the eye toward your main subject.
**Example:** Look through any open doorway into the room beyond. The doorframe — two vertical sides and a top bar — makes the room beyond look almost like a picture. Your eye goes straight through the opening to whatever is on the other side because the doorframe funnels your attention. Artists deliberately create the same effect inside a painting by placing a tree trunk on one side, an overhanging branch on top, and some bushes at the bottom, so the landscape beyond them feels like it is being "presented" to you through a natural doorframe.
**Use in output:** You can strengthen the sense that your viewer is "looking into" the scene by giving them a natural border to look through. Try placing a darker element — a curtain edge, a tree trunk, a doorway — along the [left/right] side of the image. It will funnel the eye toward your [main subject] the way a doorway funnels your gaze into the room beyond.

---

### Focal point
**Plain name:** The one spot you want the viewer to look at first
**Plain definition:** The single most eye-catching spot in your image — the place that grabs attention before the viewer has had any conscious choice about where to look.
**Example:** Turn on a single lamp in a dark room at night. Your eyes go directly to the lamp. You don't decide to look at it; the brightness difference makes the decision for you. Everything else in the room is dark and your eyes have nowhere else to go. In a painting, you create the same magnetic pull by making one spot clearly brighter, sharper, or more detailed than everywhere else — that spot becomes the lamp in the dark room.
**Use in output:** Right now your image has [no clear focal point / several competing spots of equal brightness]. The viewer's eye doesn't know where to land. Pick one spot — the [face, weapon, light source, etc.] — and make it the brightest or sharpest thing on the canvas. Then quietly lower everything else slightly so that one spot is the undisputed lamp in the room.

---

### Leading lines
**Plain name:** Lines that walk the eye toward your subject
**Plain definition:** Any lines, edges, or paths in your image — roads, fences, rivers, a character's outstretched arm — that naturally guide the viewer's eye from one part of the image toward your main subject.
**Example:** Stand at one end of a long straight road and look toward the horizon. Both edges of the road converge toward the same distant point. Your eye follows those edges automatically, sliding along them toward the horizon. You don't decide to do it — the converging lines pull your gaze. A painting can use any kind of line this way: the line of a banister, a character's arm pointing toward someone, a row of trees, the edge of a tabletop. If the line aims toward your focal point, the viewer's eye will follow it there.
**Use in output:** Look at the [road / arm / fence / edge] in your image — it currently leads the eye [away from your subject / off the edge of the canvas / toward a blank area]. Rotate or reposition it slightly so that it points toward [your main subject]. The viewer will follow the line there without realising they are being guided.

---

### Symmetry / Asymmetry
**Plain name:** Mirror-image balance versus lopsided-on-purpose balance
**Plain definition:** Symmetry means both halves of your image are near-identical mirror images of each other; asymmetry means the two halves are different but still feel balanced because of differences in size, brightness, or detail.
**Example:** Look at a face straight-on. The left eye roughly mirrors the right, the left cheek mirrors the right — a broad symmetry that reads as stable and calm. Now look at a photo of a person sitting at one end of a park bench with an empty bench stretching out beside them. The person is on the right, emptiness is on the left — asymmetrical. But the image still feels balanced because the empty bench implies presence, loneliness, or waiting. A perfectly symmetrical painting often reads as formal or monumental (think cathedrals). A carefully asymmetrical one can feel more alive and full of tension.
**Use in output:** Your image right now is [very symmetrical, which gives it a formal, still feeling / heavily weighted to one side in a way that feels unintentional rather than purposeful]. If you want the symmetry to feel deliberate, strengthen the [mirroring / central element] to own it. If you want asymmetry to feel intentional, add a small [darker/brighter/more detailed] accent on the lighter side to create a counterweight.

---

### Balance
**Plain name:** Making the image feel stable, not tippy
**Plain definition:** When the different areas of your image feel evenly "weighted" so the whole thing feels settled and not like it is about to fall over to one side.
**Example:** Think of a see-saw with two children of different sizes. One heavy child on the right and a light child on the left tips the see-saw down on the right. But if the light child scoots farther from the centre, the see-saw levels out — a lighter object far from centre can balance a heavier object close to centre. A painting works the same way: a large dark object close to the middle can be balanced by a small bright object near the edge, because brightness and detail attract the eye strongly even at small sizes.
**Use in output:** Your image is currently feeling a bit heavy on the [left/right/bottom] side — most of the visual weight is pooled there. You can rebalance without moving your main subject: try adding a small bright or detailed accent on the [opposite] side, or lighten a large dark area that is pulling too much attention toward one corner.

---

### Rhythm
**Plain name:** A beat or pulse that moves the eye through the image
**Plain definition:** A repeated pattern of similar shapes, colours, or intervals in your image that gives the eye a sense of movement — like a drumbeat, but visual.
**Example:** Watch telephone poles passing by through a car window on a highway. Your eye skips from pole to pole in a regular beat — pole, gap, pole, gap, pole. That regularity is soothing and creates a sense of motion even from a still image. A painting can create the same beat using repeated trees, repeated arches, repeated character poses, or repeated patches of a colour. When the beat is consistent, the eye flows through the image smoothly. When it is broken deliberately, that interruption becomes a focal point.
**Use in output:** The repeated [shapes/colours/elements] in your image are creating a nice visual beat. Right now the spacing between them is [very even, which feels mechanical / irregular in a way that feels accidental rather than expressive]. Try [evening out the spacing / adding one deliberate break in the pattern at the focal point] to turn that beat into something the eye enjoys following.

---

### Pattern
**Plain name:** A repeated design that tiles or fills an area
**Plain definition:** A visual motif — like a polka dot, a diamond grid, or a repeated leaf — that repeats at regular intervals to fill a surface or area.
**Example:** Look at the fabric on a plaid shirt. The same crossing stripes repeat across the entire shirt surface. Because the repeat is consistent, your eye reads the whole shirt as one textured surface rather than counting every individual stripe. In a painting, a background of repeated leaf shapes, or repeated scale textures on armour, works the same way: the repeating motif reads as one unified surface and the eye stops trying to read each individual piece.
**Use in output:** The repeated [texture / motif / tile] you have in the [background / armour / fabric] is working as a surface pattern. Right now it is [too large, so each repeat competes for attention / slightly irregular, which makes the surface look handmade rather than deliberate]. Try scaling it [down / up] so the individual repeats are small enough that the eye reads them as texture rather than as separate objects.

---

### Unity
**Plain name:** Making the whole image feel like it belongs together
**Plain definition:** The quality that makes all the parts of your image feel like they came from the same world rather than being pasted together from different sources.
**Example:** Imagine a jigsaw puzzle where every piece came from the same puzzle box — every piece fits with every other piece and the finished picture is one coherent image. Now imagine someone snuck in five pieces from a different puzzle. They might fill a gap, but the colour, lighting, and style will look jarring — they don't belong. A painting achieves unity when all the objects are lit by the same light source, share a consistent level of detail, and feel like they exist in the same space.
**Use in output:** Your [background/foreground character/object] currently reads as coming from a different world than the rest of the image — the [lighting direction / level of detail / brightness level] doesn't match. Let's make everything feel like it lives in the same scene by [unifying the light direction / matching the level of detail / adjusting the brightness of the outlier].

---

### Contrast (compositional)
**Plain name:** Difference that creates interest and focus
**Plain definition:** Any strong difference in your image — between bright and dark, large and small, busy and calm, smooth and rough — that makes certain areas pop and others recede.
**Example:** Imagine a page of grey text on a white background. Now imagine one sentence printed in bold black. That bold sentence jumps off the page because it is surrounded by lighter, less bold text. The difference between the bold sentence and everything around it is contrast. In a painting, placing a very dark shape right next to a very bright shape creates the same jump — the eye goes to that boundary first, before anywhere else.
**Use in output:** Your focal point needs more contrast around it — the area you want the viewer to look at first is currently about the same brightness as everything around it. Try darkening the area directly behind or beside your [subject] so that the difference between your subject and its surroundings is clearly the biggest difference in the image.

---

### Proportion
**Plain name:** How the sizes of things relate to each other
**Plain definition:** The size of one thing compared to another thing in the same image — getting this right makes objects look like they belong to the same scene; getting it wrong makes things look like toys sitting next to real people.
**Example:** Look at a family photograph where everyone is standing at different distances from the camera. The person in front looks bigger than the person in the back — and that difference in size tells you instantly who is closer. If someone edited the photo so that the person at the back was the same height as the person in front, both figures would look like they exist on a flat surface with no depth at all. In a painting, the relative sizes of objects are one of the main things your brain uses to judge distance, age, and the relationship between things.
**Use in output:** The [object/character/building] on the [left/right/background] is currently [too large / too small] relative to [the figure / the foreground objects]. That mismatch is flattening the sense of depth. Try [scaling it down / moving it slightly] so the size difference between the [near object] and the [far object] clearly communicates which one is farther away.

---

### Scale
**Plain name:** How big something is compared to its surroundings
**Plain definition:** The overall size of an object in your image relative to everything around it — scale tells the viewer whether something is enormous and imposing or small and vulnerable.
**Example:** Look at a photograph of a person standing at the base of a redwood tree. The person looks tiny — not because the photographer shrank them, but because the tree is enormous and the photo shows both together. Remove the person and you lose all sense of how large the tree is. That sense of size — how big something is compared to a known reference — is scale. Artists often place a small person or familiar object next to a large building or creature specifically to communicate scale.
**Use in output:** Right now it is hard to tell how large your [creature/building/object] is supposed to be. Consider adding a [small human figure / familiar everyday object] somewhere in the scene. The viewer's brain will immediately use it as a ruler to figure out how enormous your [main subject] is.

---

### Shape language
**Plain name:** Shape personality — whether the shapes in a design feel spiky, round, or boxy
**Plain definition:** The deliberate choice to build a character, object, or environment mostly out of one type of outline — sharp triangles, soft rounded blobs, or solid rectangles — so the viewer gets an emotional message just from the silhouette before seeing any detail.
**Example:** Look at three traffic signs: a yield sign (triangle, pointing downward), a stop sign (octagon with sharp corners), and a speed-limit sign (rectangle). Before you read a single word, each sign feels different — the triangle feels urgent, the rectangle feels calm and informational. Now imagine a villain in a cartoon drawn entirely from sharp, angular wedge shapes, versus a friendly sidekick drawn from overlapping circles and ovals. You know who to trust before seeing their face. That is shape language: the emotional message carried by the type of outline.
**Use in output:** Look at the silhouette of your character or object — strip away all the internal detail in your mind and just look at the outline. Is it built from sharp points, soft curves, or boxy flat sides? If you want the subject to feel threatening, push the sharp points further; if you want it to feel approachable, round off the corners. The outline is sending a message before the detail does.

---

### Directional force
**Plain name:** Visual push — forces inside the image that shove the eye in a particular direction
**Plain definition:** Any line, edge, value gradient, or repeated shape inside the image that acts like an arrow, pushing the viewer's gaze in a specific direction whether the viewer realises it or not.
**Example:** Stand at a busy intersection and look at the road markings painted on the tarmac: arrows pointing straight ahead, arrows bending right, arrows bending left. Your eye follows each arrow before you consciously decide to. Now replace those arrows with the edge of a tabletop in a painting, a character's outstretched arm, or a bright gradient that fades toward one corner. Each of those elements acts exactly like a painted arrow — it has a direction, and your eye follows it. A painting full of directional forces all pointing toward the focal point pulls the eye home; forces pointing toward the edge let the eye escape.
**Use in output:** Look at the [edge / arm / gradient / row of shapes] in your image — it is currently pushing the eye [toward the edge of the canvas / away from your main subject]. Try redirecting it: tilt the arm so it points toward the face, curve the road so it bends back toward the figure, or flip the gradient so it brightens toward the focal area rather than away from it.

---

### Radial balance
**Plain name:** Spoke balance — when elements radiate outward from a central point like the spokes of a wheel
**Plain definition:** A type of balance where the visual elements spread outward from one central point in all directions equally, like the petals of a flower or the spokes of a bicycle wheel.
**Example:** Look at a bicycle wheel lying flat on the ground. Every spoke goes from the central hub straight outward to the rim, and they are spaced evenly all the way around. Your eye instinctively finds the centre because everything points back to it. A dart board, a clock face, a sunflower — all of these have the same quality: radiating outward from a single centre. A painting with radial balance places the focal point at the centre and arranges all the other elements to fan outward from it in roughly even intervals.
**Use in output:** Your composition currently has all its elements radiating outward from the [central point / light source / figure]. That radial arrangement is pulling the eye toward the centre, which is working in your favour if that is your focal point. To strengthen it, make sure the elements fanning outward are roughly evenly spaced around the centre — gaps or clusters on one side will break the spoke feeling.

---

### Value notan first
**Plain name:** Dark-and-light check first — testing the big blobs before adding any detail
**Plain definition:** The practice of reducing your image to just two or three flat tones — a dark blob, a mid blob, and a light blob — before doing any detailed rendering, to make sure the large-scale arrangement of darks and lights is working.
**Example:** Squint at any photograph hard enough that all the detail blurs away and only a handful of blobs remain: a dark blob, a medium blob, a light blob. If those blobs make an interesting, readable picture even when all the detail is gone, the image has a strong dark-and-light skeleton. If the blobs all run together into one muddy medium patch, all the detail in the world will not fix the image. The dark-and-light check runs this test on purpose — before you spend hours on detail, reduce your image to two or three tones and ask whether those tones alone are telling a story.
**Use in output:** Before adding any more detail or colour, run a quick dark-and-light check. On a new layer set to Multiply or just desaturate the whole canvas temporarily, reduce the image to just two or three tones: a dark, a mid, and a light. Squint at the result. If the three tones form a clear, interesting arrangement, your foundation is solid. If everything blurs into one flat medium patch, that is the thing to fix first — no amount of detail will compensate for a weak dark-and-light skeleton.

---

### Silhouette readability
**Plain name:** Recognisable outline
**Plain definition:** Whether your main subject is instantly recognisable as a distinct shape when reduced to a flat black blob on a white background, with no internal detail visible.
**Example:** Think of the Batman logo — the black bat silhouette on a yellow background. Cover the yellow and just look at the black shape. You can still tell it is a bat immediately, even though it is just a flat black blob with no face, no texture, no detail. That is strong silhouette readability. Now imagine a character whose sword arm is raised next to their body at the same angle as the body — the arm and the body merge into one blob and you cannot tell where the arm ends and the body begins. That is weak silhouette readability.
**Use in output:** If you squint at your character until all the detail blurs away, the [arm / weapon / wing] is currently merging with the [body / background] into one indistinct blob. Try separating them — either move the [arm/wing] to a different angle, or put a sliver of [lighter/darker] background visible between them so the two shapes stay readable as separate things.

---

### Entry and path (eye path)
**Plain name:** Where the viewer enters the image and where they travel next
**Plain definition:** The route the viewer's eye takes through your image — where it lands first, where it moves next, and whether it circles back to your main subject or wanders off the edge of the canvas.
**Example:** Watch someone read a menu at a restaurant for the first time. Their eye almost always starts at the top left and moves across and down — the restaurant designer probably reinforced this with a bold header and an eye-catching daily special near the top. Then the eye drifts down through categories, landing briefly on anything with a box around it or a bold price. The eye has a path. A painting similarly has entry points (usually the most contrasting spot) and then lines, arrows, and gazes that carry the eye from there to there to there. If those paths lead off the edge of the canvas, the viewer's attention escapes and never returns to the subject.
**Use in output:** The viewer's eye is currently entering your image at [the bright area in the top right], which is great, but then the [line of the arm / fence / road] leads it directly off the [left] edge of the canvas. Let's turn that line so it curves back toward your [main subject] instead of escaping the frame.

---

## Light and Value

---

### Value
**Plain name:** How light or dark something is
**Plain definition:** The simple measure of whether a colour, a surface, or a patch in your image is closer to white, closer to black, or somewhere in between — completely separate from what colour it is.
**Example:** Take any colour photograph and convert it to black and white. Every pixel that was bright yellow, bright pink, or bright green all end up as light grey. Every pixel that was dark navy, dark red, or dark green all end up as dark grey. That black-and-white version is the value map of the photograph — it shows only how light or dark things are, with all the colour information stripped away. Everything in painting is built on this light-or-dark information first, with colour added on top.
**Use in output:** Before we look at the colour, let's check the black-and-white version of your image. If you desaturate it in your software right now (Image > Hue/Saturation > drag Saturation to -100), the thing we are looking for should still be clearly readable. Right now the [subject] [disappears/blends in] when the colour is removed, which tells us the light-and-dark structure needs strengthening first.

---

### Value family
**Plain name:** The bright team and the dark team
**Plain definition:** A group of patches in your image that are all kept at similar brightness levels so they read as belonging together — usually "the bright team" and "the dark team," kept clearly separate from each other.
**Example:** In a black-and-white photo, everything is either bright or dark. A good painting keeps all the bright things in one "team" and all the dark things in another team. The moment those teams mix everywhere into the same in-between grey — neither clearly bright nor clearly dark — the image looks flat and hard to read.
**Use in output:** Look at your image and ask: can I find a clear "bright team" and a clear "dark team"? Right now your [shadow areas / bright areas] have drifted into a medium grey that belongs to neither team. Push them back: the dark team should be clearly darker than medium grey, and the bright team should be clearly lighter than medium grey, with not too much middle-of-the-road grey in between.

---

### Light group
**Plain name:** All the bright parts of the image — one team
**Plain definition:** Every surface in your image that is being hit directly by the main light source, gathered together and kept within a similar brightness range so they all read as "lit."
**Example:** Think of a stage with a single spotlight aimed at a performer from above. Every surface the spotlight catches — the top of the head, the shoulders, the front of the chest — glows at a similar bright level. If you painted one of those spotlight-hit surfaces much darker than the others, it would look as if a second, absent spotlight was creating a random dark patch. The surfaces that a single light source hits should all belong to the same bright club — similar in brightness, even if they are different shapes or at different angles.
**Use in output:** All the surfaces that your main light is hitting — the top of the [head, shoulder, table, etc.] — should belong to the same bright team. Right now some of those lit surfaces are drifting darker than the rest of the bright team, which is making the light look inconsistent. Bring those surfaces back up in brightness until they all clearly belong together.

---

### Shadow group
**Plain name:** All the dark parts of the image — one team
**Plain definition:** Every surface in your image that is turned away from the main light source or blocked from it, gathered together and kept within a similar darker range so they all read as "in shadow."
**Example:** Look at the shaded side of a row of houses on a sunny afternoon — the side facing away from the sun. All the walls on that shaded side are dark, but they are all roughly the same level of dark. You would not expect one wall to suddenly be bright when everything else on that side is in shade. The shadow sides of objects work the same way: the dark team stays together. If one shadow area drifts much lighter than the others, your eye reads it as a second surprise light source rather than as a consistent shadow side.
**Use in output:** The shadow side of your [figure/object] should be a unified dark team. Right now some shadow patches are nearly as bright as the lit surfaces, which makes it impossible to tell which side is facing the light. Darken the shadow areas as a group so the boundary between lit and dark is clearly readable.

---

### Highlight
**Plain name:** The tiny bright glint from the light source itself
**Plain definition:** The very brightest, often tiny spot on a shiny surface where the light source reflects back almost directly into the viewer's eye — like the small white dot you see on a grape or an eyeball.
**Example:** Pick up a grape and hold it under a single lamp. You will see a small bright dot or patch — almost white — at the point where the lamp's reflection is strongest. Move the grape and the dot moves with it, always sitting at the spot where the lamp bounces most directly toward your eye. That tiny dot is the highlight. It tells you instantly where the light is coming from and whether the surface is shiny or matte (matte surfaces have no sharp dot at all).
**Use in output:** Your highlight on the [eyeball / armour / wet surface] is currently sitting in the wrong place for where your light source is. If the lamp is coming from the upper left, the highlight dot should be on the upper-left edge of the [sphere / eye / surface], not the centre. Move the highlight dot to match where your light source is, and it will immediately read as the correct material.

---

### Halftone / Midtone
**Plain name:** The in-between brightness — the turning surface
**Plain definition:** The band of medium brightness on a rounded surface where the surface is neither fully facing the light nor fully turned away — the part that is transitioning from lit to dark.
**Example:** Think of a cardboard box sitting in sunlight. The top face is bright. The front face is medium. The side is dark. Even though a nose or an arm is curved, your brain reads it the same way — bright side, medium side, dark side. When painting anything rounded, start by asking: which "face of the box" is this part? The medium face is the halftone — the surface that is partly angled away from the light but not yet in full darkness.
**Use in output:** The middle-brightness band on your [rounded arm / sphere / cheek] is where the surface is turning away from the light. Right now that band is either [too wide, which makes the surface look flat / too narrow, which makes it look very shiny / the same brightness as the lit side, which removes the sense of roundness]. Darken it gradually as it approaches the fully dark side.

---

### Core shadow
**Plain name:** The darkest stripe on a rounded object — the belt of darkness
**Plain definition:** The darkest band on a rounded surface's shadow side, sitting in the zone where the surface is turning away from the light but has not yet received any light bouncing back from surrounding surfaces.
**Example:** Roll a white cylinder — a mug, a soup can, a paper roll — under a single desk lamp in a dim room. Look at the shadow side carefully. The very edge of the shadow side (the edge closest to the lit side) is dark but not the darkest. The area near the back edge (the edge closest to the table or nearby wall) also gets lighter because light is bouncing off the table back onto it. But the stripe in between — the belt that gets neither the direct lamp nor the bounced light — is the darkest stripe on the whole cylinder. That belt is the core shadow.
**Use in output:** On your [cylinder / arm / rounded object], the darkest stripe is currently [too close to the lit edge / spread too wide / not present]. The darkest belt should sit in the middle of the shadow side, not at the very edge nearest the lit area. Move your darkest values to that middle belt and let the very back edge lighten slightly.

---

### Reflected light
**Plain name:** Light bouncing off nearby surfaces back into the shadow
**Plain definition:** The faint brightness you see on the shadow side of an object caused by light that has bounced off a nearby surface — like a floor, wall, or another object — back onto the part that is facing away from the main light.
**Example:** Hold your hand under your chin and look in a mirror in a dark room with only a desk lamp above you. The underside of your chin should be in shadow — but look closely. It is not completely black. A very faint glow of light bounces off your chest or shirt and lights the underside of your chin from below. That is reflected light. It keeps shadows from looking like holes cut in the paper and makes things look like they exist in a real room rather than floating in a void.
**Use in output:** The shadow side of your [figure / object] currently looks like a flat black cutout. Add a very faint, slightly cooler brightness along the very back edge of the shadow — where a nearby [floor / wall / other surface] would be bouncing a little light back onto it. Keep it clearly darker than your main lit areas; it should whisper, not shout.

---

### Cast shadow
**Plain name:** The shadow an object throws onto another surface
**Plain definition:** The dark patch thrown by one object onto another surface — like the shadow a coffee mug throws on a desk — which tells viewers where your light is coming from and how the objects relate in space.
**Example:** Set a coffee mug on a table near a window on a sunny day. Look at the floor or table around the mug's base. There is a dark patch extending away from the mug in the direction opposite the window. That patch is the cast shadow — the mug is blocking the sunlight from hitting that patch of table. The shadow's shape tells you the mug is round. The shadow's direction tells you where the window is. The shadow's sharpness tells you whether the sun is bright and direct (sharp edges) or cloudy (soft, blurry edges).
**Use in output:** The cast shadow from your [object/figure] is currently missing [or pointing in a different direction from your other cast shadows]. This is making your [object] look like it is floating above the surface rather than resting on it. Add a dark patch extending away from the base of your [object] in the direction opposite your light source.

---

### Occlusion shadow / Contact shadow
**Plain name:** The darkest dark right where two surfaces touch
**Plain definition:** The very darkest bit of shadow in your entire image — the tiny dark line or patch at the exact point where one surface presses against or sits on another, where almost no light at all can reach.
**Example:** Put a book flat on a table and look at the thin line where the book's bottom edge meets the table surface. That thin dark line is darker than the shadow on the side of the book and darker than the cast shadow beyond the book. Light from above cannot reach down into that narrow crack between the book's bottom and the table. That paper-thin strip of near-black is the contact shadow. Adding it is what makes objects look like they are truly sitting on a surface rather than hovering slightly above it.
**Use in output:** Your [object] looks like it is floating slightly above the [floor / table / surface] it is supposed to be resting on. The fix is a single thin, very dark line right at the base where the [object] meets the [surface] — just a few pixels wide but very dark. This contact dark line is the thing that makes brains read "object is touching surface."

---

### Key light
**Plain name:** The main lamp — the one that does most of the work
**Plain definition:** The brightest, most directional light in your scene — the one that decides where all the main shadows fall and what direction your object is lit from.
**Example:** Think of a stage with a single powerful spotlight aimed at an actor from the upper left. That spotlight is doing almost all the work: it decides which side of the actor's face is bright, where the shadow falls on the neck, and where the cast shadow falls on the floor. All the other lights on the stage (if any) are weaker and secondary. In a painting, your key light is that main spotlight. Every surface that faces it is bright; every surface that turns away from it is dark.
**Use in output:** Right now your image does not have a clear main light direction — different parts of the [figure / object] appear lit from different sides. Let's pick one direction for your main lamp: upper [left/right], roughly at [10 o'clock/2 o'clock]. Once we lock that in, every lit surface should be the side that faces that clock position, and every dark surface should be the side that turns away from it.

---

### Fill light
**Plain name:** The soft secondary light that lifts the shadows
**Plain definition:** A weaker, gentler light that softens the darkness of the shadow areas slightly, so they are not completely black — it "fills in" the very darkest spots a little without erasing the clear difference between light and shadow.
**Example:** Stand near a single desk lamp in a dim room and hold your hand up so the lamp lights one side. The other side of your hand will be in shadow. Now have someone hold a white piece of paper near the shadowed side. The paper bounces a soft, dim light back onto your shadow hand, lifting it from near-black to a deep grey. Your hand now has a bright side and a slightly lifted shadow side — both clearly there, but the shadow is no longer a void. That paper-bounce is what fill light does in a painting.
**Use in output:** Your shadows are currently very dark — almost black. That can look dramatic, but if it is not intentional, add a very gentle brightening to the shadow side only. Keep the shadow side clearly darker than the lit side — if the lit side is a 9 out of 10 brightness, the fill-lit shadow should be around a 3 or 4, not a 7.

---

### Rim light / Back light
**Plain name:** The glow around the edges that separates subject from background
**Plain definition:** A light coming from behind or beside your subject that traces a bright outline along the edge of the subject, making it pop away from the background.
**Example:** Watch any backlit person standing in front of a bright window. Their face is in shadow (because the window is behind them), but the edges of their hair and shoulders glow brightly because the window light is shining directly on those edges from behind. That glowing edge halo is rim light. It works like a cookie-cutter edge — it traces the exact outline of the subject and separates it cleanly from whatever is behind it.
**Use in output:** Your [character / subject] is currently blending into the [dark / similarly coloured] background. A thin bright edge on the [left/right] side — just along the silhouette — will separate them cleanly. Set your brush to a very light colour and trace only the outer edge of the [shoulder, arm, head] where a light from behind would catch it.

---

### Ambient light
**Plain name:** The general glow from everywhere at once
**Plain definition:** The soft, directionless light that fills an environment when no single strong light source is pointing directly at something — like the light on a very overcast day where there are no distinct shadows.
**Example:** Go outside on a completely overcast, cloudy day with no sun visible. Look at your hand. It is evenly lit on all sides — there are no strong shadows, no bright spots, no dark spots. The cloud cover is scattering the sunlight in every direction equally, so the light seems to come from the whole sky at once. This even, directionless glow is ambient light. It is why objects photographed on overcast days look flat — everything is equally lit and nothing pops.
**Use in output:** Your scene currently looks like it is lit on an overcast day — everything is a similar medium brightness with soft or absent shadows. If you want stronger depth and drama, introduce a clear directional main light (from one side) so objects have a clearly bright face and a clearly dark face. Save the soft even glow for scenes where you want a gentle, low-drama mood.

---

### "Muddy values" failure mode
**Plain name:** When darks and lights have blended into a grey mush
**Plain definition:** When the bright parts of your image and the dark parts have been accidentally blended together so many times that everything is a similar medium grey and nothing reads as clearly lit or clearly in shadow.
**Example:** Take a glass of clean water and a glass of black ink. Pour a little ink into the water. Repeat many times, adding a little more each time. Eventually the water is not clean water or black ink — it is a murky grey-brown that is neither. Muddy values in a painting happen the same way: if you keep blending the lit areas into the shadow areas and the shadow areas into the lit areas without committing to which is which, everything drifts to the same in-between grey and the image looks flat and lifeless.
**Use in output:** Your image has drifted into the muddy-middle problem — most of the image is sitting around the same medium grey brightness. The fix is to commit: pick the areas that are supposed to be lit and push them brighter, pick the areas that are supposed to be dark and push them darker. Use a Levels or Curves adjustment in your software to spread the values apart again.

---

### Value compression
**Plain name:** Everything squashed into a too-narrow brightness range
**Plain definition:** When the darkest dark and the brightest bright in your image are too similar in brightness — so nothing is truly bright or truly dark and the whole image looks washed out or flat.
**Example:** Imagine a dial that goes from 0 (pure black) to 10 (pure white). If all the darks in your painting are at 4 and all the lights are at 6, you have only used the middle two notches of a ten-notch dial. The image will look grey and flat, like a photocopied photocopy that has lost its extremes. A punchy, readable painting typically uses most of the dial — the darkest darks close to 0 and the lightest lights close to 10 — even if only a small area of the painting actually reaches each extreme.
**Use in output:** Your image's darkest and lightest areas are currently too close together in brightness — the dial is only using the middle range. In your software, open the Levels panel (usually Ctrl/Cmd + L) and drag the black point slider to the right and the white point slider to the left until the image has a genuine dark and a genuine bright. The goal is to use more of the full range from dark to light.

---

### Overblending
**Plain name:** Smoothing away all the hard edges until everything looks rubbery
**Plain definition:** Blending neighbouring areas together so thoroughly with a soft brush that all the edges have disappeared and the surface looks like melted plastic or rubber instead of a real material.
**Example:** Take a pencil drawing of a ball and smudge it all over with your finger. The shading information is still there, but because every edge has been blended into every other edge, the ball looks like a smooth grey balloon with no texture, no crisp details, and no sharp accents. The edges between areas are what give a painting its sense of material — skin has some soft transitions and some crisp edges; metal has mostly crisp edges; fabric has longer gradients. When everything is equally smudged, all materials start to look the same.
**Use in output:** The [face / arm / fabric / material] in your image has been blended very smoothly and is starting to look rubbery and textureless. Try introducing some crisper edges — particularly where there should be a definite change in surface, like the edge of a [lip / crease / fold / the tiny bright glint on a shiny surface]. Not every edge needs to be hard, but right now none of them are, and that is removing the sense of material.

---

### Form shadow
**Plain name:** The dark side of a rounded object — the natural shadow of its own shape
**Plain definition:** The dark area on a rounded or angled surface where the surface itself has turned away from the light — this is the object's own built-in shadow, separate from any shadow it throws onto other surfaces.
**Example:** Hold a bowling ball under a lamp. One half of the ball faces the lamp and is bright. The other half faces away from the lamp and is dark. No other object is blocking the light from hitting the dark half — the curved surface has simply turned away from the lamp of its own geometry. That dark half is the form shadow. It is the shadow of the shape itself. It is completely separate from the cast shadow the ball throws on the floor beneath it.
**Use in output:** The dark area on the [side / back] of your [figure / sphere / arm] is the form shadow — the surface has turned away from your main light. Right now it is [too light, so the object looks flat / merging with the cast shadow, which removes the separation between the object and the floor]. Keep the form shadow on the object and the cast shadow on the surface below clearly distinct — they are two different things.

---

### Terminator (light/shadow boundary)
**Plain name:** The line where light stops and shadow begins
**Plain definition:** The edge on a surface where the lit side ends and the shadow side begins — it can be a sharp crisp line or a gradual soft band, depending on the type of light source.
**Example:** Go outside on a sunny day and hold your arm so part of it faces the sun and part of it is in shadow. Look at the exact boundary where the sunlit skin ends and the shadow skin begins. On a bright sunny day, that boundary is fairly sharp — a clear line. On a cloudy day, that boundary is a wide, soft gradient — the transition from light to dark takes up a larger area and is not a clear line at all. The size of the light source (sun on a clear day = small and sharp; overcast sky = huge and soft) determines how sharp or soft that boundary edge is.
**Use in output:** The line where your [lit side] meets your [shadow side] on the [arm / face / cylinder] is currently [too sharp for a soft light source / too blurry for a sharp midday sun]. If your scene has a hard, direct light source (a lamp, a sunny day), sharpen that boundary. If it is a soft, overcast light or a large window, soften it into a wider gradient.

---

### Specular reflection
**Plain name:** The mirror-like glint — a direct reflection of the light source
**Plain definition:** The type of reflection you see on very shiny surfaces — like metal, glass, or wet skin — where the light source itself is visibly reflected back at you as a bright glint or dot.
**Example:** Look at a metal spoon under a kitchen light. You can often see a distorted image of the light bulb itself reflected in the spoon's bowl. That is a specular reflection — the surface is smooth enough to act like a mirror and actually show you the shape of the light source. Matte surfaces like paper or unfinished wood do not do this. The shinier the material, the smaller and crisper that glint; the rougher the material, the broader and softer it becomes until it disappears entirely on a completely matte surface.
**Use in output:** Your [metal / wet / glass] surface needs a specular glint — the tiny, very bright spot that tells the viewer the surface is shiny. Right now it looks matte. Add a very small, high-contrast bright dot or stripe at the point where your light source would reflect directly toward the viewer's eye. Keep it small and crisp for very shiny materials; make it larger and softer for semi-shiny materials.

---

### Diffuse reflection
**Plain name:** The broad, scattered glow across a matte surface
**Plain definition:** The way light scatters in all directions equally off a rough or matte surface — like the flat overall brightness of a painted wall or an unpolished piece of wood — with no mirroring or glinting.
**Example:** Shine a flashlight on a blank white wall. The wall glows brightly at the spot where the beam hits, but the glow spreads in all directions — you do not see the flashlight bulb reflected in the wall. You can move your head left or right and the wall looks the same brightness from every angle. That is diffuse reflection: the surface is rough enough to scatter incoming light in every direction, so the brightness looks the same regardless of where you stand. Smooth, shiny surfaces (like a mirror or a still pond) do the opposite — they reflect the light source in one specific direction only.
**Use in output:** Your [skin / clothing / stone surface] should show a broad, even brightening on the lit side rather than a single bright glint — these are matte materials that scatter light in all directions. If you have a hard, shiny glint on them, soften it into a wide, gentle brightness across the whole face that points toward the light, rather than a concentrated dot.

---

### Local value
**Plain name:** How naturally light or dark a surface is before any lighting is applied
**Plain definition:** The inherent brightness of a surface's own colour — a white wall is inherently bright, a black cat is inherently dark — separate from whether any additional light is hitting it.
**Example:** Look at a black cat and a white cat sitting side by side in the same room, both lit by the same lamp. The white cat's lit side is very bright and its shadow side is a medium grey. The black cat's lit side is only a medium-dark grey and its shadow side is very dark — almost black. Both cats follow the exact same lighting rules, but the white cat starts from a bright starting point and the black cat starts from a dark starting point. That starting point is local value — the material's own built-in darkness or brightness.
**Use in output:** Your [dark clothing / brown fur / pale skin] has its own inherent brightness before any lighting is applied. Right now your [dark fabric] is being lit to a brightness that is almost as bright as the [light skin] nearby — the fabric's own dark nature has been lost. Keep your [dark fabric] in the dark-middle range even on its lit side; it should never be as bright as an inherently pale surface.

---

### Value scale
**Plain name:** The full brightness ladder from pure black to pure white
**Plain definition:** The complete range of possible brightnesses from the darkest possible black (step 1) to the brightest possible white (step 10), with greys in between — a reference ladder that helps you make sure you are using a wide enough range of brightnesses.
**Example:** Think of a paint store fan-deck for grey paint — 10 chips ranging from pure black at one end to pure white at the other, with 8 shades of grey in between. When you paint a picture, you are selecting which chip each area of your image sits on. A flat, grey-mush painting uses only chips 4 through 6. A punchy, well-lit painting uses chips 1 through 9 or 10. The fan-deck is the value scale; the key question is: how much of the fan-deck am I using?
**Use in output:** Look at your image and mentally assign it a fan-deck chip number from 1 (darkest) to 10 (brightest). Right now your darkest dark is probably around a [3 or 4] and your lightest light is around a [6 or 7]. That means you are only using the middle section of the ladder. Let's push your darkest areas toward [1 or 2] and your lightest areas toward [9 or 10] so you are using more of the full range.

---

### Lost edge
**Plain name:** A soft, melted boundary between two areas
**Plain definition:** A place in your image where two neighbouring areas blend together so gradually that there is no visible line or clear border between them — the two areas fade into each other.
**Example:** Look at a photo of a person's face taken in soft indoor lighting — not a harsh flash, just a window. Try to find the exact point where the bright skin on the forehead ends and the darker skin below the cheekbone begins. There is no sharp line — the skin just gradually gets darker as it curves away from the window, like a slow fade. That slow fade is a lost edge. Compare it to the edge of a printed letter on paper, which has a crisp, hard boundary you could trace with a fingernail. A painting uses both: soft fades where you want things to look gentle, distant, or atmospheric, and hard lines where you want things to look sharp and close.
**Use in output:** The boundary between the bright side and the dark side of your [cheek / hair / background] is currently a sharp, crisp line — you can trace exactly where one ends and the other begins. If you want that area to feel soft or to recede into the background, soften that boundary with a low-opacity soft brush until the transition becomes a gradual fade rather than a cut edge.

---

### Found edge
**Plain name:** A sharp, crisp boundary between two areas
**Plain definition:** A place in your image where two neighbouring areas meet at a clean, clearly defined line — you can see exactly where one thing ends and another begins.
**Example:** Look at a hardback book lying on a table in a bright room. The exact edge where the cover meets the table surface is crisp and sharp — your eye can trace it precisely. There is no blending or gradual transition; the cover just ends and the table begins. That sharp, traceable line is a found edge. In a painting, found edges draw the eye because they are crisp and defined — they feel close, sharp, and important.
**Use in output:** The sharpest, most crisply-edged areas of your painting are where the viewer's eye will land first — those hard, traceable edges signal "important, close, look here." Right now your [main subject / the face / the key edge] has been softened into a gradual fade, which is making it recede instead of pop. Sharpen that boundary using a harder brush or the Sharpen tool along just that edge.

---

### Value compression (see also the primary entry above)
*(Duplicate concept — see Value compression entry above for the full PTM entry.)*

---

### Atmospheric perspective (from glossary)
**Plain name:** Distant things look faded and bluish
**Plain definition:** The way objects far away look less sharp, less colourful, and slightly bluer or hazier than objects close to you — caused by the miles of air between you and the distant object.
**Example:** Look at a mountain range on a clear day. The nearest hills are dark green and detailed. The hills behind them are lighter green, less detailed. The mountains farthest away are pale blue-grey and almost featureless. Nothing changed about the mountains themselves — but each extra mile of air between you and them adds a faint blue haze that washes out their colour and detail. In a painting, making background objects lighter, bluer, and softer automatically makes them read as "far away" to the viewer's brain.
**Use in output:** Your [background buildings / distant trees / far mountains] are currently the same level of dark, detailed, and vivid as your foreground objects. This is making the image feel flat, as if everything is on the same plane. Lighten them, reduce their detail, and add a very slight cool (bluish) tint. Those three changes together will make them look further away.

---

### Hard light vs soft light
**Plain name:** Hard light vs soft light — the difference between a spotlight and an overcast sky
**Plain definition:** Hard light comes from a small, distant source and casts sharp-edged shadows; soft light comes from a large or close source and casts shadows with wide, gradual edges or no visible shadow edge at all.
**Example:** Go outside on a clear sunny day and look at the shadow your hand makes on the pavement. The shadow has a crisp, hard edge you could trace with a finger — that is hard light, because the sun is a small bright point in a vast sky. Now go outside on a completely overcast day and make the same shadow. The shadow is gone, or barely visible as a faint smudge with no edge at all — that is soft light, because the whole cloud cover is acting as one enormous glowing ceiling that wraps light around everything from all sides. In a painting, deciding whether your light is hard or soft decides how sharp every shadow edge in the entire image will be.
**Use in output:** Before shading anything, decide whether your light source is hard or soft. A single bare bulb, direct midday sun, or a spotlight is hard — your shadow edges will be crisp and traceable. An overcast sky, a light bounced off a large white wall, or a lamp through a diffuser is soft — your shadow edges will be wide and gradual. Right now your shadow edges are [describe what is observed], which suggests a [hard / soft] light source. Make sure all the shadow edges in the image agree with that one decision.

---

### Edge control
**Plain name:** Edge control — choosing which boundaries are sharp, which are soft, and which dissolve away
**Plain definition:** The deliberate management of how clearly defined the edges are throughout a painting — using hard edges to pull the eye in and signal sharpness, soft edges to push things back or show smooth turns, and lost edges where two areas blend together completely.
**Example:** Look at a professional photograph taken with a shallow focus setting — perhaps a portrait where the face is sharp and the background is blurred. The photographer did not accidentally blur the background; they chose to make the face sharp (a hard edge) and the background soft (a lost edge) to direct your eye straight to the face. Every painting makes the same choices, whether the artist plans them or not. A painting where every single edge is equally sharp looks like a technical drawing; a painting where every edge is equally soft looks like a fog. Variety in edge quality — some crisp, some soft, some dissolved — is what makes a painting feel alive and guides the viewer's eye.
**Use in output:** Step back and look at the edges throughout your image. Right now most edges are [equally sharp / equally soft / unvaried]. Try making the edges sharpest at your focal point — the place you want the viewer to look first — and progressively softer as you move outward into backgrounds and secondary areas. The contrast between the sharp focal edge and the softer surrounding edges will pull the eye exactly where you intend.

---

### Firm edge / soft edge
**Plain name:** Soft edge — a boundary that is blurred but still visible, used for turning surfaces and background areas
**Plain definition:** A boundary between two areas where the transition is gradual enough that you cannot trace a hard line, but the two areas do not blend completely together — they remain distinguishable as separate areas with a wide, fuzzy border between them.
**Example:** Look at a cotton ball sitting on a white table under a lamp. The shadow cast by the cotton ball has no hard line at all — it fades from dark to light so gradually that you cannot point to where the shadow starts. That is a soft edge. Compare it to the crisp edge of a glass tumbler's cast shadow on the same table — you can trace exactly where it begins. The cotton ball edge is soft; the glass edge is hard. Most painted surfaces sit somewhere between the two extremes: a cheek curving away from the light has a soft edge, not a hard line, but the boundary is still visible if you look — it has not dissolved away entirely the way a lost edge would.
**Use in output:** The transition between the lit side and the shadow side of your [cheek / rounded arm / background cloud] needs to be a soft edge — wide and gradual, not a traceable line, but still distinguishable as a boundary. Use a soft brush at low opacity and make several passes along the boundary, blending it into a band two or three brush-widths wide. The boundary should still be readable as a transition — just too gradual to trace with a fingernail.

---

## Colour

---

### Hue
**Plain name:** The colour's name — which colour it actually is
**Plain definition:** The basic identity of a colour — whether it is red, orange, yellow, green, blue, violet, or anything in between — completely separate from how bright or dark or vivid it is.
**Example:** Look at a bag of mixed M&Ms on a table. Pick out all the red ones and all the blue ones. You just sorted by hue — by which colour each candy actually *is*, regardless of how much light is hitting it. In a painting, "hue" is the same sorting question: is this area red, or is it blue, or is it somewhere between the two?
**Use in output:** Your sky and your water are both blue — they share the same basic colour family, even though one is much darker and duller than the other. Shifting one of them toward green-blue or violet-blue would give them their own identity without breaking the blue mood of the scene.

---

### Saturation / Chroma
**Plain name:** Colour vividness — how punchy or faded a colour looks
**Plain definition:** How much pure, intense colour is in a colour versus how much grey or white is mixed in — a fully vivid red versus a dusty, faded pink are the same colour but at very different levels of vividness.
**Example:** Take a neon-red plastic cup and put it next to an old, sun-bleached red garden chair. Both objects are red. But the plastic cup looks like it is almost glowing, while the chair looks dull and dusty. The only thing that changed is how much grey crept in. In a painting, turning down that "vividness dial" on an area makes it feel worn, distant, or less important — and turning it up makes that area jump out for attention.
**Use in output:** Right now, almost every part of your image is equally punchy and intense — like a room where every single person is shouting at the same volume, so no one stands out. Try dialling down the vividness in the background and farther-back areas so the main subject becomes the loudest voice.

---

### Value (in colour context)
*See "How light or dark something is" in the Light and Value section above. The same rule applies here: before adjusting colours, squint at your image until the colour nearly disappears. The light-and-dark pattern that remains must tell a clear story on its own — if it does not, fixing the colours will not help.*

---

### Colour wheel
**Plain name:** The circle that shows how all colours relate to each other
**Plain definition:** A circular chart that arranges all colours in a continuous ring — red, orange, yellow, green, blue, violet, and back to red — so you can see at a glance which colours are neighbours, which are opposites, and everything in between.
**Example:** Think of a round clock face, but instead of numbers it has colours printed around the edge: red at twelve o'clock, then orange, yellow, green, blue, violet, and back to red by the time you return to twelve. Any two colours sitting right next to each other on the clock face will look harmonious side by side. Any two colours sitting exactly opposite — red at twelve and green at six — will make each other look more intense and vibrant when placed next to each other. The colour wheel is just that clock, used for deciding which colours to put together.
**Use in output:** "Picture a clock face printed with colours instead of numbers. The colour wheel works exactly like that — colours close together on the clock face blend peacefully, while colours on opposite sides of the clock create strong, eye-catching contrast."

---

### Primary / Secondary / Tertiary colours
**Plain name:** The building-block colours, the mixed-in-between colours, and the in-between-the-in-betweens
**Plain definition:** Primary colours are the three starting points that cannot be made by mixing others (red, yellow, blue in paint; red, green, blue in light); secondary colours are made by mixing two primaries (orange, green, violet); tertiary colours are made by mixing a primary with the secondary next to it (red-orange, yellow-green, etc.).
**Example:** When you were a child with a box of crayons, red, yellow, and blue were the three crayons you could mix together to make every other colour — those are primaries. Mix the red and yellow crayons and you get orange — that is a secondary. Mix that red crayon with the orange you just made and you get a red-orange in between — that is a tertiary. On a TV or phone screen, mixing works differently: the screen makes colours by adding red, green, and blue light together, so those three are the primaries for screen work.
**Use in output:** "The three starting colours that cannot be mixed from anything else are the primaries. Mix two primaries and you get a secondary. Mix a primary with the secondary sitting next to it and you get a tertiary — one of the in-between steps. This matters because the position of your chosen colours on this chain tells you which other colours will work peacefully next to them."

---

### Complementary pairs
**Plain name:** Opposite colours that make each other pop
**Plain definition:** Two colours that sit directly across from each other on the colour circle — such as red and green, orange and blue, or yellow and violet — which make each other look more vivid and intense when placed side by side.
**Example:** Look at a stop sign (red) against a background of green trees. The red looks almost electric against the green, and the green looks unusually rich against the red. Neither colour would look as vivid sitting against a beige wall. That high-energy clash is what happens when two colours from opposite sides of the circle are placed next to each other. In a painting, a small patch of orange in a predominantly blue scene will grab attention powerfully because of this same effect.
**Use in output:** "Your main subject is a strong orange, and the background is blue — these two colours are on opposite sides of the colour circle, so they are naturally pulling against each other and making both look more vivid. That is a useful tension, but right now it is equal everywhere. Try greying down the blue in areas farther from the focal point so the tension is concentrated where you want the viewer's eye to land."

---

### Analogous groups
**Plain name:** Neighbouring colours that feel calm and unified together
**Plain definition:** A cluster of colours that sit next to each other on the colour circle — such as yellow, yellow-green, and green, or red, red-orange, and orange — and look naturally peaceful and harmonious when used together because they share common ingredients.
**Example:** Look at a photograph of a forest in late summer: the leaves range from yellow-green through mid-green to a darker blue-green, but the whole scene feels unified and restful. None of those colours are fighting each other because they are all close neighbours on the colour circle — they share a lot of the same ingredients. Compare that to how a single bright red berry in the same photo immediately grabs your eye because it is a stranger that does not belong to the neighbourhood. In a painting, sticking to neighbouring colours for large areas creates that same calm, unified feeling.
**Use in output:** "The large background areas are using colours that are close neighbours — yellow-green, green, and blue-green. Because these are neighbouring colours, they naturally feel calm and unified. This is working in your favour for the background. Now the challenge is to introduce your focal point in a colour that is *not* from that neighbourhood, so it stands out clearly."

---

### Simultaneous contrast
**Plain name:** How the colours around something change how that thing looks
**Plain definition:** When a colour looks different depending on what colour is placed next to it — the same grey square looks bluish when surrounded by orange and looks orangish when surrounded by blue — because your eyes automatically compare and adjust.
**Example:** Print two identical grey squares on paper. Glue one onto a sheet of bright orange paper and glue the other onto a sheet of bright blue paper. Hold them up and look: the grey on the orange paper looks slightly cool and bluish, while the identical grey on the blue paper looks slightly warm and orangish. The grey itself did not change — but your eyes are comparing each grey to its surroundings, and that comparison changes what you perceive. In a painting, a skin tone that looks perfect in isolation might look too warm or too cool once it is surrounded by other colours, for exactly this reason.
**Use in output:** "The area that looks too [colour description] may not actually need to change — the problem might be what is surrounding it. Your eyes automatically compare every colour to its neighbours, so the same paint colour can look completely different depending on what is next to it. Try checking that area in isolation by covering the surrounding colours temporarily."

---

### Temperature (warm/cool)
**Plain name:** Whether a colour feels like fire or like ice
**Plain definition:** Colours associated with sun, fire, and heat (reds, oranges, yellows) are called warm, while colours associated with sky, water, and shadow (blues, greens, and violets) are called cool — and mixing these feelings strategically makes a painting feel more alive and three-dimensional.
**Example:** Hold a lit candle in a dim room. The flame and the skin lit by it has a yellowish-orange glow. The shadows falling away from the flame — on the wall behind it, under the chin, in the corners of the room — shift toward a cooler, bluer grey. This happens in real life because warm light sources cast warm light on the surfaces they hit, and the shadowed areas pick up cooler ambient light from the sky or surroundings. A painting that puts warm colours on lit surfaces and cool colours in shadows instantly reads as more believable and three-dimensional than one where every area is the same temperature.
**Use in output:** "Think of the lit parts of your subject as being touched by a candle or the sun — those areas should lean toward the orange-yellow end of things. The shadows, meanwhile, have less direct light and tend to pick up cooler, bluer light from the sky or the room around them. Right now, your shadows are the same temperature as your lit areas, which makes the whole image feel a little flat and airless."

---

### Colour temperature shift
**Plain name:** The change from warm to cool (or cool to warm) across a surface or between light and shadow
**Plain definition:** The predictable way that the lit side of an object and the shadowed side often sit at opposite ends of the warm-cool scale — if the light source is warm and orange, the shadows tend to look cooler and bluer by comparison.
**Example:** Step outside on a sunny afternoon and look at a white-painted wall. The side facing the sun looks warm and slightly creamy-yellow. Walk around to the side of the wall that is in shadow, away from direct sun, and it looks cooler — slightly bluish or grey-blue — because it is now lit only by the sky above it, which is blue. The actual wall is the same white paint throughout; the shift from warm to cool is entirely caused by which light source is hitting each face. Paintings that include this shift feel more real and three-dimensional than those that simply darken the shadow without changing its temperature.
**Use in output:** "Your light side and your shadow side are both the same temperature — they feel like they are lit by the same source, just at different brightness levels. In reality, the lit side is usually warmer (more orange or yellow) and the shadowed side is usually cooler (more blue or violet), because the two faces are being lit by different sources. Try shifting your shadows a few steps toward blue-violet while keeping the lit areas on the warm side."

---

### Extension / Area ratio
**Plain name:** Small-but-punchy — why a tiny patch of a strong colour can outweigh a huge area of a quiet colour
**Plain definition:** A tiny splash of a strong, eye-catching colour can draw more attention than a huge area of a soft, dull colour — so you do not need to cover the whole image in strong colours to make one area stand out.
**Example:** Look at a plain grey suit with a single bright red pocket square. The grey covers almost the entire suit; the red covers only a tiny rectangle. Yet your eye goes straight to the red. The red does not need to be bigger to compete — its intensity compensates for its small size. If someone had printed a large red stripe across the whole jacket, the effect would be overwhelming and the grey would lose. In a painting, a tiny accent of a vivid colour placed near the focal point can balance and anchor large areas of quieter, more muted colour without the image feeling shouty or chaotic.
**Use in output:** "Right now your most vivid colour is spread across a large part of the image, which is using up all of its attention-grabbing power with nothing left for a focal point. Think of vivid colour like a strong spice — a small amount in the right place is powerful, but using it everywhere makes the whole dish taste the same. Try pulling back the vividness in the large areas and concentrating it in one smaller focal spot."

---

### sRGB / Colour space
**Plain name:** The agreed set of colours a screen can show — and the rulebook for how your file stores them
**Plain definition:** A colour space is a defined range of colours that a device can produce or a file can store; sRGB is the standard rulebook most screens and web images use, so colours look consistent whether you save, share, or open the file on a different computer.
**Example:** Imagine you describe a paint colour to a friend over the phone as "medium red." They might mix something darker or more orange than what you pictured, because "medium red" means different things to different people. Now imagine instead you give them the exact recipe: "35% red pigment, 5% white, no other pigments." They can now mix precisely what you intended. A colour space is that exact recipe system for digital images — it ensures that the "medium red" you painted on your screen looks like the same "medium red" on someone else's screen, or when it gets printed. sRGB is the most widely agreed-upon recipe system for screens and the internet.
**Use in output:** "Make sure your file is set to sRGB before you export for web or sharing. This is the colour recipe system that browsers, phones, and most screens understand. If your file is in a different system, some programs will translate it automatically but others will not, and your colours can look duller or differently tinted on someone else's screen."

---

### Colour gamut
**Plain name:** The full range of colours a device or file can actually reproduce
**Plain definition:** The complete set of colours that a specific screen, printer, or file format is physically capable of showing — some colours you can see with your eyes cannot be reproduced by a standard screen, and knowing the limits of your gamut helps you avoid planning colours that will silently shift when displayed.
**Example:** Imagine printing a photo of a neon-green sports car on a standard home inkjet printer. On screen the car looks electrically vivid, but the printed page comes out looking like a regular olive-green car. The printer's inks cannot physically make that particular neon green — it is outside the printer's range of achievable colours. That range of achievable colours is the gamut. Screens generally have a wider range than printers, which is why images often look duller when printed. High-end monitors have a wider range than standard ones. When a colour you pick is outside your output device's range, the software guesses the nearest colour it *can* show — and the result is often a surprise.
**Use in output:** "Some of the vivid colours you are seeing on screen may fall outside what can be faithfully reproduced when printed or displayed on a standard screen. This is a gamut problem — the target device's range of achievable colours is smaller than your editing display. In your export settings, look for a soft-proof or gamut-warning option to see which colours will shift before you commit to final output."

---

### Local colour
**Plain name:** What colour an object actually is when not affected by coloured light
**Plain definition:** The true, neutral colour of an object's surface as you would describe it in a normal, white-lit room — a banana's local colour is yellow, a sky's local colour is blue — before any coloured lighting, shadows, or reflections from nearby objects tint it.
**Example:** Put a red apple on a white table in a room with plain white overhead light. The apple is red. That straightforward, no-drama red is its local colour. Now shine an orange lamp on the same apple. The apple now looks orange-red on the lit side. Put it next to a bright blue tablecloth and a subtle blue tint reflects into the shadow side. The apple is still a red apple — its local colour has not changed — but what you actually see painted on it is a mixture of local colour plus light colour plus reflected colour. Beginners often paint only the local colour and wonder why things look flat; the answer is that real objects are only partly local colour, and the rest is reaction to their environment.
**Use in output:** "Your apple (or whichever object) looks flat right now because every part of it is the same straightforward red — just brighter or darker. In real life, the lit side picks up warmth from the light source, the shadow side picks up reflected colour from whatever is nearby, and only a small zone in the middle is closest to the object's 'true' colour. Try letting the lit areas drift warmer and the shadowed areas pick up a hint of whatever colour is nearby."

---

### Colour harmony
**Plain name:** The feeling that all the colours in an image belong together
**Plain definition:** When the colours in a painting feel naturally coordinated and pleasant together — not because every colour is the same, but because they have been chosen using a relationship that makes them feel like they came from the same world.
**Example:** Look at the inside of a forest at dawn: pale golden light comes through the trees and falls on leaves ranging from yellow-green to deep green, while the shadowy undergrowth has cool blue-green tones, and the trunks have warm brown tones that sit between the two. Everything feels like it belongs together even though there are multiple colours, because all of them share a similar underlying warmth from the dawn light — they are all slightly tinted the same way. Compare that to a painting where you have grabbed random colours: a harsh electric blue sky, a neon green bush, and a vivid pink building all at full vividness. Nothing links them. The first scene has colour harmony; the second does not.
**Use in output:** "Right now the colours feel like they came from different paintings — each one is fine on its own but they are not sharing any common thread. One way to unify them is to add a faint wash of the same colour over the whole image on a new layer set to a blending mode like 'Colour' or 'Overlay' at low opacity. This gives every colour a shared tint, like they are all being lit by the same light source."

---

### Split complementary
**Plain name:** One colour plus the two colours on either side of its opposite
**Plain definition:** A three-colour arrangement where you take one main colour, find its opposite on the colour circle, and then use the two colours that sit just to either side of that opposite — giving you strong contrast without the harshness of a direct opposite pair.
**Example:** Imagine you decide to use blue as your main colour. The colour directly opposite blue on the circle is orange. Instead of pairing blue with orange (which would be very stark and high-tension), you instead pair blue with the two colours that flank orange: red-orange and yellow-orange. You get interesting contrast and variety without the raw clash. Think of it like choosing not to argue directly with someone but instead having a lively discussion with their two close friends — you still get the energy and engagement, just without the head-on collision.
**Use in output:** "Your palette is built around [main colour] and its direct opposite on the colour circle — the colour sitting exactly across from it — which is creating tension everywhere. One way to keep the energy but soften the clash is to shift slightly off that direct opposite: use the two colours that sit just beside it instead. This gives you contrast and variety without the image feeling like two colours shouting at each other."

---

### Triadic
**Plain name:** Three colours spaced evenly around the colour circle
**Plain definition:** A three-colour arrangement where the colours are spread evenly around the colour circle — like points of a triangle — producing a palette that feels lively and balanced without becoming chaotic.
**Example:** Imagine a clock face with colours instead of numbers. Place a dot at twelve, a dot at four, and a dot at eight — you have divided the clock into three equal sections. The colours at those three positions are a triadic set. The classic example is red, yellow, and blue — they are equally spaced around the circle. Think of a primary school classroom: red chairs, yellow walls, blue cubbies. That bright, energetic, "everything has equal weight" feeling is the characteristic effect of a triadic palette. In a painting, a triadic palette tends to feel vibrant and balanced but can feel busy if all three colours are used at full intensity everywhere.
**Use in output:** "You are working with three colours that are roughly equally spaced around the colour circle — a triadic arrangement. This naturally creates a lively, energetic feeling. To keep it from feeling too chaotic, let one of the three colours dominate most of the painting, use the second as a supporting player, and keep the third as a small accent. That way the viewer still reads one clear mood, with the other two providing variety."

---

### Tetradic
**Plain name:** Four colours arranged as two pairs of opposites
**Plain definition:** A four-colour arrangement where the colours form two pairs of opposites — like picking two completely different pairs of opposite colours from the colour circle at once — which gives a rich, varied palette but easily becomes chaotic if no single colour is given more space than the others.
**Example:** Imagine the clock face again. Place dots at twelve, three, six, and nine — four equally spaced positions forming a square. The colours at those positions are a tetradic set. A real-world example: a garden with red roses, green leaves, orange marigolds, and blue delphiniums. All four colours are present and every pair is pulling against its opposite. It looks rich and lively in a garden where no single flower covers all the ground evenly, but if someone painted every wall of a room those four colours in equal amounts, the room would feel chaotic and unsettled. In a painting, tetradic palettes require you to decide firmly which colour gets the most space and which gets the least, otherwise the image feels like it cannot decide what it is about.
**Use in output:** "You are working with four colours arranged as two opposite pairs — a tetradic palette. This gives you a lot of richness and variety, but it is easy for a tetradic palette to feel unsettled if all four colours are fighting for equal attention. Try assigning one colour to dominate the large areas, one to handle the mid-size supporting areas, and use the remaining two only as small accents. That hierarchy will make the image feel controlled rather than chaotic."

---

### Monochromatic
**Plain name:** One colour family used throughout the image, varied only by how light or vivid it is
**Plain definition:** A colour approach that uses only one base colour — such as blue — and varies only its lightness and vividness to create the whole image, without introducing any other distinct colour.
**Example:** Look at a well-made blue-and-white ceramic bowl. The entire surface is painted using only blue, ranging from a very pale almost-white blue to a deep navy, with every shade in between. Despite having only one colour, it does not feel monotonous — it feels calm, unified, and sophisticated. That is a monochromatic approach. In a painting, working monochromatically is a useful study exercise because it removes all colour decision-making and forces you to focus on getting the lightness and darkness right first.
**Use in output:** "Try rebuilding this image using only one colour — pick a blue, a brown, whatever suits the subject — and vary only how light or dark and how vivid each area is. No other colours at all. This is a great way to check that your light-and-dark structure is solid, because without multiple colours to distract you, problems in the structure become immediately obvious."

---

### Atmospheric colour / Atmospheric perspective
*See "Distance fade" in the Perspective section. The same concept applies here from a colour perspective: distant objects look paler, less vivid, and shifted toward a cool blue-grey. Use the coaching language from that entry.*

---

### Colour mixing — additive vs subtractive
**Plain name:** Light mixing vs paint mixing — why red plus green gives yellow on a screen but mud on paper
**Plain definition:** Mixing coloured light (like on a screen) makes colours brighter — red plus green light makes yellow light; mixing coloured paints or pigments makes colours darker — red paint plus green paint makes a muddy brown, not yellow.
**Example:** Hold a red torch and a green torch and shine both beams onto the same white wall so the beams overlap. The overlapping area glows yellow. This seems bizarre — everyone learns in school that red plus green makes brown. But that is paint mixing, not light mixing. On a screen, every pixel is a tiny lamp; mixing light colours makes them brighter. In paint, pigments work the opposite way — every pigment you add absorbs more light and makes the result darker and muddier. This is why digital painting on a screen behaves differently from physical oil painting when you mix colours, and why some blending modes in painting software are named after these two different mixing systems.
**Use in output:** "In your software, different layer blending modes use different mixing rules. Modes like 'Screen' and 'Add' behave like mixing lights — they make things brighter. Modes like 'Multiply' behave like mixing paints — they make things darker. If a blend is getting unexpectedly bright or unexpectedly muddy, it is usually because the blending mode is using the wrong mixing rule for what you intended."

---

### Colour grading
**Plain name:** Adjusting the overall colour mood of a finished image
**Plain definition:** The process of adding a unified colour tint or shift to a finished image to create a specific mood or atmosphere — making the whole thing feel warmer, cooler, more nostalgic, more cinematic, or more stylised.
**Example:** Watch any modern action movie and then look at old 1990s family films. The action movie tends to have a slightly teal-and-orange look — skin tones pushed orange, shadows pushed teal. The family films tend to look warmer and softer. Neither is "correct" colour — both are deliberate colour grades applied after filming to produce a specific emotional mood, the same way a musician might add reverb to make a song feel like it is in a large hall. In a painting or digital artwork, adding a subtle overall tint on a top layer is the equivalent of this process.
**Use in output:** "Once the colours are feeling right locally, try adding a final overall colour mood. Create a new layer at the top of your layer stack, fill it with a colour — perhaps a very warm golden for a sunset feeling, or a cool pale blue for a wintry atmosphere — and reduce the layer opacity to somewhere between 5 and 20 percent. This is the equivalent of the colour grading step in film: it does not change the individual colours dramatically, but it gives everything a shared emotional tint."

---

### Desaturation
**Plain name:** Pulling the vividness out of a colour until it goes grey
**Plain definition:** The process of reducing how vivid or intense a colour is — moving it toward grey — either selectively in one area or across the whole image.
**Example:** Take a colour photograph of a bowl of fruit and drag the "Saturation" slider all the way to the left in any photo app. The image slowly loses all its colour until it becomes a pure black-and-white photo. Drag it only halfway and you get a dull, washed-out image where the colours are present but muted, as if the fruit has been sitting there for days and lost its freshness. In a painting, deliberately desaturating background areas, distant objects, or less important parts of the scene is a powerful tool for pushing those things back visually and making the focal point feel more important.
**Use in output:** "Try pulling the vividness out of the background areas — not all the way to grey, but far enough that they feel quieter and less demanding than the main subject. In [software name], you can do this with a Hue/Saturation adjustment layer with a mask that protects the focal area. The contrast between the vivid subject and the quiet background will make the subject feel more present and alive."

---

### Oversaturation failure mode
**Plain name:** When everything is too vivid at once and the image feels like it is screaming
**Plain definition:** The common mistake of making too many colours too vivid at the same time, so the image feels garish, harsh, or overwhelming — because vivid colour only has impact when it is surrounded by quieter, more muted areas.
**Example:** Think of a fairground at night with every ride lit by bright neon in multiple colours simultaneously: red, yellow, green, blue, all at maximum brightness. After a few seconds, your eyes tire and the whole scene blurs into visual noise — no single ride stands out because they are all equally loud. Now imagine the same fairground with one single neon-lit carousel at the centre and everything else lit softly and warmly. The carousel immediately becomes the centre of attention. A painting where every colour is pushed to maximum vividness has the same problem as the first fairground: everything shouts, nothing is heard.
**Use in output:** "Almost every colour in your image is pushed to full vividness right now. When everything shouts, nothing stands out. Pull back the saturation on the largest background and mid-ground areas significantly — leaving only the focal point at high vividness. You can do this quickly with a Hue/Saturation adjustment layer masked to protect the main subject. The result should be that the focal point immediately pops."

---

### Colour mudding failure mode
**Plain name:** When mixed colours turn grey-brown and lifeless
**Plain definition:** The common mistake of mixing too many different colours together (or mixing opposite colours directly) so the result becomes a dull, brownish, lifeless grey — because opposite colours cancel each other out when mixed.
**Example:** Get a tub of yellow paint and a tub of purple paint and mix them together on a palette. Instead of a bright new colour, you get a brown-grey sludge. This happens because yellow and purple are opposite colours, and mixing them cancels each other's vividness out. The same thing happens in digital painting if you blend warm and cool colours in the wrong way — instead of a lively mid-tone, you get a murky middle. The solution is usually to keep transitions between warm and cool colours as separate, crisp layers rather than blending them directly into each other.
**Use in output:** "The mid-tone area in your painting is looking muddy and grey-brown. This usually happens when warm and cool colours are being directly blended together in the same layer, which cancels their vividness out. Instead, try keeping the warm areas and cool areas on separate layers and use opacity to control their blending, or add a thin sliver of a clean, vivid accent colour along the transition edge between the two areas — this 'refreshes' the edge and removes the muddy feeling."

---

### Colour cast
**Plain name:** An unwanted overall tint that makes everything look the wrong colour
**Plain definition:** When a photo, scan, or painting has an unintended overall shift toward one colour — everything looks too yellow, too blue, too magenta — as if a tinted piece of glass has been placed over the whole image.
**Example:** Take a photo indoors under old incandescent light bulbs without adjusting your camera. Every person and surface in the photo comes out looking orange-yellow, even though people's skin does not actually look that orange in real life. The warm light from the bulbs has cast an orange tint over everything in the image. A different person photographed under an overcast sky outside often comes out looking slightly blue-purple for the same reason. That unwanted overall tint is a colour cast. In digital painting, a colour cast can also develop accidentally if you have been painting for a long time without stepping back to check that all your "white" and "grey" areas are actually neutral.
**Use in output:** "Your lightest areas — the parts that should read as white or pale grey — are actually reading as [describe the tint]. This suggests your whole image may have drifted with an overall tint in that direction. Try adding a Curves or Colour Balance adjustment layer and neutralising the tint in the midtones and highlights. Once your neutrals are genuinely neutral, every other colour will automatically look more correct."

---


---

### Colour hierarchy / Saturation hierarchy
**Plain name:** Colour pecking order — the most important area gets the most vivid colour
**Plain definition:** Deliberately assigning the most vivid, intense colours to the most important parts of the image and using quieter, more muted colours everywhere else — so the viewer's eye is guided to the right place by the colour choices, not by accident.
**Example:** Think of a magazine advertisement with a plain grey background and one product — a bottle of perfume — photographed in vivid gold and amber tones. The grey background occupies most of the page, but your eye goes directly to the bottle because it is the most vivid thing present. The art director made a deliberate decision about which element gets the most colour intensity. In a painting, if every area has the same level of vividness — background, midground, and focal point all at full intensity — the eye does not know where to go.
**Use in output:** "Right now the colour intensity is roughly equal across your whole image. Try thinking of it as a budget: you only have a limited amount of 'maximum vividness' to spend, and spending it on the main subject means spending less everywhere else. Reduce the vividness of your background by at least half. The main subject will immediately feel more important without changing anything about the subject itself."

---

### Split complementary (see also: Complementary pairs)
*Note: Full entry appears above under "Split complementary."*

---

### Display-referred vs scene-referred workflow
*(Advanced — most hobbyists painting from scratch do not need this entry.)*
**Plain name:** Screen-ready vs raw — whether your file's colours are already set up for display or still need adjusting
**Plain definition:** Most digital painting files are already set up to display correctly on screen; a raw camera file is not, and painting directly on top of one without adjusting it first can make your painted colours look wrong compared to the photo underneath.
**Example:** A JPEG photo that you open and it looks right immediately is display-referred — it has already been cooked for screen viewing. A raw camera file (like a Canon .CR2 or Nikon .NEF) is scene-referred — it stores the raw sensor data before any adjustments, giving you more flexibility but requiring you to set the look yourself. If you take a display-referred file and run it through a pipeline designed for scene-referred files, the colours will look wrong — they have been adjusted twice. For most hobbyist digital painting, you are working in display-referred mode and do not need to think about this, but if you are working with photographs as base images or delivering files to a professional pipeline, it becomes relevant.
**Use in output:** "If you are starting from a raw camera file as the base of your painting, make sure you apply the camera's colour profile before you start painting on top of it. Otherwise the colours you paint will be in a different 'colour language' than the photo underneath, and matching them will be unexpectedly difficult. For most digital painting from scratch, this is not a concern — just make sure you are working in sRGB."

---

### Colour study (vs value study)
*See "Colour study" in the Pipeline and Workflow section. Use the entry and coaching language from there.*

---

### Palette (restricted palette)
**Plain name:** The limited set of colours you decide to use for an image
**Plain definition:** The specific collection of colours you choose to work with for a painting — whether that is every colour available or a deliberately small, curated set — where a smaller, more restricted set typically produces more unified, professional-looking results.
**Example:** A professional house painter coming to paint your living room brings a few carefully chosen sample chips and asks you to pick from a coordinated range, rather than telling you to pick any colour from any of the 10,000 options in the full catalogue. The reason is that coordinated ranges are designed to work together, and picking freely from 10,000 options makes it very easy to end up with colours that clash. A restricted palette in a painting works the same way: deliberately choosing a small number of colours before you start, and mixing everything from those colours, keeps the image unified automatically.
**Use in output:** "Try restricting yourself to three or four colours for this image instead of picking colours freely as you go. Set them up as swatches at the start and commit to mixing everything from those. This constraint sounds limiting but it actually makes decisions faster and produces a more unified result — you spend less time wondering what colour to use next and more time painting."

---

### Accent colour
**Plain name:** A small pop of a contrasting colour used to draw the eye
**Plain definition:** A colour that is deliberately different from the dominant colours in the image — often more vivid or from the opposite side of the colour circle — used sparingly in one or two key places to create a focal point or add liveliness.
**Example:** Look at a room decorated entirely in greys, whites, and pale blues — calm and cohesive. Now add a single bright red throw pillow on the sofa. The pillow immediately becomes the first thing your eye goes to when you enter the room. It is the accent — a small amount of a contrasting colour in a dominant-colour environment. Remove the pillow and the room feels calm but perhaps a bit flat. Put red pillows on every chair and sofa in the room and the accent effect disappears completely because the red is no longer special. In a painting, one or two small accents of a contrasting, vivid colour near the focal point guide the viewer's eye precisely.
**Use in output:** "Your painting would benefit from a single accent — a small touch of a colour that does not belong to the main palette, placed right at the focal point. Keep it small: a hint of vivid orange against a predominantly blue scene, for example. Its job is not to cover much area; its job is to be different enough from everything else that the eye goes there first."

---

### Dominant temperature
**Plain name:** The overall warm or cool feeling of the whole image
**Plain definition:** Whether the overall feeling of the painting leans warm — like afternoon sun, orange and yellow — or cool — like a cloudy day, blue and grey — which sets the emotional mood before the viewer even looks closely at anything.
**Example:** Compare two beach photographs: one taken at golden hour, where sand, skin, and water all glow orange-yellow; the other taken on a grey overcast day, where the same sand and water look pale, cool, and slightly blue-grey. The subject is identical — a beach — but the first feels inviting, warm, and nostalgic, while the second feels lonely and cold. The difference is entirely which temperature dominates the overall image. In a painting, deciding whether warm or cool tones are in charge shapes the mood from the first second a viewer sees the image.
**Use in output:** "Before refining individual areas, decide whether this image should feel predominantly warm or predominantly cool. That dominant temperature will carry the emotional mood of the whole piece. Right now the temperature is mixed without a clear leader, which gives the image a slightly unsettled feeling. Pick one temperature to dominate — and let the other appear only as a supporting contrast."

---

### Neutral (in colour context)
**Plain name:** A colour that has had all its vividness removed — a true grey, white, or black
**Plain definition:** A colour with no discernible lean toward any particular hue — a pure grey, pure white, or pure black — which acts as a resting place for the eye and makes vivid colours nearby look more vivid by contrast.
**Example:** Look at a grey concrete pavement next to a flower bed full of red tulips. The grey pavement has no colour of its own — it is completely neutral. Because of this, the red tulips look even more vivid than they would if they were surrounded by other colours competing for attention. The pavement is doing invisible but important work: it is giving the eye a rest and making the flowers pop. In a painting, areas of true neutral grey or muted near-neutral function the same way — they give vivid accents somewhere to stand out against.
**Use in output:** "Some areas of your painting that you intend to read as neutral grey are actually slightly [warm/cool/tinted]. This is sometimes intentional — reflected light or atmosphere — but if those areas are supposed to be genuinely neutral, a slight correction in Curves or Colour Balance will make your vivid colours elsewhere feel more vivid by contrast."

---

### Munsell system
*(Advanced — most hobbyists do not need this.)*
**Plain name:** The three-axis colour address — a system that gives every colour a precise location using three measurements
**Plain definition:** A standardised framework that describes any colour using exactly three numbers: which colour family it belongs to, how light or dark it is, and how vivid or muted it is — giving every possible colour a unique, reproducible address.
**Example:** Think of how a postal address works: street name, house number, postcode — three pieces of information that together pinpoint one specific building out of millions. The Munsell system does the same thing for colour. Take a paint chip and describe it as "5R 5/10" — that means it is a middle red (5R), medium brightness (5), and very vivid (10). Anyone with the system can find that exact colour from the description alone. Without such a system, "medium red" could mean twenty different things to twenty different people. The system is used by industries that need to specify colour precisely — car paint factories, textile manufacturers, fine art conservators.
**Use in output:** If you need to match or communicate a specific colour precisely — for example, ensuring that the skin tone in a portrait is consistent across multiple sessions — the three-axis colour address system gives you a way to write down and reproduce exact colours. In most painting software, the HSB or HSL sliders are a practical approximation of the same idea: one slider for the colour family, one for brightness, one for vividness.

---

### Itten's colour contrasts
*(Advanced — most hobbyists do not need this.)*
**Plain name:** Itten's colour contrast types — the seven ways two colours can contrast with each other
**Plain definition:** A named set of seven different ways two colours can differ from each other — not just by being opposite on the colour wheel, but also by differing in brightness, temperature, vividness, or how much space each one covers.
**Example:** Put a red square next to a green square — those two colours are opposites on the colour circle and they clash intensely. That is one type of contrast. Now put the same red square next to a black square — the red stands out not because of colour opposition but because one is bright and one is dark. That is a different type of contrast. Now put a tiny red square inside a huge blue square — the red jumps out partly because it is surrounded and outnumbered. That is a third type. Itten's framework names all seven of these different kinds of colour tension, so an artist can deliberately choose which type of contrast to use — not just "make them different" but "make them different in this specific way."
**Use in output:** When deciding how to make two areas of colour feel distinct from each other, there are several different tools available beyond just making them different hues. Consider whether the contrast you want is about temperature (one warm, one cool), brightness (one light, one dark), vividness (one vivid, one muted), or area (one a tiny accent, one a large field). Naming the type of contrast you are going for helps you tune it more precisely.

---

### Bit depth
*(Advanced — most hobbyists do not need this.)*
**Plain name:** Colour depth — how many different shades of brightness your file can store
**Plain definition:** The number of distinct brightness steps a digital file can record for each colour channel — more steps mean smoother gradients and less visible banding, but also larger file sizes.
**Example:** Imagine a paint store that sells grey paint in only eight shades: pure white, near-white, light grey, medium-light grey, medium grey, medium-dark grey, dark grey, and pure black. If you try to paint a smooth sky gradient using only those eight shades, you will see visible jumps between each band — the sky does not look smooth, it looks like eight stacked stripes. Now imagine the same store sells 256 shades of grey instead of 8 — the steps are so small the eye cannot see the jumps, and the sky looks smooth. An 8-bit file gives 256 steps per channel (smooth enough for most screen work); a 16-bit file gives 65,536 steps per channel, which matters when you are doing heavy colour corrections or printing at high quality, because the extra steps prevent banding from appearing after adjustments.
**Use in output:** For most screen-based painting, 8-bit is fine. If you are planning to do a lot of colour grading or heavy Curves adjustments after painting, or if the final image will be printed at large size, consider working in 16-bit — the extra breathing room means adjustments will not introduce visible banding. You can set the bit depth when creating a new canvas (usually in the canvas settings or new document dialog).

---

## Anatomy and Gesture

---

### Gesture
**Plain name:** The main action of the whole body in one stroke
**Plain definition:** The single sweeping idea of what a person's body is doing — leaning, twisting, reaching, collapsing — before you draw any individual body part.
**Example:** Watch someone sprint for a bus. Before you register the individual legs or arms, your eye catches the whole body tipped forward, stretched diagonally like a falling plank. That full-body lean is the thing to capture first when you put pencil to paper. Every detail you draw after that should agree with that initial lean — if the lean disappears, the figure looks like it is standing still even if the legs are mid-stride.
**Use in output:** Before you draw any individual part — arm, leg, head — try laying down one single flowing stroke that captures what the whole body is doing right now. Is it leaning forward? Twisting sideways? Collapsing downward? That one stroke is your guide; every detail you add should agree with it.

---

### Line of action
**Plain name:** The spine of the pose — one curved stroke through the whole body
**Plain definition:** A single curved or S-shaped line drawn through the body from head to toe that captures the overall tilt and direction of the pose before any details are added.
**Example:** Hold a flexible plastic ruler loosely at one end and let it droop into a curve. That single curve, from top to bottom, is the line of action. Now imagine you started drawing a person by tracing that ruler first, end to end — every body part you add afterward stays consistent with that droop. If you draw the head tilted one way, the spine another, and the hips a third, it looks like three separate people glued together rather than one continuous body in motion.
**Use in output:** Try starting with a single curved stroke from the top of the head down through the spine to the feet — one flowing line that captures the overall tilt of the body. Once that line feels right, build the rest of the figure around it so everything curves the same direction.

---

### Structural anatomy (artistic)
**Plain name:** Body map — the bony bumps and big muscle shapes that actually show through the skin
**Plain definition:** A simplified map of the human body that focuses only on the bumps, ridges, and large muscle shapes that are actually visible through the skin, rather than every bone and muscle a doctor would study.
**Example:** Think of a coat hanger inside a winter jacket. You can't see the hanger directly, but you can see where its corners poke the fabric at the shoulders. You don't need to know how a coat hanger is manufactured — you just need to know where its corners are so you know where the jacket fabric will tent. The body works the same way: a few key bony points poke through the skin and tell you where the surface changes direction, and the big muscle shapes underneath push the skin into recognizable hills and valleys.
**Use in output:** Rather than memorizing every muscle, focus on the handful of bony bumps that poke through the skin at the shoulders, hips, and joints — those are your fixed markers. Once those points are in the right place, you can draw the skin and muscle between them with confidence — the surface will fill in naturally between the fixed points.

---

### ASIS (anterior superior iliac spine)
**Plain name:** The two bony hip points — the bumps you can feel at the front of your hips on each side
**Plain definition:** The two bony bumps you can feel at the front of your own hip area, one on each side, which act as reliable markers for where the pelvis is tilted when drawing a figure.
**Example:** Put your hands on your hips with your thumbs pointing forward. Your thumbs are resting roughly on these two bony bumps. If one thumb is higher than the other, your hips are tilted. Now imagine drawing someone standing with their weight on one foot: one of those bumps rises and the other drops. If you draw both bumps at the same height, the figure will look like it is standing rigidly at attention no matter how casual the pose is supposed to be.
**Use in output:** Find the two bony hip points at the front of the pelvis — you can feel them on yourself by resting your thumbs on your hips. Plotting those two dots early and checking whether they're level or tilted will lock in the whole hip angle before you draw any more of the lower body.

---

### Greater trochanter
**Plain name:** The outer leg bump — the hard knob on the outside of each upper leg where the leg joins the hip
**Plain definition:** The large bony lump on the outer side of each upper leg, at roughly the widest point of the hip area, which marks where the leg bone meets the hip socket and controls how wide the hips look in a drawing.
**Example:** Stand sideways next to a wall and press the outside of your upper thigh against it. The first hard bump that touches the wall, about a hand's width below your belt line on the outer side, is this point. When a figure has the weight shifted onto one leg, this bump on the weight-bearing side pushes noticeably outward while the other side drops. If you miss this point and draw the outer hip as a smooth straight line, the figure's hips will look unnaturally narrow and the legs will appear to attach to the body in the wrong place.
**Use in output:** Mark the outer hip bump on each side — it sits roughly a hand's-width below the belt, on the very outside of each upper leg. Getting those two points correct sets the true width of the hips and tells you exactly where each leg attaches.

---

### Clavicle
**Plain name:** The collarbone — the two ridges running from the base of your throat out toward each shoulder
**Plain definition:** The pair of horizontal bones that run from the base of the throat outward to each shoulder, forming a visible ridge across the top of the chest that tilts whenever the shoulders move.
**Example:** Look at any person wearing a slightly low-cut shirt. You can often see a thin horizontal ridge on each side running from the center of the neck toward the shoulder. When someone shrugs one shoulder up, that ridge on that side tilts upward. It works like a seesaw mounted at the throat: one end goes up, the other stays put. If you draw both collarbones as a flat horizontal line in a pose where one shoulder is raised, the whole top of the figure looks frozen even if the rest of the body is moving.
**Use in output:** Sketch a short line on each side from the base of the throat outward toward the shoulder — and tilt those lines to match whatever the shoulders are doing. That simple step immediately makes the top of the figure feel like it is part of the same moving body rather than a separate piece.

---

### Foreshortening
*Note: There are two kinds of squishing. This entry covers limb and body-part squishing. See "The squishing of depth" in the Perspective section for how the same effect applies to distances and receding spaces.*
**Plain name:** The squishing effect — how a limb or object looks shorter when it points straight at you
**Plain definition:** The way an arm, leg, or any object appears shorter and more compressed when it is aimed toward or away from you rather than pointing sideways across your field of view.
**Example:** Hold a cardboard paper-towel tube horizontally in front of you, parallel to the floor. It looks long. Now slowly tilt one end toward your face while keeping the other end the same distance away. The tube appears to shrink — not because it got shorter, but because you are now seeing it end-on. A finger pointing straight at a camera looks almost like a circle with a tip; the same finger held sideways looks like a full-length finger. When drawing a figure throwing a punch straight at the viewer, the punching arm looks stumpy and almost round rather than long and slender — and that is correct.
**Use in output:** When a limb is aimed toward you, it will look much shorter than you expect — almost like a squashed version of itself. Trust what you actually see rather than what you know the arm "should" look like when held sideways. Draw the short, compressed shape you observe; the underlying structure will keep it reading correctly as an arm.

---

### C-curve / S-curve
**Plain name:** C-shape and S-shape in the body — the natural bends that keep a figure from looking stiff
**Plain definition:** The simple letter-shaped curves — one smooth arc like a C, or a double reverse curve like an S — that describe how the spine and body flow through most natural poses.
**Example:** Look at a garden hose lying on the ground after someone used it. It rarely lies in a straight line; it settles into a loose S or C shape. A person standing relaxed does the same thing: the spine gently curves, the hips push to one side, and the shoulders tip the other way, creating that S. If you draw the spine as a perfectly straight vertical pole, the figure looks like a toy soldier even if the arms and legs are in a natural position.
**Use in output:** Look at the overall curve running through the spine and body. Does it bend one way, like a C? Or does it reverse partway, like an S? Identify that simple letter-shaped curve early and let everything else follow it — it is what separates a relaxed, living figure from a stiff, locked-up one.

---

### Bean shape (torso)
**Plain name:** The bean method — drawing the torso as one rounded bean before adding details
**Plain definition:** A shortcut for drawing the upper body as a single rounded, slightly pinched oval — like a kidney bean — to establish the overall tilt and twist of the chest and belly before any muscles or clothing are added.
**Example:** Take a dry kidney bean and set it on the table at various angles — flat, tilted left, twisted so the narrow waist faces you. Even without arms, legs, or a head, you immediately read an orientation: where the top is, where the bottom is, how far it is twisted. The human torso, from collar to hip, behaves almost identically as a starting shape. Trying to draw muscles before you have placed that bean is like trying to decorate a cake before you have baked it — you have no shape to put the decoration on.
**Use in output:** Before drawing the chest or belly muscles, sketch the whole torso as a single rounded bean shape — widest at the top, narrowing slightly at the waist, a bit wider again at the hip. Tilt and twist the bean to match the pose. Everything else gets added on top of that first shape.

---

### Rhythm (figure)
**Plain name:** The visual flow — how the eye travels smoothly from one body part to the next
**Plain definition:** The way curves and directions in a figure link together so the eye glides continuously through the drawing rather than stopping and jumping from part to part.
**Example:** Watch a flag ripple in a steady breeze. The wave does not stop at arbitrary points — one ripple flows into the next in a continuous rolling motion. A well-drawn figure works the same way: the curve of the hip connects to the curve of the outer thigh, which connects to the curve of the knee, which connects to the calf. Each section picks up the direction the previous one ended with, creating a chain. If one section suddenly goes in a completely unrelated direction, the eye trips and the figure looks assembled from spare parts.
**Use in output:** After sketching the basic body parts, step back and trace the path the eye takes from the shoulder down the arm, or from the hip down the leg. Does each curve flow into the next without a jarring change in direction? If the path feels bumpy or interrupted, look for where one curve stops and a mismatched one starts — smoothing that transition point is what makes the figure feel like one continuous, living body rather than parts joined together.

---

### Landmark bones
**Plain name:** Surface markers — the bony bumps that show through the skin and tell you where you are on the body
**Plain definition:** The specific points on the body where bones sit close enough to the surface that they create visible or touchable bumps, providing reliable fixed reference points for drawing a figure in any pose.
**Example:** Look at your own elbow — there is a hard knobby point right at the tip. That point is there in every position your arm takes, whether bent or straight. When drawing an arm, that knob tells you exactly where the elbow is regardless of how the arm is twisted. The same applies to the bony ridge of the shin, the kneecap, the bump at the back of the ankle, and the knuckles. These fixed points are like rivets on a canvas — once you place them correctly, the flesh between them can be filled in with confidence.
**Use in output:** Look for the hard, bony bumps at the joints — the knobby tip of the elbow, the kneecap, the outside of the ankle. Place those first, before drawing the softer flesh around them. They are fixed points that do not shift with the muscle underneath, so getting them right first prevents the arm or leg from bending in the wrong place later.

---

### Action pose
**Plain name:** A pose that shows movement or effort — the body clearly doing something
**Plain definition:** A pose in which the body's position communicates physical activity, exertion, or movement so clearly that the viewer understands what the person is doing even with no background or context.
**Example:** Compare two photos of the same person: one sitting in a chair reading, one mid-jump with arms thrown upward. The jumping photo communicates "leaping" the instant you see it, with no caption needed. Everything in the body — the bent knees, the raised arms, the tipped torso — works together to say the same thing. An action pose is any position that delivers that instant, single-word readability of "what the body is doing."
**Use in output:** For this pose to read as [describe the action], every part of the body needs to point toward the same story. Right now, look at whether the tilt of the torso, the direction of the arms, and the placement of the feet all agree with each other. If any one of them contradicts the others, the action will look ambiguous.

---

### Dynamic pose
**Plain name:** An energetic pose — one that feels like it is mid-motion or full of tension
**Plain definition:** A pose in which the body appears to be in the middle of moving or about to move, creating a sense of energy or tension rather than stillness.
**Example:** Think of a coiled spring versus a loose spring lying flat on a table. The coiled spring looks like it is storing energy and could release at any moment. A dynamic pose does the same thing with a body: the torso twists one way while the hips twist another, the weight is shifting, and nothing is symmetrical. The viewer's eye expects the figure to move in the next instant. A spring lying flat gives no such expectation.
**Use in output:** To push this pose toward feeling more energetic, try increasing the difference between where the shoulders are pointing and where the hips are pointing. The more those two tilt in opposite directions — like wringing a towel — the more the figure will read as mid-motion rather than at rest.

---

### Static pose
**Plain name:** A still pose — one that looks planted, stable, and at rest
**Plain definition:** A pose in which the body is symmetrical or evenly balanced so the figure reads as standing still, standing at attention, or at complete rest, with no sense of motion.
**Example:** Compare a person standing with both feet shoulder-width apart, arms at their sides, facing straight ahead — like a soldier at attention — versus someone mid-stride with one arm swinging. The first figure looks planted and still; you would describe the photo in one word: "standing." That planted, at-rest quality is a static pose. It communicates stability and calm but can also read as stiff or lifeless if stillness is not the intended message.
**Use in output:** This pose currently reads as quite still and stable. That is perfect if you want a calm, grounded feeling — but if you were hoping for energy or motion, try shifting the weight onto one foot and letting the hips tilt slightly. Even a small shift breaks the symmetry and wakes the figure up.

---

### Mannequin method
**Plain name:** The wooden puppet approach — drawing the body as jointed blocks before adding flesh
**Plain definition:** A way of building a figure by first sketching the body as simple jointed shapes — boxes for the torso and pelvis, cylinders for the limbs — before adding any muscle, clothing, or surface detail.
**Example:** Think of a wooden artist's mannequin — the kind sold at art supply stores with ball joints and rectangular blocks for the torso. It has no muscles, no skin, no face. But you can tilt it, twist it, and immediately see how the torso and hips relate to each other and how the limbs attach. Drawing the figure as that kind of jointed block structure first means you solve the big questions — where is the weight, how are the hips oriented, how does the torso twist — before you spend time on details that will all have to change if the big structure is wrong.
**Use in output:** Try building this figure in two steps. First, sketch the body as simple jointed blocks — a brick for the chest, a brick for the pelvis, simple tubes for the arms and legs — and get the overall pose working. Then add the surface detail over those blocks. Doing it in that order means fixing a proportion problem never costs you the time you already spent on the muscles.

---

### Bean-and-limbs method
**Plain name:** The bean shortcut — one round shape for the torso, simple tubes for the limbs
**Plain definition:** A quick approach to sketching a figure by drawing the torso as a single rounded bean shape and the limbs as simple tapered tubes, capturing the whole body's pose in seconds before committing to any detail.
**Example:** Look at how a child draws a stick figure: a circle for the head, a rectangle for the body, lines for arms and legs. The bean-and-limbs approach is one step above that: instead of a rectangle, you use a kidney-bean shape that can twist and tilt, and instead of single lines you use slightly tapered sausage shapes. You can sketch a rough full-body pose in about thirty seconds. The point is not for this sketch to look finished — it is to quickly test whether the pose works before spending time on anything else.
**Use in output:** Before committing to this pose, try roughing it out in about thirty seconds as a bean-and-limbs sketch: one rounded bean for the torso, simple tapered tubes for each limb. If the rough version reads the way you want, you have your foundation. If it does not, you have saved yourself the time of working out the problem at the detail level.

---

### Exaggeration (gesture)
**Plain name:** Pushing the pose further — deliberately making the curves and tilts bigger than real life
**Plain definition:** The deliberate act of making a pose's tilt, stretch, lean, or twist bigger than a photograph would show, so the figure communicates its action more loudly and immediately.
**Example:** Watch a slow-motion video of a sprinter leaving the starting blocks. In real life, the body is dramatically tilted forward — maybe 45 degrees. But in a photograph the tilt often reads as much less extreme because the camera flattens depth. Illustrators who draw sprinters often tilt the figure to 60 degrees or beyond, because that is what it takes to give the flat drawing the same visual punch the real thing has in three dimensions. Exaggeration is not inaccuracy — it is the adjustment that makes a flat image feel as intense as the real event.
**Use in output:** This pose is reading as a little flat or hesitant. Try pushing the main tilt or stretch about 20-30% further than it is now — more lean on the torso, more reach in the arm, more bend in the knee. Exaggerating slightly beyond what a photo would show is often what it takes to make the pose read clearly in a flat drawing.

---

### Weight and balance
**Plain name:** Where the body's weight is going — and whether the figure looks stable or about to fall
**Plain definition:** The distribution of a figure's body mass over its feet (or other support points), which tells the viewer whether the person looks grounded and stable or caught in the act of falling.
**Example:** Stand on one foot and lean slowly to the side. At a certain point you have to put your foot down or hop, because your weight has moved outside the area your one foot covers. A figure drawn with all the body mass shifted far to one side, but with both feet planted together under the other side, will look like it should be falling over — the viewer's body knows this instinctively and the drawing feels wrong without knowing why. Getting the weight and the foot position to agree is what makes a figure look like it belongs on the ground.
**Use in output:** Check where the weight is sitting in this pose. Find the foot (or both feet) that are touching the ground, and mentally drop a straight line down from the center of the torso. Does that line land between the feet, or outside them? If it lands outside the feet and the pose is meant to be balanced, shift the torso or the feet until the line lands safely between them.

---

### Centre of gravity
**Plain name:** The balance point — the spot in the body that needs to be over the feet for the figure to look stable
**Plain definition:** The invisible point roughly in the middle of the body's weight where, if the body were balanced on a pin, it would sit level — and which needs to be directly above the support (feet, seat, etc.) for the figure to look stable.
**Example:** Balance a broom handle upright on your open palm. The handle stays up only while your palm is directly below the point where all the stick's weight collects. The moment your hand shifts to one side, the handle falls. A drawn figure obeys the same rule: if the point where all the body's weight collects is hanging over empty air rather than over a foot, the figure looks like it is about to tip over — even if you cannot name the rule, your eye reads it instantly.
**Use in output:** To check whether this pose looks stable, mentally find the midpoint of the torso and drop a straight vertical line from it to the floor. Does that line land on or between the feet? If the pose is meant to be a steady standing position, it should. If the line misses the feet, either bring the torso more toward center or shift a foot outward to catch it.

---

### Proportions (figure)
**Plain name:** The size relationships between body parts — how tall the head is compared to the whole body, etc.
**Plain definition:** The set of size relationships between different parts of the body — how many head-heights tall the full figure is, how long the arms are compared to the torso — used as a starting reference to keep the figure consistent.
**Example:** Hold a pencil at arm's length next to a person standing across the room and use your thumb to measure how tall their head appears against the pencil. Then, without moving, see how many of those head-lengths stack up to cover their full height. Most adults measure roughly seven to eight head-lengths tall. This simple counting method gives you a portable ruler made from the figure itself. If you draw the head very large and the body proportionally shorter than seven heads, the figure will read as child-like; very small head with a tall body reads as heroic or exaggerated.
**Use in output:** Use the head as your measuring unit — it is the most convenient ruler already in your drawing. Once the head is placed, check that the total height of the figure is roughly seven or eight times that head height. If the body is coming out shorter or taller than that, the proportion will read as deliberately stylized rather than naturalistic, which may or may not be what you want.

---

### Joint range of motion
**Plain name:** How far a joint bends — the natural limits of elbows, knees, and wrists that stop a pose from looking physically impossible
**Plain definition:** The maximum angles a specific joint can actually reach in a living body — knowing these limits prevents you from drawing poses where arms bend the wrong way or knees flex past their natural stop point.
**Example:** Hold your arm straight out in front of you and try to bend your elbow backward — away from you. It will not move. Now bend it forward — toward you — and it stops at roughly a 145-degree bend before muscle and bone prevent it going further. That hard stop is the joint's range of motion. Every joint in the body has a specific direction it bends and a maximum angle it reaches; drawing a knee that bends forward instead of backward, or an elbow that hyperextends dramatically, will immediately read as broken or impossible to anyone looking at it.
**Use in output:** Check the bent joints in this pose — the [elbow / knee / wrist / shoulder]. Does each one bend in the correct direction for that joint type? Elbows hinge forward (toward the shoulder), knees hinge backward (toward the hip), wrists can flex and extend but only within a moderate range. If a joint looks like it is bending in a direction that would require breaking the bone, straighten it out and find a different angle that reads the same pose.

---

### Muscle groups as form blobs
**Plain name:** Muscle lumps — thinking of each muscle as a simple rounded blob that changes shape when the limb moves
**Plain definition:** An approach to drawing muscles by treating each major muscle as a simple rounded lump — not a flat outline — that changes its shape and bulge when the joint it controls moves.
**Example:** Squeeze your own upper arm with your opposite hand. When your arm is relaxed and straight, the bicep feels like a soft rounded lump lying flat along the bone. Now bend your elbow — the same lump shortens, bunches up, and becomes harder and rounder under your fingers. It did not become a different muscle; the same lump just changed its shape because the joint moved. Drawing muscles as rounded lumps that bulge and compress with movement — rather than as outlines traced from a diagram — is what makes a painted arm look like it is made of real tissue rather than flat pattern.
**Use in output:** Instead of drawing the outline of each muscle separately, try thinking of the [bicep / calf / shoulder / thigh] as a single rounded lump sitting on top of the bone. Where is that lump pointing? Is the joint bent (the lump bunches up and shortens) or straight (the lump flattens and elongates)? Getting the lump's direction and degree of bulge right will make the muscle read as three-dimensional even before you add any shading.

---

### Torso-pelvis relationship
**Plain name:** Chest-and-hips block — treating the upper and lower torso as two connected boxes that tilt and twist independently
**Plain definition:** The practice of drawing the chest and the pelvis as two separate box-like volumes connected at the waist, which can tilt and twist in different directions relative to each other, before adding any detail to the body.
**Example:** Take two cardboard boxes of different sizes and connect them loosely with a short length of rope — a large box for the chest and a smaller box for the pelvis. Now tilt one box left while the other stays level. Now twist one clockwise while the other stays facing forward. The rope between them allows each box to move independently within limits. The human torso works exactly this way: the chest and the pelvis are two rigid structures connected at the flexible waist. Every natural standing pose involves some tilt or twist between those two boxes, even if it is subtle. Drawing them as the same flat rectangle produces a stiff, unnatural figure.
**Use in output:** Before drawing any muscles or clothing, sketch the chest and the pelvis as two separate tilted boxes. Is the chest tipping left while the hips tip right? Is the chest twisted slightly toward the viewer while the hips are turned away? Once those two boxes are in the right relationship to each other, attach the limbs to them — the arms to the chest box, the legs to the pelvis box. That two-box structure is what gives the torso its natural, living quality.

---

### Proportional canon
**Plain name:** Body proportion guide — a standard set of size ratios used as a starting reference before adjusting for the specific character
**Plain definition:** A standardised set of size relationships for the human figure — such as "a standing adult is about seven to eight head-heights tall" — that serves as a reliable starting point which you then adjust for your specific character's age, build, and style.
**Example:** A tailor's size chart lists standard measurements for a "medium" shirt: collar width, sleeve length, chest circumference. No real person is exactly a medium in every measurement, but the chart gives a reliable starting point so the tailor is not guessing from nothing. A proportional canon works the same way for drawing the human figure: start from the known ratios (roughly seven heads tall, the waist at three heads from the top, the fingertips reaching mid-thigh) and then adjust for the specific person. A heroic or fantasy figure might be stretched to eight or nine heads tall; a child might be only four heads tall. The canon is the baseline, not the rule.
**Use in output:** Use the standard proportions as a starting checklist for this figure: place the head, then mark where seven or eight head-heights down lands (that is the floor), then check that the waist, hips, knees, and ankles fall at roughly the expected positions. If something feels off, measure it against the head unit — usually the error is that one section is too long or too short by half a head-height, which is easy to fix at this stage and very hard to fix after the detail is in.

---

## Form and Construction

---

### Primary forms (box / cylinder / sphere / cone)
**Plain name:** The four starter shapes — the building blocks everything gets made from first
**Plain definition:** The four simple three-dimensional shapes — a box, a tube, a ball, and a pointed cone — used as the first rough stand-ins for any complex object before details are added.
**Example:** Walk through a hardware store and look at the objects on the shelves: a bucket is a cylinder with a narrower bottom (a truncated cone); a paint can is a short cylinder; a brick is a box; a ball valve is a sphere with tubes attached. Everything in the store, and everything in a painting, can be roughed in with some combination of those four shapes. Starting with them means you can solve where things sit in space and how light falls on them before worrying about the label on the paint can.
**Use in output:** Before adding any detail to this object, try roughing it in as a combination of simple shapes — a box here, a tube there, a sphere for that rounded part. Get the sizes and angles of those rough shapes right first. Once they are correct, the details you add on top will automatically sit in the right place.

---

### Planar analysis
**Plain name:** Flat-face thinking — reading any curved surface as a set of flat faces like a cut gemstone
**Plain definition:** The practice of mentally dividing any rounded surface into a small number of flat sections — front face, side face, top face — so you can work out how light falls on each section before blending them into a smooth curve.
**Example:** Think of a cardboard box sitting in sunlight. The top face is bright. The front face is medium. The side face is dark. Even though a nose or an arm is curved, your brain reads it the same way — bright side, medium side, dark side. When painting anything rounded, start by asking: which "face of the box" is this part of the nose or arm? Lock in those three light levels first, then soften the edges between them into a smooth curve. If you try to blend before you have set those three levels, everything smears into an undifferentiated grey.
**Use in output:** Before blending this rounded surface, try treating it as if it had three or four flat sections — a bright top face, a medium front face, a dark side. Set the light level of each flat section first, then soften the edges between them. Going straight to blending without that step is what causes rounded objects to lose their three-dimensional quality and look flat.

---

### Cross-contour lines
**Plain name:** Wrap-around lines — lines that circle around the surface of a shape like latitude lines on a globe
**Plain definition:** Lines drawn across the surface of a shape that follow the surface as it curves away from the viewer, like the lines on a contour map or the horizontal rings around a ball, which show whether the surface is curving toward you or away.
**Example:** Look at a peeled orange. The segments run from top to bottom over the surface, curving over the rounded front and disappearing around the back. Those segment lines tell you exactly where the surface is curving and how steeply. Now draw a circle on paper and add a set of horizontal lines across it that curve upward in the middle (like a globe's latitude lines). The circle suddenly looks like a ball instead of a flat disk. The lines did that — they communicated "this surface curves away from you on both sides."
**Use in output:** To make this rounded surface read as three-dimensional rather than flat, try adding a few wrap-around lines — imagine drawing the latitude lines of a globe across the surface. Even if you erase them afterward, the act of drawing them will show you whether your surface is curving in the right direction, and it will train your eye to see the curve instead of the flat silhouette.

---

### Surface planes
**Plain name:** The faces of a shape — each individual flat section that a surface is made of
**Plain definition:** Each distinct flat section that makes up a surface, like the individual faces of a cut diamond or the sides of a building — understanding which way each section faces tells you how bright or dark it will be.
**Example:** Hold a die (the kind from a board game) up to a window. The face pointing toward the window is the brightest. The face pointing away is the darkest. The faces on the sides are somewhere in between, depending on their angle. That one die has six surface planes, and the light treats every single one differently depending on the angle it faces. A human nose has roughly the same behavior: a face pointing up toward the light source, a face pointing toward the viewer, a face pointing down into shadow. Each face gets its own light level.
**Use in output:** Pick one area of this object and ask: how many separate flat faces does it have, and which direction does each one point — toward the light, away from it, or sideways? Give each face its own light level before blending them. That step is what separates a convincingly solid object from one that reads as flat.

---

### Form shadow vs cast shadow (in construction context)
**Plain name:** Own shadow vs thrown shadow — the dark side of the object itself vs the shadow it throws onto something else
**Plain definition:** The difference between the shadow that lives on the object's own surface (on the side turning away from the light) and the shadow the object throws across an adjacent surface like a table or the ground.
**Example:** Put a coffee mug on a table next to a lamp. The dark area on the side of the mug that faces away from the lamp is the mug's own shadow — it lives on the mug itself and follows the mug's rounded surface. The dark patch on the table below and beside the mug was put there by the mug blocking the light — that is the thrown shadow, and its shape is determined by the mug's silhouette and the direction the light is coming from, not by the mug's surface curves. The two shadows behave completely differently and should never be drawn the same way.
**Use in output:** Look at the shadowed areas in your drawing and separate them into two groups: shadow that is on the object itself (the dark side of a rounded surface turning away from the light) and shadow that the object is projecting onto the surface it sits on or against. Treat those two groups separately — they have different edges, different darkness levels, and different shapes.

---

### Simplified forms
**Plain name:** The rough block-in — reducing a complex object to its simplest possible version first
**Plain definition:** The process of drawing a very rough, stripped-down version of a complex object using only the largest, simplest shapes before adding any secondary shapes or surface details.
**Example:** If you wanted to sculpt a realistic face in clay, you would not start by sculpting the nostril. You would start by making a rough egg shape the right size, then adding a rough nose bump, then refining the bump into a nose shape, and only then worrying about the nostril. Working the other way — starting at the nostril level — means you have no context for whether the nostril is the right size or in the right place. A simplified form is that first rough egg: get the big shape right before you go smaller.
**Use in output:** Step back from the detail level and look at the largest, simplest shape this object is. Can you see it as one big rounded box, or one elongated cylinder? Sketch that one big shape in the correct position and at the correct angle first. Everything else you add will be a subdivision of that first shape, which keeps proportions consistent all the way through.

---

### Organic vs geometric forms
**Plain name:** Natural shapes vs built shapes — the difference between a rock and a brick
**Plain definition:** The distinction between irregular, flowing shapes found in nature (a body, a tree, a cloud) and the precise, angular shapes created by construction or manufacture (a building, a table, a gear).
**Example:** Pick up a potato and a cardboard box. The potato has no two sides the same — it bulges, dips, and curves unpredictably. The box has flat faces that meet at sharp, consistent right angles. Both are solid three-dimensional objects and both respond to light, but the potato requires you to observe and record each individual curve, while the box can be fully described by a set of measurements and angles. When drawing, knowing which category an object falls into tells you whether to look for consistent flat faces and sharp corners (geometric) or variable flowing curves (organic).
**Use in output:** This object sits somewhere between a geometric shape (precise, angular, built) and an organic shape (irregular, flowing, natural). Which is it closer to? If it is more geometric, try constructing it from flat-faced blocks and let the sharp edges be sharp. If it is more organic, let the surfaces flow and avoid the urge to make everything symmetrical or perfectly even.

---

### Volume
**Plain name:** The sense of solid three-dimensional space an object takes up — the "filled-in" feeling
**Plain definition:** The quality of a drawn shape that makes it look like a solid, filled-in three-dimensional object rather than a flat outline, as if you could pick it up and hold it in your hand.
**Example:** Draw a circle on paper. It looks flat — like a coin or a sticker. Now draw a sphere: the same circle, but with shading that gets darker on one side and a highlight on the other, and a few curved lines across it. Suddenly the same circle looks like a ball you could pick up. Nothing physically changed about the paper — but the shading and the curved lines communicate that the surface wraps around a solid, space-filling ball rather than lying flat. That pickable-up quality is volume.
**Use in output:** This shape is currently reading as flat rather than solid. The quickest fix is to add a dark side and a bright side — pick one direction for the light, make the side facing it noticeably lighter, and make the opposite side noticeably darker. That simple contrast between two sides is what communicates that the shape takes up real space.

---

### Mass
**Plain name:** The weight and density a shape appears to have — how heavy or solid it looks
**Plain definition:** The visual quality that makes an object in a drawing look as if it has actual weight and substance, like a boulder rather than a balloon, created through the way shadows, edges, and proportions are handled.
**Example:** Compare a photograph of a boulder to a photograph of a crumpled piece of paper. Both might take up the same amount of space in the photo, but the boulder looks heavy and dense — you would not want it to fall on your foot. The paper looks light and hollow. The boulder looks that way because of how its shadow is deep and consistent, its edges firm, and its surface shows no thinness. You can communicate the same quality difference in a drawing by making shadows on heavy objects solid and deep, and by keeping the object's silhouette firm rather than wispy.
**Use in output:** To make this object feel heavier and more solid, deepen the shadows on its underside and against any surfaces it sits near. Heavy, dense things press against their surroundings and create deep, dark contact shadows. Lightening or softening those contact areas will make it float; darkening them will make it feel planted and heavy.

---

### 3D construction method
**Plain name:** Building in depth — starting with a three-dimensional skeleton of simple shapes before adding surface
**Plain definition:** The overall approach of building a drawing by first establishing the three-dimensional structure of an object with simple solid shapes, then refining and detailing on top of that structure.
**Example:** Think about how a house is built. The crew does not start by installing door handles. They pour a foundation, frame the walls and roof in lumber, and then add siding, windows, and finally hardware. The framing stage is where all the important structural decisions are made — room sizes, wall angles, roof pitch. If the framing is wrong, no amount of nice door handles will fix it. Drawing a complex object works identically: the structural skeleton of simple three-dimensional shapes is the framing. Get that right first.
**Use in output:** Think of this as a two-phase drawing. Phase one: build the skeleton using simple three-dimensional shapes — boxes, tubes, balls — in the right position, at the right angle, with the right size relationships. Phase two: refine the surface of that skeleton into the final shape. Working in that order means you can catch and fix structural problems while they are still cheap to fix.

---

### Ribbon method
**Plain name:** Drawing limbs as flat twisting ribbons instead of tubes — a way to show how the surface turns
**Plain definition:** A technique for drawing arms, legs, and other elongated body parts as if they were made of flat ribbon that twists along its length, rather than simple tubes, so that the direction the surface faces is always visible.
**Example:** Take a strip of paper and hold both ends. Now slowly twist one end while keeping the other still. The paper strip shows you a flat top surface, then the edge, then the flat bottom surface — it communicates the twist. Drawing an arm as a twisted ribbon like this tells you and the viewer exactly where the arm's surface is facing at every point along its length: toward the viewer, away from the viewer, or sideways. A plain tube does not communicate that information — it looks the same from every angle.
**Use in output:** Try drawing this arm (or leg) as a flat strip of paper that twists from the shoulder to the wrist. At the top, which face of the strip is pointing toward the viewer? At the wrist, has the strip twisted so a different face is toward the viewer? Sketching it this way will clarify exactly where the surface turns, which in turn tells you exactly where to put the light and dark areas.

---

### Contour (silhouette vs internal)
**Plain name:** The outline vs the surface lines — the edge of the shape vs lines that describe the surface inside the edge
**Plain definition:** The difference between the outer edge of a drawn shape (the outline where the object ends and the background begins) and any lines drawn on the interior of the shape that describe its surface bumps, ridges, or curves.
**Example:** Trace around the outside of your hand on paper. That traced line is the outline — it tells you the hand's silhouette. Now draw the lines for the knuckle ridges, the crease at the palm, and the thumb joint inside that silhouette. Those interior lines are surface lines. Both kinds of line are important, but they do different jobs: the outline tells you the shape; the interior lines tell you the surface. A drawing made only from an outline will look like a flat cutout; adding interior lines is what communicates that the hand is rounded and three-dimensional.
**Use in output:** Look at whether the lines in this area are describing the outer edge of the shape or the surface inside it. The outer edge tells the viewer what shape the object is; the interior lines tell the viewer how the surface curves. If this area looks flat, try adding a few interior lines that wrap around the surface — even a single curved line across a rounded object can turn a flat shape into something that reads as solid.

---

### Relative measurement
**Plain name:** Comparing sizes within the drawing — using one part to measure another
**Plain definition:** The practice of using a length already established in your drawing as a measuring stick to check the size of another part, rather than measuring against an external ruler or guessing.
**Example:** If you have already drawn a head that looks the right size, you can use that head as a portable ruler. Hold a pencil at arm's length, use your thumb to mark the height of the head on the pencil, then swing the pencil down to see how many of those head-heights fit in the torso. If you drew the torso as three head-heights long when it should be about two and a half, you will see the discrepancy immediately — and you found it by measuring against your own drawing, no external ruler needed.
**Use in output:** To check whether the proportions are holding together, pick one part of the drawing — often the head — and use it as your measuring unit. Use a pencil held at arm's length or a quick tick-mark on a scrap of paper to see how many times that unit fits into the part you are checking. This keeps all your measurements relative to each other rather than to an outside scale.

---

### Envelope / silhouette first
**Plain name:** The outer box first — drawing the overall bounding shape before the internal details
**Plain definition:** The practice of lightly sketching the outermost boundary of the whole object — as if drawing the box it came packaged in — before drawing anything inside that boundary.
**Example:** Think of how a jigsaw puzzle looks when all the pieces are still loose in the box. Before you find any internal pieces, experienced puzzlers find all the flat-edged border pieces and build the outer frame first. The outer frame tells you the total size and shape; then you fill in the middle. Drawing the outer silhouette first does the same thing: it tells you the total space the object occupies before you commit to any internal line.
**Use in output:** Before drawing any internal detail, lightly sketch the outermost outline of the whole object — imagine the box it would come shipped in, or the shape its shadow would cast straight down onto the floor. Get that outer boundary in the right position and at the right size. Then fill in the interior.

---

### Construction drawing
**Plain name:** Structure map — the drawing that records how all your objects are built in space
**Plain definition:** A finished structural skeleton drawing — made of simple geometric shapes in correct perspective — that records the three-dimensional layout of your objects and is kept as a reference so later painting stages stay consistent with it.
**Example:** A builder frames a house in lumber before hanging any drywall or fitting any doors. The lumber frame is a full-scale skeleton of the finished building, showing exactly where every wall, window opening, and roof pitch will be. Once the frame is approved, everyone on the site works from it — the electrician, the plumber, the plasterer. None of them redesign the rooms while they work. A construction drawing is the equivalent for a painting: the structural skeleton in correct perspective that all later stages refer back to. If the painting drifts away from the skeleton — if a shading pass accidentally makes a wall look further away than the construction placed it — the drawing is there to catch the error.
**Use in output:** Keep your construction drawing visible on a separate layer or as a pinned reference while you shade and colour. If at any point the lighting or perspective in a later pass starts to feel wrong, compare it back to the construction skeleton — the error is almost always a painted surface that has drifted away from where the structural drawing placed it.

---

### Planar orientation
**Plain name:** Which way each face points — figuring out whether a surface faces toward the viewer, away, or sideways
**Plain definition:** The specific direction a surface plane is pointing — toward the light, away from it, or at an angle — which determines how bright or dark that surface will be before any shading is applied.
**Example:** Hold a flat book cover in front of you with both hands. Tilt the top away from you: the cover now faces the ceiling and is brightly lit from above. Tilt it so the cover faces you directly: it is fully visible, mid-brightness. Tilt it so the cover faces the floor: it is in shadow. The book cover did not change; only the direction it points changed. Planar orientation is just the formal name for that direction. Before shading any surface in a painting, you need to know which way it is pointing — toward the light, away from it, or sideways — because that answer determines the brightness before you even pick up a brush.
**Use in output:** Before shading this [face / wall / plane], ask: which direction is it pointing? Is it pointing toward your light source (bright), away from it (dark), or at roughly 90 degrees to it (medium)? Settle that question for each distinct surface before mixing any paint. Shading without knowing the planar orientation first is what causes forms to look randomly lit rather than consistently lit from one direction.

---

### Contour-chasing
**Plain name:** Outline-only drawing — the trap of drawing only the outer edge of shapes without thinking about the solid object inside
**Plain definition:** A common drawing error where instead of building a three-dimensional solid shape, the artist traces only the visible edges and outlines, producing a flat form that falls apart when shaded or viewed from a different angle.
**Example:** Imagine tracing around a photograph of an arm by following its outer edge with a pen — you get a flat, bean-shaped outline. That outline looks like an arm from exactly that angle, but it gives you no information about whether the arm is a cylinder, a ribbon, or a flat board. Now try to shade that flat outline — you have no idea where the light and dark areas go because you never decided what three-dimensional solid is inside the outline. Contour-chasing produces drawings that look like outlines of things rather than things themselves: they flatten under shading and lose their shape when the pose changes, because there was never a solid inside.
**Use in output:** The outline of your [arm / torso / object] is correct, but the surface inside it looks flat — there is no sense of the solid shape underneath. This usually means the object was drawn by following its edge rather than by building a cylinder or box first. Try starting over on a new layer: rough in a simple cylinder or box at the correct angle, then draw the surface detail over that solid. The shading will fall into place naturally once the solid is there to shade.

---

## Perspective

---

### One-point perspective
**Plain name:** Single-point depth — when all the depth lines in a scene aim at one single dot on the horizon
**Plain definition:** A way of drawing depth where all lines that run away from the viewer converge to one single dot on the horizon line, used when the viewer is looking straight at the front face of objects in the scene.
**Example:** Stand in the middle of a long, straight hallway and look straight ahead. The ceiling meets the wall in a line that appears to slope downward toward the far end. The floor meets the wall in a line that slopes upward toward the far end. Both lines aim at the exact same dot at the end of the hallway. The walls, floor, and ceiling all meet at that one dot. If you drew this hallway, every line traveling away from you would point at that single dot — that is all one-point perspective is.
**Use in output:** In this scene, you are looking fairly straight at the front of the objects. That means all the lines going away from you — the top and bottom of walls, the floor edges, the ceiling — should converge toward a single dot on the eye-level line. Try placing that dot first, then use it as the target for all lines going into the distance.

---

### Two-point perspective
**Plain name:** Two-dot depth — when you see a corner of an object and depth lines aim at two separate dots
**Plain definition:** A way of drawing depth where edges going to the left converge to one dot on the horizon and edges going to the right converge to a different dot on the horizon, used when the viewer sees the corner of an object rather than its flat front face.
**Example:** Stand at a street corner and look at the corner of the building in front of you. The left face of the building has all its horizontal edges running away to the left and downward toward the far left. The right face has all its horizontal edges running away to the right and downward to the far right. Both sets of lines aim at dots far off in opposite directions along the same horizon. Every box-shaped object you see from a corner angle works this way — two separate sets of lines, two separate dots, both on the same horizon.
**Use in output:** You are seeing this object from a corner angle — you can see two faces of it at once. Place two dots on the eye-level line, one far to the left and one far to the right. All the horizontal edges on the left face of the object should aim at the left dot; all the horizontal edges on the right face should aim at the right dot. Vertical edges stay vertical.

---

### Three-point perspective
**Plain name:** Three-dot depth — used for extreme up-or-down views where even the vertical lines converge
**Plain definition:** A way of drawing depth that adds a third convergence dot either far above or far below the horizon, used when the viewer is looking steeply upward or downward so that even the vertical edges of buildings and objects appear to lean inward.
**Example:** Stand at the base of a very tall building and look straight up. The corners of the building, which you know are parallel straight lines, appear to lean toward each other as they rise, eventually appearing to meet at a point directly above you. That point far above your head is the third dot. The same thing happens when you look straight down from a tall window: the corners of the building below you appear to converge toward a point far below. Any time the view is steep enough that vertical lines appear to tilt, a third dot is needed.
**Use in output:** Because this view is looking steeply [upward/downward], even the vertical lines of buildings and objects need to converge. Place a third dot [above the image/below the image] — far enough away that the convergence is subtle rather than extreme — and have the vertical edges of tall objects lean gently toward that dot.

---

### Horizon line
**Plain name:** The eye-level line — the invisible horizontal line that sits exactly at the viewer's eye height
**Plain definition:** The horizontal line across the scene that sits exactly at the viewer's eye level, which is where all the convergence dots for horizontal edges live.
**Example:** Go to a beach and look out at the water. The line where the water meets the sky is exactly at your eye level — that is the actual horizon. Now crouch down: the line drops. Stand on a wall: the line rises. The horizon always sits at your eye height. In a drawing of a room or street, there is no actual sky-meets-water line, but the same invisible horizontal line exists at the viewer's eye height, and all the lines going into the distance still aim at dots sitting on that invisible line.
**Use in output:** Decide how tall the viewer's eye is in this scene — standing height, crouching height, or looking down from a window. Draw a light horizontal guide line across the full width of the canvas at that height. Every convergence dot you place goes on that line, and every horizontal edge going into the distance will aim at a dot on it.

---

### Vanishing point
**Plain name:** The convergence dot — the single point where parallel lines that go into the distance appear to meet
**Plain definition:** The dot on the horizon line where a set of lines that are actually parallel to each other in real life (like the two rails of a train track) appear to meet in a drawing.
**Example:** Stand between two parallel train rails and look down the track. The rails are the same distance apart your entire life — they never actually meet. But to your eyes, they appear to get closer and closer and finally touch at a single point in the far distance. That meeting point on the horizon is the vanishing point. If you drew those rails without having the two lines meet at the same point, one rail would appear to veer in a different direction than the other, which would look wrong even to someone who has never studied drawing.
**Use in output:** For this set of parallel edges — the top and bottom of that wall, the two sides of that road — pick a single dot on the eye-level line and make sure both lines in the pair aim exactly at that same dot. If even one line aims at a slightly different spot, the parallelism breaks and the scene looks structurally incorrect.

---

### Eye level
**Plain name:** The viewer's height — how high off the ground the imaginary camera or viewer is
**Plain definition:** The height at which the viewer's eyes are positioned in the scene, which determines where the horizon line sits and whether objects appear above, below, or right at the viewer's line of sight.
**Example:** Sit down at a dining table and look at a glass of water on the table. You are looking at it at roughly the same height as the glass — you can see the top of the water surface. Now stand up: the glass is below your eye level and you see more of the top. Now kneel on the floor: the glass is above your eye level and you are looking at the bottom of the glass. The glass did not change — your eye level did, and it completely changed what you see. In a drawing, deciding where the eye level is decides all of this at once for every object in the scene.
**Use in output:** Before placing any objects in this scene, decide where the viewer's eyes are: ground level, standing height, or above the scene looking down? Mark that as a horizontal guide line. Objects above that line will show their undersides; objects below it will show their tops. Getting this consistent across all objects is what makes the scene feel like everything inhabits the same space.

---

### Station point
**Plain name:** Camera position — where you are imagining the viewer standing when they look at the scene
**Plain definition:** The spot where you imagine the viewer (or camera) is standing — decide it early, because every perspective line in the scene flows from that one decision.
**Example:** Think of setting up a camera on a tripod to photograph a room. You decide where in the room to place the tripod, how high to set it, and which direction to point it. That tripod location is the station point. Move the tripod closer to the window and everything outside becomes dominant. Move it to the opposite corner and you see more of the room itself. In a drawing, you make the same choice — even without a camera — and every perspective decision flows from that implied position.
**Use in output:** Think of yourself as choosing where to place a camera for this scene. Are you close to the objects or far away? Are you at the center of the space or off to one side? Deciding that position clearly — and sticking to it — is what keeps the perspective consistent. Inconsistencies usually mean the viewer's position has shifted mid-drawing.

---

### Cone of vision
**Plain name:** The safe drawing zone — how wide an angle you can draw before things start looking stretched or bent
**Plain definition:** The zone directly in front of the viewer where objects look natural and undistorted — anything you draw too far toward the edges of an unusually wide scene can start to look stretched or bent.
**Example:** Hold both arms straight out to your sides and look straight ahead. You can dimly sense your fingers at the edge of your vision, but if you were to try to read text held at your fingertips, it would be blurry and distorted. Now bring both hands in to about 30 degrees either side of center — roughly where you would hold a newspaper to read it comfortably. That comfortable reading zone is roughly the cone of vision. Objects drawn within that zone look natural. Objects drawn far outside it — like a building placed at the very edge of the canvas when the canvas covers a very wide angle — will appear stretched or leaning unnaturally.
**Use in output:** The object in the far corner of this scene may be starting to distort because it is sitting outside the comfortable viewing zone. Try either pulling that object closer to the center of the scene, or widening the implied distance between the viewer and the scene so everything fits within a narrower angle. Alternatively, treat the distortion as a deliberate stylistic choice — but be aware that it will read as distortion to the viewer.

---

### Foreshortening (in perspective context)
*Note: There are two kinds of squishing. This entry covers distances and receding spaces. See "The squishing effect" in the Anatomy and Gesture section for how the same effect applies to limbs and body parts.*
**Plain name:** The squishing of depth — how objects or distances shrink the further they go from the viewer
**Plain definition:** The visual compression of any object or distance that extends toward or away from the viewer, making it appear shorter than its true length, which must be drawn as it appears (compressed) rather than as it actually is (full length).
**Example:** Look down a long street with evenly spaced telephone poles. The gap between the first and second pole looks wide. The gap between the tenth and eleventh pole looks tiny — even though all the gaps are the same actual size. The depth is being foreshortened: distances that extend away from you appear compressed. A road that is ten kilometers long and photographed from one end would appear to be only a few centimeters long in the photograph. Drawing it any other way — showing the full ten kilometers — would look completely wrong.
**Use in output:** The depth of this object or space is compressing as it goes away from the viewer. The parts closest to you should appear the largest; the parts furthest away should appear noticeably smaller, even if you know they are the same size in real life. Resist the urge to draw the far end at full size — the compression is correct and expected.

---

### Atmospheric perspective
**Plain name:** Distance fade — how objects get hazier, lighter, and less colorful the further away they are
**Plain definition:** The natural effect where distant objects look faded, lower in contrast, and shifted toward a pale bluish-grey because of the air and particles between the viewer and the object.
**Example:** Look out a window at a mountain range on a hazy day. The nearest hills are dark green and show sharp edges and individual trees. The hills behind them are lighter and greener-grey. The furthest hills are barely visible — pale blue-grey shapes with no visible detail, almost the same tone as the sky. That is not a painting technique; that is just what air does when you look through miles of it. It scatters light, reduces contrast, and shifts colors toward grey-blue. Painting a distant mountain the same dark green and sharp as the foreground tree makes the mountain look like it is sitting right next to you.
**Use in output:** To push this background further away, narrow the gap between its darkest and lightest areas — make the darks a little lighter and the lights a little darker until the whole background sits in a similar medium range. Also shift the background colour slightly toward a cool pale blue-grey. The more you compress that brightness range and shift the colour in the background, the further back it will appear, even if you add no other depth cues.

---

### Measuring lines
**Plain name:** Equal-spacing guides — how to make fence posts, tiles, or windows shrink at the right rate as they go into the distance
**Plain definition:** Construction guide lines that help you figure out where to place evenly spaced objects — like fence posts or floor tiles — so they shrink by the right amount as they get further away from the viewer.
**Example:** Imagine you are painting a tiled floor receding into the distance. The tiles are all the same size in real life, but in the drawing they get smaller as they go back. You cannot just make each tile a little smaller by eye — you will get the shrinking rate wrong and the tiles will look uneven. Measuring lines give you a geometric method to find each tile edge in exactly the correct shrunken position. It is the same process a contractor uses to lay out equally spaced tiles on an actual floor using a chalk line — a systematic method so the result comes out evenly spaced rather than eyeballed.
**Use in output:** To space these repeating elements — fence posts, window frames, floor tiles — evenly as they recede, use a geometric dividing method rather than guessing by eye. Find the center of the receding face by drawing diagonal lines corner to corner; the center is where they cross. That center point lets you find the halfway point in perspective-correct space, and you can keep subdividing to find any spacing you need.

---

### Picture plane
**Plain name:** The canvas window — the imaginary flat glass surface between the viewer and the scene
**Plain definition:** The imaginary flat surface, like a pane of glass, that sits between the viewer's eye and the three-dimensional scene, onto which all the three-dimensional information is projected to create the two-dimensional drawing.
**Example:** Imagine pressing your face against a window and tracing with a grease pencil directly on the glass what you see through it — trees, buildings, street. The glass you are drawing on is the picture plane. Everything on the other side of the glass is the three-dimensional scene; everything you trace on the glass is the two-dimensional drawing. This is not a metaphor — early Renaissance painters literally used gridded glass windows to trace their scenes. The canvas in digital or traditional painting is that same glass, and every perspective rule is simply a description of how three-dimensional points project onto it.
**Use in output:** Think of the canvas as a pane of glass placed between you and the scene. You are tracing what you would see through the glass at a single frozen moment. Every perspective rule — where lines converge, how objects shrink with distance — is just a description of how the three-dimensional objects project onto that glass. If something looks wrong perspectively, ask: if I were actually looking through the glass at this scene, would it look the way I have drawn it?

---

### Aerial perspective
*Same concept as "Distance fade" above — this is an older term for the same effect. Use "Distance fade" and the coaching language from that entry.*

---

### Horizon line (at ground level vs elevated views)
**Plain name:** High horizon vs low horizon — how the viewer's height changes everything in the scene
**Plain definition:** The difference between placing the eye-level line low in the image (creating a low-horizon view, as seen by someone close to the ground) versus placing it high (creating a high-horizon or bird's-eye view looking down on the scene).
**Example:** Compare two photographs of a city street: one taken from the pavement with the camera at knee height (horizon line near the bottom of the photo — buildings tower above), and one taken from the top floor of a building (horizon line near the top of the photo — you are looking down onto roof tops and the street is far below). The actual street and buildings are identical in both photos. Only the camera height changed. That single decision — where the horizon line sits in the frame — entirely controls the emotional quality of the scene: low horizon feels monumental, high horizon feels like a map or overview.
**Use in output:** The current position of the eye-level line in this scene is placing the viewer at [describe: ground level / mid-height / above the scene]. Is that the feeling you want? Lowering the eye-level line toward the bottom of the canvas will make everything in the scene tower over the viewer; raising it toward the top will let the viewer look down and see the tops of objects. Adjust it now, before adding more detail — it is much easier to shift early than late.

---

### Convergence
**Plain name:** The coming-together of parallel lines — how lines that are actually parallel appear to meet in the distance
**Plain definition:** The visual effect by which two or more lines that are truly parallel in real life appear to angle toward each other and meet at a point as they extend into the distance.
**Example:** Look at a long straight road from above on a map — the two edges of the road are parallel lines a constant distance apart. Now look at the same road from standing height at one end. The two edges appear to narrow and meet at a point on the horizon. The road did not change shape; your viewpoint did. Every set of parallel lines that runs in any direction has exactly this behavior when viewed from a position that is not directly perpendicular to them — they appear to converge. Getting convergence wrong is the most common cause of a scene that looks "off" even when you cannot identify why.
**Use in output:** Check this pair of edges — the top and bottom of this wall, the two sides of this road. Are both lines aiming at the same point in the distance? Hold a straightedge against each line and extend it mentally. If they would meet at two different points rather than one, the convergence is inconsistent and the parallel relationship is broken. Correct them so both lines aim at the same dot.

---

### Linear perspective
**Plain name:** Lines-to-a-dot depth system — the family of perspective methods that all work by making parallel lines appear to meet at dots on the horizon
**Plain definition:** The overall system of depth drawing in which lines that are actually parallel in real life appear to converge toward one or more fixed dots on the horizon line, creating the illusion of three-dimensional space on a flat surface.
**Example:** Stand in the middle of a long, straight railway track and look down the track. The two rails appear to get closer and closer until they seem to touch at a single point far ahead. The track did not actually narrow — your viewpoint made the parallel rails appear to meet. That single meeting point is the core idea behind the whole system. Whether a scene uses one meeting point (a hallway viewed straight on), two meeting points (a building seen from its corner), or three (a building seen from far below or above), the basic principle is the same: parallel lines appear to converge toward dots, and placing those dots correctly is what makes the scene read as three-dimensional.
**Use in output:** Linear perspective is the umbrella term for all the dot-on-the-horizon methods — one-point, two-point, and three-point perspective all belong to this family. The method you choose depends on your viewpoint: looking straight at a face uses one dot; looking at a corner uses two; looking steeply up or down uses three. All three work by the same underlying rule: find your horizon line, place your dots on it, and make all the parallel edges in the scene aim at the correct dot.

---

### Isometric / parallel projection
*(Advanced — most hobbyists do not need this.)*
**Plain name:** Flat-depth view — a way of showing three dimensions where parallel edges stay parallel and never converge
**Plain definition:** A method of drawing three-dimensional objects in which all parallel edges in real life remain parallel on the page — they do not converge toward a vanishing point — giving a crisp, technical look where depth is shown by angle rather than by shrinking.
**Example:** Look at a technical diagram of a piece of flat-pack furniture assembly — the kind printed in the instruction booklet. The cabinet is shown in three dimensions, but the front edges are perfectly vertical, the top edges are perfectly horizontal, and the side edges all go off at the same diagonal angle. Nothing converges. Nothing shrinks. The far end of the cabinet is the same size as the near end. That flat, diagrammatic clarity is isometric projection. Compare it to a photograph of the same cabinet: in the photo, the far end looks smaller and the edges all converge toward dots. Isometric drawings trade photographic realism for consistency and readability — every measurement in the drawing can be read directly off the page at a fixed scale, which is why engineers, game designers, and architects use it.
**Use in output:** Isometric projection is widely used in game art, technical illustration, and certain graphic design styles. If you are working in this style, be aware that it is a deliberate departure from photographic perspective — the rules are different. Edges that are parallel in real life stay parallel on the page; there are no vanishing points; and the three visible faces of a box are each drawn at a consistent 30-degree angle from the horizontal. Mixing standard perspective with isometric elements in the same image will look inconsistent.

---

## Software Tools

---

### layer (in digital painting context)
**Plain name:** Layer — a separate sheet you can draw on
**Plain definition:** A layer is a separate, invisible sheet sitting above or below your drawing, so you can add or change things on it without ever touching the art underneath.
**Example:** Think of an overhead projector from school. You can lay a fresh clear sheet of film on top of the projected image and draw on the new sheet with a marker. Whatever you draw sits on top without touching the original. You can slide that sheet out, scribble on it, and throw it away — the original is untouched. Layers in painting software work the same way: each one is a separate sheet of film stacked in order.
**Use in output:** "Create a new layer for this step — think of it as a fresh sheet of clear film placed on top of your painting. You can draw or paint on it without disturbing anything you've already done, and if you don't like the result, you can simply delete that sheet and start again."

---

### new layer
**Plain name:** New layer — a blank sheet added on top
**Plain definition:** Adding a new layer creates an empty, transparent sheet placed on top of everything you've already painted, ready for you to work on without risk to the art below.
**Example:** Imagine you have a finished pencil drawing on paper. Instead of erasing and redrawing on the same sheet, you place a second blank sheet of tracing paper on top and draw your changes there. If you hate the changes, you crumple up the second sheet and the original is perfectly fine. "Add a new layer" in the software does exactly this — it slides a fresh blank sheet on top of your stack.
**Use in output:** "Before you start this step, add a new layer — it keeps your existing work safe underneath while you experiment on a fresh surface. You can find the button to add a new layer in the Layers panel (usually a small page icon with a plus sign)."

---

### layer opacity
**Plain name:** Layer transparency — how see-through that sheet is
**Plain definition:** Layer opacity controls how visible or see-through one whole layer is, like adjusting how heavily a sheet of frosted glass sits over the layers below it.
**Example:** Hold a white tissue paper over a photograph. When you hold one layer of tissue, you can still mostly see the photo through it. Stack ten tissues and the photo nearly disappears. Drag the opacity slider on a layer and you are choosing how many "tissues thick" that layer is — 100% is a solid sheet; 10% is almost invisible.
**Use in output:** "Lower the opacity of that layer to around 20–30% — there is a slider at the top of the Layers panel. At full strength the paint will look too heavy; pulling the slider left makes the whole layer partially see-through, so the color blends gently with what's underneath."

---

### blending modes (general concept)
**Plain name:** Blend mode — the rule for how two layers mix together
**Plain definition:** A blend mode is a setting that tells the software exactly how the colors on one layer should interact with the colors on the layer below — instead of simply covering them, you can choose options like multiply them, add their brightness together, or only keep the dark parts.
**Example:** Imagine printing a photo on transparent film and holding it under a bright lamp, then placing a second film on top. Depending on how you combine them — whether you press them tightly together, hold one above the lamp and one below, or illuminate only the edges — the final image on the wall looks completely different. Each of those arrangements is a different "blend mode." In painting software, you pick the rule from a dropdown menu at the top of the Layers panel; "Normal" just covers, "Multiply" darkens, "Screen" lightens.
**Use in output:** "Change that layer's blend mode to Multiply — you'll find it in the dropdown at the very top of the Layers panel (it probably says 'Normal' right now). Multiply mode acts like stacking two photographic slides: the dark parts of the top layer make the layer below it darker, so shadows become richer without painting over your detail."

---

### soft brush
**Plain name:** Soft brush — a brush with fuzzy, blended edges
**Plain definition:** A soft brush lays down paint with edges that gradually fade out, like the edge of a puff of smoke, so there is no visible hard line where the paint starts or stops.
**Example:** Press a damp sponge flat against a table, then lift it. The mark left behind has edges that fade from full color to nothing — there is no sharp cut-off line. A soft brush makes marks like that: full color in the center, fading to transparent at the edges. Compare that with a rubber stamp, which leaves a sharp, hard-edged outline all the way around.
**Use in output:** "Switch to a soft brush for this — in your brush settings, drag the hardness slider all the way to the left (toward 0%). The edges of each stroke will blur out gently, which is what lets you blend colors smoothly without leaving a visible outline where the brush started."

---

### hard brush
**Plain name:** Hard brush — a brush with sharp, clean edges
**Plain definition:** A hard brush lays down paint with crisp, clearly defined edges, like pressing a rubber stamp or a felt-tip pen directly onto the surface.
**Example:** Stamp a rubber stamp onto paper. The ink has a perfectly clear, sharp border all the way around the shape — there is no gradual fade. A hard brush in the software works the same way: every stroke has a clean, defined edge, which is why it is used for linework, crisp highlights, and areas where you want no blurring.
**Use in output:** "Use a hard brush here — drag the hardness slider all the way to the right (toward 100%). This gives you a clean, sharp-edged stroke with no fuzzy border, which is exactly what you need for a crisp highlight edge or a clean outline."

---

### airbrush
**Plain name:** Airbrush — a spray-paint style brush that builds up gradually
**Plain definition:** The airbrush tool sprays a very thin, soft mist of color that builds up slowly the longer you hold it in one spot, just like a can of spray paint held close versus far from the surface.
**Example:** Think of spray painting a wall with a can. If you move the can quickly, you get a very light, almost invisible mist. Hold it still in one spot and a dark patch of color slowly builds up. The airbrush tool in the software behaves exactly the same way: quick passes leave barely a trace, and hovering over one spot gradually deepens the color. That slow build-up is why it is perfect for adding gentle haze or a soft glow.
**Use in output:** "Grab a large airbrush and set the opacity low — around 10 to 15%. Move in slow, sweeping passes across the area. Because the airbrush builds up gradually, you have full control; if you go too far, just undo one step. A few passes will add a soft haze without any hard edges."

---

### eraser
**Plain name:** Eraser — removes paint from the current layer
**Plain definition:** The eraser removes paint from whatever layer you are currently working on, making those pixels transparent again, without affecting the layers above or below.
**Example:** Imagine you drew on a sheet of clear acetate film with a whiteboard marker. A cloth eraser lets you wipe away parts of what you drew on that sheet without touching the drawing on the sheet underneath it. The eraser tool works the same way: it clears paint off the layer you are on, revealing the layer below through the cleared area.
**Use in output:** "Use a soft eraser at low opacity to gently fade out the edge of that shape — set the eraser to about 20% strength and make light passes. At full strength the eraser removes everything sharply; at low strength it slowly fades the edge, so you can get a gradual, natural transition."

---

### smudge tool
**Plain name:** Smudge tool — pushes and drags wet paint around
**Plain definition:** The smudge tool acts like dragging a finger through wet paint — it stretches and pushes the colors already on the canvas rather than adding new color.
**Example:** Put a small drop of two different colored paints on paper and drag your fingertip through them. The colors stretch in the direction you drag, blend together at the edges, and leave a smeared trail. The smudge tool does exactly this on screen: it grabs the colors already painted and pulls them, which is useful for softening the boundary between two colors or creating the look of loose, blended strokes.
**Use in output:** "Pick up the smudge tool and drag it gently along the edge where those two colors meet — think of it as dragging a finger through fresh paint. Short strokes blend the edge softly. Longer strokes will pull the color out too far, so keep your strokes short and light."

---

### blur tool
**Plain name:** Blur tool — softens and fogs an area of the painting
**Plain definition:** The blur tool softens the detail in any area you brush over, making sharp edges and fine details look hazy and out of focus.
**Example:** Look through a steamed-up shower door at something on the other side. The shapes are still there but all the sharp detail is gone — everything blurs into soft patches of color. The blur tool does that to whatever you paint over: it takes the sharp detail out and leaves soft, smudged color behind, which is exactly how distant objects look in real life.
**Use in output:** "Take the blur tool and lightly brush over the far edge of those clouds — just a few passes at medium strength. It takes the sharp border away and makes that edge look soft and vaporous, which immediately reads as distance to the viewer."

---

### lasso / selection tool
**Plain name:** Selection tool — draws a fence around an area to protect the rest
**Plain definition:** The selection tool lets you draw a boundary around a specific part of your painting so that any change you make afterward only affects what is inside the fence, leaving everything outside it untouched.
**Example:** Imagine cutting a hole in a piece of paper and placing it over your painting. You can paint through the hole and only the paint that falls inside the hole touches the canvas. Everything the paper covers is protected. A selection works the same way: draw the selection around the area you want to change, and every tool you use — brushing, filling, adjusting color — only reaches inside that boundary.
**Use in output:** "Use the lasso tool to draw roughly around just the water area, then make your changes inside that selection. Everything outside it will be completely protected — none of the sky or characters will be affected by what you do next."

---

### mask (layer mask)
**Plain name:** Layer mask — a stencil that hides parts of a layer without deleting them
**Plain definition:** A layer mask is a separate black-and-white stencil attached to a layer; black on the mask hides the layer's paint, white reveals it, and you can repaint the mask at any time to show or hide more — nothing is ever permanently deleted.
**Example:** Take a piece of card, cut a shape out of the middle, and hold it over a photograph. The cutout hole reveals the photo; the card covers the rest. Now imagine you can reshape that cutout any time by drawing on it — making the hole bigger to reveal more, or drawing over part of the hole to cover it again. The layer mask is that card: it never touches the actual photo. Your painting stays intact underneath; you are only controlling what shows through.
**Use in output:** "Rather than erasing that area directly, add a layer mask — the small rectangle icon at the bottom of the Layers panel. Paint black on the mask to hide parts of the layer, and white to bring them back. Because nothing is actually deleted, you can always change your mind later."

---

### clipping mask
**Plain name:** Clipping mask — a layer that stays inside the shape below it
**Plain definition:** A clipping mask locks one layer so its paint can only appear inside the boundaries of the layer directly below it — anything painted outside those boundaries is automatically hidden.
**Example:** Pour paint onto a cookie cutter sitting on paper. The cookie cutter is the shape — the paint fills the inside and the cutter prevents it from spreading outside. A clipping mask works the same way: the layer below it acts as the cookie cutter, and whatever you paint on the clipped layer only shows up within that shape.
**Use in output:** "Create a new layer, right-click it, and choose 'Create Clipping Mask' — this clips it to the layer below. Now you can paint shadows and highlights on this clipped layer and they will stay perfectly inside your character's outline. No tidying up around the edges."

---

### merge / flatten
**Plain name:** Merge / Flatten — combining multiple sheets into one permanent sheet
**Plain definition:** Merging or flattening combines two or more separate layers into a single layer, which simplifies your file but removes the ability to edit each layer independently afterward.
**Example:** Take four sheets of tracing paper with drawings on them, hold them tightly together, and make a photocopy. The photocopy shows everything from all four sheets but is now a single piece of paper — you cannot separate the layers again. Merging layers does exactly this in the software: it bakes the chosen layers into one, which makes the file simpler and faster to work with but means you can no longer move or change each layer separately.
**Use in output:** "Before you merge those layers, make sure you are happy with all of them — once they are combined into one, you cannot separate them again. When you are ready, select them all in the Layers panel and choose Merge Layers (or press Ctrl/Cmd+E). From that point they behave as a single piece of painting."

---

### non-destructive editing
**Plain name:** Non-destructive editing — making changes you can always take back
**Plain definition:** Non-destructive editing means making adjustments in a way that never permanently changes your original painting, so you can undo, tweak, or remove any change at any time.
**Example:** Imagine writing notes on sticky notes placed over a book page instead of writing in the margins with a pen. You can peel the sticky notes off at any time; the original page is untouched. Working on separate layers, using layer masks, or using adjustment layers are all "sticky note" methods: they change how the image looks without ever altering the original paint underneath.
**Use in output:** "Keep your edits non-destructive at this stage — that means working on separate layers and using masks rather than painting directly onto your original. Think of it as writing on sticky notes placed on top of your painting. You can remove them any time and the painting underneath is exactly as you left it."

---

### color picker
**Plain name:** Color picker — the palette panel where you choose your paint color
**Plain definition:** The color picker is the panel or popup where you choose exactly which color the brush will paint with — you can click anywhere on a rainbow gradient or type in a number to pin down a precise color.
**Example:** Think of it as an enormous paint-chip display at a hardware store, except instead of picking up a chip and taking it to the desk, you just click on the exact shade you want and your brush is instantly loaded with that color. The large square in the center of the panel lets you fine-tune exactly how light or dark and how vivid or muted the chosen color is.
**Use in output:** "Open the color picker — it is usually the two overlapping squares near the bottom of the toolbox. Click inside the large color square to choose a precise shade: move toward the top-right corner for a brighter, purer color, and toward the bottom for a darker one. The vertical bar on the right side moves between hues (reds, blues, greens, and so on)."

---

### eyedropper
**Plain name:** Eyedropper — samples a color already in your painting
**Plain definition:** The eyedropper tool lets you click on any color already in your painting and instantly loads that exact color into your brush, so you can pick up and reuse colors without guessing.
**Example:** Imagine dipping a clean brush into a color you already mixed on your palette. You are not mixing a new color — you are just picking up one that already exists. The eyedropper does the same thing: click on any pixel in your painting and your brush is immediately set to that exact color.
**Use in output:** "Instead of trying to mix that color again from scratch, use the eyedropper — hold Alt (on Windows) or Option (on Mac) while using any brush and click the color you want to match. Your brush will immediately switch to that exact color. Release the key and your brush is ready to paint with it."

---

### dodge tool
**Plain name:** Dodge tool — a brush that makes areas brighter
**Plain definition:** The dodge tool brightens whatever you brush over, as though you are shining a small flashlight onto that part of the painting.
**Example:** Take a photograph and shine a small torch onto one corner of it in a darkened room. That corner looks noticeably brighter, even though you have not changed the photo. The dodge tool does this digitally: drag it across any area and those pixels brighten up as if lit from a fresh light source. The effect builds up gradually the more you go over the same spot.
**Use in output:** "Pick up the dodge tool (it looks like a lollipop in the toolbox) and set it to a low exposure — about 10 to 15%. Lightly brush over the very top edges of the waves where the light would hit. Each pass brightens them a little more. A low exposure lets you build the brightness gradually so it stays believable."

---

### burn tool
**Plain name:** Burn tool — a brush that makes areas darker
**Plain definition:** The burn tool darkens whatever you brush over, as though you are holding a piece of paper close to a flame — the areas you pass over gradually deepen in tone.
**Example:** Imagine a piece of dark sunglasses lens held close to a window letting light through unevenly — the areas that receive less light look darker and richer. The burn tool deepens whatever it touches in the same gradual way: a single pass darkens a little, several passes darken more. It is the shadow-building counterpart to the dodge tool.
**Use in output:** "Use the burn tool to deepen the shadow under those clouds — set exposure to about 10% and make gentle overlapping passes over the base of the cloud band. At low exposure the darkening builds slowly and stays smooth; cranking the exposure too high can make the shadow look muddy, so keep it subtle."

---

### stamp / clone tool
**Plain name:** Clone / Stamp tool — copies one part of the painting to another place
**Plain definition:** The clone tool lets you pick a sample spot on your painting and then paint a copy of whatever is at that spot onto a different area, which is useful for repeating a texture or covering up an unwanted mark.
**Example:** Think of a rubber stamp dipped in ink that reproduces whatever image is carved into it. You press it down, pick it up, and press it somewhere else — and an identical copy appears. The clone tool works the same way: you Alt-click (or Option-click) to "load" the stamp from a spot in your painting, then brush somewhere else and the software paints an exact copy of the loaded area there.
**Use in output:** "Grab the clone / stamp tool to fill that gap. Hold Alt (Windows) or Option (Mac) and click the area of texture you want to copy — that loads the stamp. Then release the key and brush over the gap you need to fill. The tool will paint an exact copy of whatever you sampled, matching the surrounding texture."

---

### fill (bucket fill)
**Plain name:** Fill / Bucket — pours one flat color into a whole area at once
**Plain definition:** The fill tool floods a connected area of the same color with your chosen color in a single click, the same way pouring a bucket of paint fills every connected section of a flat surface.
**Example:** Imagine pouring a bucket of red paint onto the floor of a room. The paint spreads instantly into every part of the floor connected to where you poured, and stops at any wall or raised edge. That is exactly how the fill tool works: click inside any enclosed shape and the tool floods it with your chosen color in one click, stopping at the edges of the shape.
**Use in output:** "Use the fill tool to lay down the base color quickly — just click inside the outlined shape and it will flood the whole area with your chosen color in one go. Make sure the area is fully enclosed first (no gaps in the outline), otherwise the color will leak outside the shape."

---

### gradient tool
**Plain name:** Gradient tool — paints a smooth fade from one color to another
**Plain definition:** The gradient tool paints a smooth, gradual blend from one color to another across the area you drag over, creating a transition with no visible brushstrokes.
**Example:** Watch a clear sky at sunset: right at the horizon it is bright warm orange and by the time you look straight up it has faded completely to deep blue, with a smooth, unbroken blend in between. There are no brush marks or sudden jumps. The gradient tool produces exactly that kind of smooth fade: you drag from one side to the other and the software fills in the transition automatically.
**Use in output:** "Use the gradient tool to build the sky fade — click at the top of the canvas, hold Shift to keep it perfectly straight, and drag down to the horizon line. The tool will fill the area with a smooth transition from deep black at the top to your lighter horizon color at the bottom. No brush strokes needed."

---

### PPI / DPI
*(Advanced — most hobbyists do not need this for screen work, but it matters at export time for print.)*
**Plain name:** PPI / DPI — how many pixels (or printed dots) fit into one inch of the final output
**Plain definition:** A number that describes how densely packed the pixels or ink dots are in a given inch of the output — a higher number means more detail is packed into each inch, which is required for sharp printed results but irrelevant for screen display.
**Example:** Take a printed newspaper photograph and hold a magnifying glass over it. You can see the individual ink dots the printer used — thousands of tiny dots packed together to create the illusion of a smooth image. A low-quality print uses fewer, larger dots per inch, so the image looks grainy up close; a high-quality print uses more, smaller dots per inch, so the image looks smooth even under magnification. When you export a digital painting for print, the PPI setting tells the printer how many of your image's pixels should be squeezed into each inch of paper. Too few pixels per inch and the printed image looks blocky; the standard for most printed artwork is 300 pixels per inch at the final print size.
**Use in output:** "For screen display — sharing online, social media, a digital portfolio — the PPI number does not matter; only the total pixel dimensions count. But if you are printing your work, check that your canvas was set up at 300 PPI at the final print size before you started. If it was not, you may not have enough pixels to print at the size you want without visible blockiness. You can check this in the canvas settings or the image size dialog of your software."

---

### Adjustment layer
**Plain name:** Adjustment layer — a special layer that changes colour or brightness without touching the original paint
**Plain definition:** A type of layer that applies a colour or brightness change to everything below it in the layer stack, without permanently altering the original painted layers — you can edit, turn off, or delete the adjustment at any time.
**Example:** Imagine you have a finished watercolour painting. Instead of painting over it, you hold a tinted sheet of transparent glass in front of it — the painting looks warmer, cooler, brighter, or darker through the glass, but the painting itself is untouched. Remove the glass and the painting is exactly as it was. An adjustment layer works exactly like that tinted glass: it sits above your painted layers and changes how they look, but your original brush strokes are never touched. You can make the whole image warmer, darker, more vivid, or shifted in hue at any point — and reverse the change completely if you change your mind.
**Use in output:** "Rather than painting directly over your work to fix the [brightness / colour / contrast], add an adjustment layer — look for the half-filled circle icon at the bottom of the Layers panel, or go to Layer > New Adjustment Layer. Choose [Levels / Curves / Hue-Saturation / Colour Balance] depending on what you want to fix. The adjustment sits above your painting like a filter: change it, reduce its opacity, or delete it at any time without ever touching the original."

---

## Pipeline and Workflow

---

### thumbnail stage
**Plain name:** Thumbnail stage — tiny rough sketches to test the layout before committing
**Plain definition:** The thumbnail stage is when you make a series of very small, rough sketches — each one the size of a postage stamp or a phone icon — to try out different arrangements of the main shapes in your scene before any detailed drawing begins.
**Example:** Before a film director starts filming, they sketch tiny comic-strip panels showing roughly where each actor will stand and where the camera will point. The drawings are messy and tiny — just enough to check whether the scene makes sense as a picture. Thumbnails work exactly the same way: small, fast, low-cost. If the layout is dull or confusing in a thumbnail no bigger than a coin, adding detail will not fix it.
**Use in output:** "Before drawing anything in detail, spend five to ten minutes on thumbnails — fill a small area of your canvas with coin-sized rough sketches, each one testing a different layout for your scene. Keep them rough: just dark and light shapes, no detail. The goal is to find the strongest arrangement of your main elements before investing time in anything detailed."

---

### sketch stage
**Plain name:** Sketch stage — a rough drawing that works out the shapes and proportions
**Plain definition:** The sketch stage is a loose, exploratory drawing that figures out where all the major shapes go and how they relate to each other in size — it is not meant to look clean, only to solve the layout before the tidy linework begins.
**Example:** When a builder plans a room, they first draw a rough pencil floor plan on scratch paper — just rectangles for walls and squares for furniture — to check everything fits. Nobody frames that rough plan; it is just for working things out. The sketch stage in painting is that rough plan: loose marks that find the right positions and sizes before you draw anything neatly.
**Use in output:** "Start with a loose sketch layer — keep it rough and fast. Use a big brush and simple shapes to work out where everything goes. Do not worry about clean lines at this point; the sketch is just for solving the 'does this fit?' question before you tighten things up."

---

### linework stage
**Plain name:** Linework stage — drawing clean, confident outlines
**Plain definition:** The linework stage is when you draw the final clean outlines over your rough sketch, creating crisp, definite lines that will serve as the outline structure for the rest of the painting.
**Example:** Architects draw a faint pencil plan first, then go over it with a sharp technical pen to produce the clean final drawing. The pencil marks are then erased or hidden. The linework stage is exactly that second pass: you already know where everything goes from the sketch, so now you draw each line cleanly and with confidence.
**Use in output:** "Create a new layer on top of your sketch and draw your clean outlines on it — take your time with each line, drawing from your shoulder rather than your wrist for long, smooth strokes. When you are happy, you can lower the opacity of your sketch layer or hide it, leaving only the clean lines visible."

---

### flat colour stage
**Plain name:** Flat colour stage — filling every area with one solid base color, no shading yet
**Plain definition:** In the flat colour stage you fill every part of your image with a single, solid, unshaded color — no highlights, no shadows — just so every area has its basic color established before any lighting work begins.
**Example:** Think of a paint-by-numbers page just after you have finished every numbered zone but before you add any blending or shading. Every section has its color but looks completely flat and evenly lit — like a cartoon cel. That is the flat colour stage: it locks in what color everything is before you start working out how the light falls on it.
**Use in output:** "Fill in all your flat colors now — one solid color per area, no shadows or highlights yet. Use the fill tool or a hard brush to lay down a clean, even tone for each element: one for the sky, one for the water, one for the ship, and so on. Getting the flat colors right first makes the shading stage much easier."

---

### rendering / shading stage
**Plain name:** Rendering / Shading stage — adding light and shadow to make shapes look three-dimensional
**Plain definition:** The rendering or shading stage is when you paint the areas of light and shadow onto your flat-coloured image, turning the flat, cartoon-like shapes into objects that look solid and three-dimensional — as if you could reach in and pick them up.
**Example:** Look at a photograph printed in flat, poster-like colors — every area one solid tone. Now imagine going back over it with a soft pencil, darkening the sides facing away from the light and brightening the sides facing toward it. The flat shapes suddenly start to look like real, round, solid objects. That is rendering: adding the light-and-shadow information that makes the painting feel like it exists in space.
**Use in output:** "Now that your flat colours are down, start the shading pass. On a new layer above the flat colour, use a soft brush at low opacity to darken the side of each shape that faces away from your light source. Build that up gradually, then add a lighter pass on the side that faces toward the light. Step back regularly to check the shapes are reading as solid."

---

### detail pass
**Plain name:** Detail pass — adding fine surface information after the main shapes are established
**Plain definition:** A detail pass is a late-stage round of work where you zoom in and add small, specific information — textures, fine edges, small markings — after the overall shapes, values, and colors are already settled.
**Example:** A carpenter builds the cabinet first (the big solid shape), then fits the drawer handles and sands the surface smooth. They do not carve the handles before the cabinet is assembled. A detail pass is the same idea: you only add fine details — rivets, eyelashes, bark texture, writing — after the larger decisions are locked, because the big shapes determine whether the detail is even in the right place.
**Use in output:** "Hold off on fine details for now — get the big shapes, proportions, and values right first. Once those are locked in, zoom into the areas that need it most and do a detail pass: add small markings, sharp edges, and fine textures. Detail applied before the large shapes are correct often has to be repainted anyway."

---

### polish pass
**Plain name:** Polish pass — the final round of small fixes and refinements before the image is finished
**Plain definition:** The polish pass is the last stage of work, where you clean up rough edges, adjust any colors that feel slightly off, add final highlights, and make sure the whole image looks coherent and finished.
**Example:** Think of a mechanic doing a final check-over before a car leaves the garage: tightening a loose bolt here, wiping off a smudge there, checking that all the lights work. The car is essentially done — this stage is not rebuilding it, just making sure every small thing is right. The polish pass is that final check and tidy: nothing major changes, but everything gets the attention it needs to look finished.
**Use in output:** "You are at the polish stage — the big decisions are made, so now work through the image methodically: clean up any rough edges, sharpen the focal point, pop any highlights that look dull, and check that the whole image reads well at a small size. Small changes made here have a surprisingly large effect on how finished the piece looks."

---

### reference gathering
**Plain name:** Reference gathering — collecting real photos or images before you start drawing
**Plain definition:** Reference gathering is the step where you collect photographs, screenshots, or other visual sources before drawing, so you have accurate real-world information to look at while you work.
**Example:** Before a cook prepares a dish they have never made before, they look at the recipe and photographs of how the finished dish should look. They are not copying the photo — they are using it so they have accurate information about color, texture, and shape. Reference gathering is exactly that: finding the visual information you need before you start, so you are working from evidence rather than guessing.
**Use in output:** "Before drawing that element, take a few minutes to gather reference — search for photographs of the real thing and keep them visible alongside your canvas (pin them in a second window or on your phone). You do not trace them; you use them to check that your shapes, proportions, and details are accurate. Guessing from memory nearly always produces something slightly off."

---

### master study
**Plain name:** Master study — copying a finished painting closely to understand how it was made
**Plain definition:** A master study is a deliberate exercise where you reproduce a finished piece of art as accurately as you can, not to steal it, but to reverse-engineer the decisions the original artist made about color, light, and composition.
**Example:** A music student learns to play a complex piano piece note for note — not to perform it as their own, but because playing through it forces them to understand every chord change, every rhythm decision, every technical choice the composer made. A master study in painting is the same exercise: copying a great painting forces you to work through every decision the artist made, which teaches you things you would never discover just by looking.
**Use in output:** "Try a master study of that image — set your canvas to the same proportions and work through it as accurately as you can: match the large shapes first, then the values, then the colors. The goal is not to copy it for any other use; it is to make your hands work through every decision the original artist made. You will spot things in ten minutes of copying that you would miss in an hour of just looking."

---

### colour study
**Plain name:** Colour study — a small quick version of the image to test the color plan before the real thing
**Plain definition:** A colour study is a small, roughly painted version of your planned image done specifically to test whether your chosen colors work together, before committing to the full-size piece.
**Example:** An interior designer paints sample squares of a few candidate wall colors onto a piece of card and holds them up in the room before buying gallons of paint. A colour study does the same thing for a painting: you paint a tiny, rough version at small scale to see whether the colors you have in mind look right together in context, so if they do not work you have only spent a few minutes, not hours.
**Use in output:** "Before going further, paint a quick rough test on a tiny canvas — even 400 pixels wide is fine. Block in the rough shapes and fill them with the colours you are planning to use. The goal is not to finish this version; just check whether your colours work together and whether the image still looks clear when you squint at it. It is much faster to change your mind now than after hours of detailed painting."

---

### value study
**Plain name:** Value study — a small black-and-white version of the image to test the light plan
**Plain definition:** A value study is a small, black-and-white or grayscale rough version of your planned image done to check whether the light and dark areas create a clear, readable composition before any color is added.
**Example:** Squint at any photograph until your eyes are almost closed and the colour disappears — what you see is a pattern of light blobs and dark blobs. If those blobs still make an interesting picture even when blurred beyond recognition, the image has a strong foundation. A value study forces you to test this on purpose: paint a small rough version in grey only to check that the light and dark areas form a clear, interesting arrangement.
**Use in output:** "Do a value study first — work in black and white on a tiny canvas, using just three or four shades of grey. Fill the areas that will be in light with a pale grey and the areas in shadow with a dark grey. Then squint hard at it. If the important shapes are still obvious and the image makes sense at that small, blurry scale, your light-and-dark design is strong enough to move forward with."

---

### warm-up sketch
**Plain name:** Warm-up sketch — a few loose drawings done at the start to get your hand moving
**Plain definition:** A warm-up sketch is a short session of quick, loose drawing done at the very beginning of a work session, purely to get your hand and eye working together fluidly before starting on anything you care about.
**Example:** A runner spends the first five minutes walking and jogging lightly before the proper run. They are not covering useful distance yet — they are waking their muscles up so the actual run goes better. Warm-up sketches are the same: a few minutes of fast, loose scribbling at the start of a session, drawing whatever comes to mind, gets your hand moving confidently before you touch the real project.
**Use in output:** "If you are feeling stiff or your lines are coming out wobbly, spend three to five minutes on warm-up sketches on a separate canvas — just quick, flowing marks and loose shapes, nothing precious. Drawing a few pages of loose scribbly lines, circles, and random scribbled shapes wakes up the connection between your eye and your hand, so when you start on your actual piece the first strokes come out more confidently."

---

### overpainting
**Plain name:** Overpainting — painting a new image on top of an existing one to improve or change it
**Plain definition:** Overpainting means painting a revised or improved version directly over an existing image, keeping the underlying work as a structural guide while replacing or updating parts of the surface.
**Example:** Imagine drawing a light pencil map of a country, then painting a detailed landscape painting over it — you use the pencil lines to keep everything in the right place, but the final surface is all fresh paint. Overpainting a digital piece works the same way: you use what is already there as a positioning guide and progressively replace the old surface with better, fresher work.
**Use in output:** "Rather than starting over, try overpainting — create a new layer on top and begin redrawing directly over the problem areas. Keep the parts you are happy with visible underneath as a reference, and paint the corrected version on top. Once the new version is right, you can hide or delete the old layer beneath."

---

### underpainting (digital)
**Plain name:** Underpainting — a simplified first layer that maps out the dark areas before the real painting begins
**Plain definition:** An underpainting is a rough first pass painted in a single dark tone that maps out the shadow areas across the whole image, giving you a guide for where the lights and darks will go before you start adding full color.
**Example:** Before painting a room, a decorator sometimes applies a tinted primer coat that gives an overall tone to the wall. It is not the final color — it is a base that influences how every coat of paint on top will look. An underpainting works the same way: a simple dark layer that defines the shadow shapes gives every paint layer on top a starting structure to work from.
**Use in output:** "Start with an underpainting — on your base layer, use a mid-dark tone to roughly fill in all the areas that will be in shadow. Do not worry about detail; just block out where the darks go. This gives you a map to work from: the areas you left unpainted will become your lights, and everything you filled in will be your shadows."

---

### blocking in
**Plain name:** Blocking in — filling the main areas with simple flat shapes before adding any detail
**Plain definition:** Blocking in is the early step where you fill the major areas of your image with rough, flat shapes of approximately the right color or tone — establishing the large-scale layout without any detail or refinement.
**Example:** A sculptor starting a clay figure does not begin by sculpting an ear. They first shape the big lump of clay into a rough upright figure — a head, a torso, two legs — just big, simple blobs of the right size, with no detail at all. All the fine detail comes later. Blocking in is the same first step in painting: fill in rough shapes for the sky, the ground, the character, the background — just big areas of approximate color to establish the layout before anything is refined.
**Use in output:** "Block in the major areas first — use a big, flat brush and fill each zone of the image with a rough approximation of its final color. Sky, ground, character, background: each one gets a solid patch of color, even if it looks crude. Do not paint any detail yet. Once all the main areas are in, you can see whether the overall picture is working before you invest time in anything small."

---

### construction pass
**Plain name:** Construction pass — drawing the underlying structure of shapes before the surface is painted
**Plain definition:** A construction pass is a drawing stage where you work out the structural skeleton of your objects — using simple geometric shapes like boxes and cylinders — before drawing the final surface details on top.
**Example:** An architect draws a floor plan and structural diagram of a building before deciding on the tiles, paint, and furniture. The structural drawing is not the finished look — it is the plan that makes sure the building will stand up and the rooms will be the right size. A construction pass in drawing works the same way: you build simple box-and-cylinder shapes to solve the structure and proportions first, and the detailed surface is drawn on top of that solid foundation.
**Use in output:** "Do a construction pass before the detail — rough in the main shapes as simple geometric forms: boxes for the body, cylinders for the limbs, a sphere for the head. They do not need to look like anything yet; they are just structural guides. Once the shapes and proportions are correct at this simple level, drawing the surface detail on top will be much easier and more accurate."

---

### cleanup pass
**Plain name:** Cleanup pass — going back through the image to fix messy edges and stray marks
**Plain definition:** A cleanup pass is a focused round of work dedicated to finding and fixing untidy areas — stray marks outside lines, rough edges, color that bled into the wrong area — rather than adding new content.
**Example:** After icing a cake, a baker goes back around the edges with a palette knife to smooth any rough spots and wipe away drips that landed on the plate. They are not adding new decoration — they are fixing the small messiness left from the previous step. A cleanup pass is that same round of tidying: methodically working through the image to fix any mess left by the previous stages.
**Use in output:** "Do a cleanup pass now — zoom into each section of your image and look for stray marks, rough edges, or color that has spread outside the area it belongs in. Use a hard eraser or a hard brush matching the background color to tighten up the edges. This pass is purely about tidying, not adding new content; work slowly and methodically rather than quickly."

---

### Primary source / locked reference
**Plain name:** Locked reference — an earlier decision that all later work must agree with
**Plain definition:** An approved earlier-stage document — such as a finished thumbnail, a value study, or a construction drawing — that is treated as the authoritative version of a key decision, so that later stages of the painting do not accidentally undo good work already done.
**Example:** Imagine you have spent an hour finding exactly the right arrangement of furniture in a room, and you take a photograph of it. That photograph is now your locked reference — if a mover accidentally shifts a chair, you hold the photo up and put the chair back where it was. You do not rethink the layout from scratch; the photograph settles the argument. In a painting pipeline, a locked reference works exactly the same way: once a thumbnail has been approved for composition, or a value study has been finalised, those documents are pinned in place. If a later shading pass accidentally makes the composition muddier or a colour pass shifts the values, the locked reference is the standard you return to.
**Use in output:** Pin your approved thumbnail (or value study, or construction sketch) somewhere visible while you work on later stages. Any time a later pass feels like it is drifting — the values look muddy, the composition feels off — compare what is on your canvas to the locked reference. Nine times out of ten, the locked reference will show you exactly what changed and where to restore it.

---

### Step-gate
**Plain name:** Stage sign-off — a short checklist you run before moving to the next step
**Plain definition:** The practice of deliberately checking that the current stage of work meets its own goals before allowing yourself to move on to the next stage, so that problems do not get carried forward and buried under new work.
**Example:** A pilot runs through a pre-flight checklist before every single flight — not because they have forgotten how to fly, but because "I think everything is fine" is not the same as "I have checked that everything is fine." The checklist catches things that feel fine but are not. A stage sign-off before moving from sketching to linework, or from linework to flat colour, works the same way: a brief deliberate check (does the composition work? are the proportions right? is the value structure clear?) before committing to the next stage. Finding a proportion problem before the linework is quick to fix. Finding the same problem after the rendering is done is expensive.
**Use in output:** Before moving from [current stage] to [next stage], run a quick check: does the [composition / proportion / value structure / perspective] hold up? Squint at it, flip it horizontally, look at it at thumbnail size. If anything feels wrong at this stage, fix it now — it will be ten times harder to fix once the next stage of work is on top of it.

---