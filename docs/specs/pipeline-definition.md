# Pipeline Definition — Digital Art Teaching Assistant

**Status:** DRAFT — PENDING OWNER CONFIRMATION
**Date:** 2026-10-02
**Supersedes:** `art-theory-draft/art-theory/pipeline/00-overview.md` (which remains as a plain-English user-facing entry point; this file is the authoritative backstage specification)
**Required for:** Issues #7–#17 (pipeline step files). No pipeline step file may be started until the owner has confirmed this document by commenting on GitHub issue #36.

---

## Section 1 — Scope

This pipeline covers the full range of 2D digital art creation tasks the teaching assistant may be asked about. No assumption is made about the user's medium, style, subject, or workflow type. The pipeline adapts per medium; steps that do not apply to a specific medium are explicitly marked as SKIP with a documented sign-off condition.

### Art types covered

- Digital illustration (standalone images)
- Character art (character design and character sheet)
- Environment art (landscapes, interiors, backgrounds)
- Creature design
- Comics and sequential art (American superhero, European BD, anthology)
- Manga (traditional and digital, Japanese right-to-left and Western left-to-right)
- Webtoon (vertical scroll, mobile-optimised)
- B&W illustration (pen and ink, pencil, charcoal)
- Line art (pure black line on white, no tone)
- Mixed traditional-to-digital workflows

### Subject types covered

Figures, faces, environments, creatures, vehicles, architecture, abstract compositions, still life.

### Workflow types covered

- Digital-only
- Traditional-to-digital (sketch on paper, ink or scan, finish digitally)
- Fully traditional (pencil/ink/charcoal, scanned for delivery)

### Style registers covered

Realistic, stylized, painterly, graphic/flat, line art, manga, chibi, cartoon.

### Mediums covered

Full colour digital painting, greyscale digital painting, colour line art (coloured linework), pure black line art, manga B&W with screentone, manga B&W with grey wash, manga full colour, B&W pencil drawing, B&W ink drawing, B&W charcoal drawing, mixed (any of the above in combination).

---

## Section 2 — Pipeline Steps

### Step 01 — Brief & Ideation

**Purpose:** Establish what the image must achieve before a single mark is made. Every downstream decision is evaluated against the brief.

**Primary outputs:** A written or clearly held brief covering: purpose, intended audience, deliverable format, medium, style register, and any explicit constraints (size, colour palette limits, content restrictions).

**Governing fundamentals:** `fundamentals/design-and-shape-language.md`, `fundamentals/composition.md`

**Failure modes from skipping:**
- Starting work without a brief produces an image that satisfies no specific goal
- Medium constraints discovered late (e.g., print resolution, mono-only requirement) force complete restarts
- Style register conflicts emerge mid-image (e.g., switching between realistic and stylized mid-character)

**Medium variants:**

| Medium | Brief-specific requirements |
|---|---|
| Painted work (full colour) | Colour vs. greyscale decision; target resolution and export format; style register |
| Pure line art / inking | Print resolution minimum (600 DPI); inking style (American, European BD, or manga line quality); mono vs. colour decision |
| Manga (traditional) | Page/chapter brief; reading direction (right-to-left Japanese vs. left-to-right Western); publishing format (magazine → tankōbon, or standalone); screentone vs. grey-wash vs. no-tone decision |
| Manga (digital) | All of above plus: software (Clip Studio Paint EX vs. Pro — EX required for multi-page story management); export destination (print or webtoon) |
| Webtoon | Vertical scroll format; standard canvas 800px wide (working at 1600px for print option); episode pacing brief; platform submission specifications |
| B&W drawing | Tonal approach (hatching, stippling, wash, or mixed); reproduction medium (print, web, or scan for digital delivery); traditional tools brief |
| Greyscale digital | Same as painted work; note that Steps 06 and 07 merge — no separate colour pass |

**Sources:** Art Theory & Digital Practice Reference v5 (§1 — project initiation); manga-source-17.md (pipeline: Storyboard > Base > Inking > Finishing Details — each stage presupposes a clear brief for the page); manga-source-18.md (Step A: Script Writing — "Without a proper script, there will be no webtoon")

---

### Step 02 — Reference Gathering

**Purpose:** Build a visual evidence base before drawing. Reference prevents guesswork and anchors the image in observable reality or a consistent visual language.

**Primary outputs:** An organised reference board (PureRef, Pinterest, physical tearsheets, or software materials library) containing: observational reference, style reference, and any palette or mood reference. Reference type varies by medium.

**Governing fundamentals:** All fundamentals (observation phase — references all fundamental domains before commitment)

**Failure modes from skipping:**
- Invented anatomy, proportions, and surface materials that do not read as believable
- Inconsistent style register across a multi-image project (characters look like they come from different source materials)
- Over-referencing: copying a single reference too closely and losing original intent

**Medium variants:**

| Medium | Reference type |
|---|---|
| Painted work | Colour palette mood boards; photographic reference for realism; lighting reference; surface material reference (skin, metal, fabric, stone, organic) |
| Line art / inking | Inking style reference (line weight range, spotting-black density from published comics); pen nib and brush type examples; published inking by relevant artists |
| Manga | Screentone pattern samples; published manga page layouts for panel flow and reading rhythm; effect-line style examples (speed lines, focus lines, impact lines); nēmu (thumbnail stage) reference for pacing |
| Webtoon | Vertical scroll pacing examples; panel break timing from comparable webtoons |
| B&W drawing | Tonal range examples (what does the full value range look like in this technique?); hatching or stippling style reference; master draughtsmen work |
| Character/creature design | Silhouette sheets of comparable characters/creatures; material breakdown sheets (what surfaces does this subject have?) |

**Sources:** R4-source-9b.md (creature design: "For the initial research, I gathered a large collection of visual references in PureRef, focusing primarily on creature design and hard-surface armor from films and games. ArtStation and Pinterest were my main sources"); manga-source-16.md (paneling and page flow reference); manga-source-19.md (inking style reference)

---

### Step 03 — Thumbnailing & Composition

**Purpose:** Solve the largest structural problem — how the major shapes are arranged — at the smallest and cheapest scale. A bad composition caught here costs 30 seconds; caught during rendering it costs hours.

**Primary outputs:** A selected thumbnail (or selected nēmu for manga/comics). The thumbnail must answer: where is the focal point, what is the value distribution, and how does the viewer's eye move through the image. It must leave unresolved: colour, detail, surface.

**Governing fundamentals:** `fundamentals/composition.md`, `fundamentals/design-and-shape-language.md`

**Failure modes from skipping:**
- Focal point is either absent or competes with secondary elements
- Value distribution is unplanned, producing a flat image with no hierarchy
- Compositional problems discovered during rendering force a repaint of the entire base

**Medium variants:**

| Medium | Thumbnail requirements |
|---|---|
| Painted work (single image) | 3–7 value-blocked thumbnails (dark/mid/light shapes only, no detail); select one and commit |
| Line art (single image) | Compositional thumbnails with line weight hierarchy marked — which outlines will be heavy, which thin; silhouette shape planning |
| Comics (American, European) | Panel layout thumbnails: panel size hierarchy (larger panel = more important moment), gutter width, reading flow direction (left-to-right), page-turn reveal planning |
| Manga (Japanese, traditional or digital) | **Nēmu (ネーム) stage**: rough page layouts showing panel arrangement, character positions, reading direction (right-to-left), flow from panel to panel. Japanese editors review and approve the nēmu before full production begins. |
| Manga (Western-style) | Same as Comics above (left-to-right reading) |
| Webtoon | Vertical scroll pacing thumbnails: panels that function as tension-builders before a vertical cliff-hanger; no page-turn reveal — pacing is managed by the placement of the scene break within a long vertical strip |
| B&W drawing | Value thumbnail — where are the darkest areas, midtones, and brightest areas? Answer this before committing to a composition |

**Sources:** manga-source-16.md ("Begin with thumbnails to help visualize your story and move you through the page. Layout each panel individually, and as if they were all the same size. After that, decide your insets and big panels from there"); manga-source-17.md (nēmu as the first stage before Base); Ctrl+Paint library (source-academic-5.md): Section 4 "Composition Basics" — Compositional Framing Elements, Shadow Shape, Why Bother with Gesture Drawing — establishes thumbnail-scale composition as a separate stage before painting.

---

### Step 04 — Gesture / Silhouette

**Purpose:** Establish that any figure, creature, or mass reads clearly at a distance before any construction begins. A clear silhouette is the first test of a successful design.

**Primary outputs:** A gesture drawing (for figures, creatures) or a mass gesture (for environments, architecture) that passes the silhouette test — recognisable as a black shape at arm's length.

**Governing fundamentals:** `fundamentals/anatomy-and-gesture.md`, `fundamentals/form-and-construction.md`

**Failure modes from skipping:**
- Poses that look natural in construction but are ambiguous or limp in silhouette
- Character and creature designs that cannot be identified from their black shape alone — defeating the purpose of design
- Environment massing that has no clear directional energy

**Medium variants:**

| Medium | Gesture / silhouette requirements |
|---|---|
| Painted work — figures, characters, creatures | Gesture lines establish directional flow before construction. Silhouette test: view as black shape. |
| Painted work — environments, architecture | Mass gesture: the directional energy and dominant shape of the landscape or structure |
| Line art / comics | Silhouette is MORE critical than in painted work — there is no shading pass to clarify form. The pose and shape must communicate from the outline alone. Gesture shorthand in comics (exaggerated action, flowing capes and hair) is a visual convention that encodes emotion and motion, not physics. |
| Manga | Exaggerated gesture for dramatic effect; chibi proportions deliberately depart from realistic gesture to create a specific emotional register. Clothing, hair, and accessories function as gesture amplifiers. |
| B&W drawing | Silhouette test is the final authority when there is no colour to separate figure from ground |
| Creature / vehicle design | Silhouette uniqueness: can the creature or vehicle be identified from its black shape alone? This is a design criterion, not just an aesthetic preference. |

**Sources:** R4-source-9b.md (creature design: "pushed the proportions further by giving the character longer legs, very large hands with three fingers, and a larger overall body proportion... For one of the backlit shots, where the Alien appears mostly as a silhouette, I wanted to make its shape immediately feel more alien. The solution was to add an extra pair of arms, which gave the character a much more distinctive silhouette"); source-character-design-2.md (character design: "thumbnailing ideas. Rough thumbnails help to flesh out the many directions that the designer could take"); R1-source-3.md (Tyler James: "Tip 3: Have a minimum of 20 pieces demonstrating capable skills in design, anatomy, and materials/lighting")

---

### Step 05 — Perspective & Construction

**Purpose:** Place all forms convincingly in space. Perspective errors visible to a reader immediately destroy credibility; construction errors that look correct in 2D but fail in 3D are discovered at this step.

**Primary outputs:** A construction drawing or block-in where all major forms sit correctly in the established perspective. Ground plane and horizon line are established. Complex forms are built from basic primitives (box, cylinder, sphere).

**Governing fundamentals:** `fundamentals/perspective.md`, `fundamentals/form-and-construction.md`

**Failure modes from skipping:**
- Buildings and vehicles that feel unstable or "floating"
- Figures that cannot be placed in the environment because the ground plane is ambiguous
- Converging lines that are close but not correct — the eye detects this without being able to name it

**Medium variants:**

| Medium | Perspective / construction requirements |
|---|---|
| Painted work | Perspective guides inform the block-in layer; construction drawing is the skeleton for form rendering |
| Line art / comics | Perspective construction IS the final line art skeleton. There is no value rendering pass to correct misalignment, so vanishing point accuracy is more critical than in painted work. Rulers and perspective guides are standard tools. Backgrounds in comics use harder, more mechanical perspective than character linework. |
| Manga | Backgrounds are often simplified or stylised relative to character detail. "Open frame" technique: the background fades to white or is absent entirely, focusing all attention on the character. Speed-line backgrounds (radial perspective) are a visual convention for shock or impact — not technically correct perspective. Fish-eye lens distortion in wide-shot manga panels is a deliberate stylistic choice. |
| Webtoon | Vertical format changes how establishing shots are composed — wide establishing shots often appear at the top of a scroll segment before cutting to close character panels |
| B&W drawing | Perspective is the structural skeleton before any hatching is applied; construction lines in pencil work remain visible and inform ink line placement |
| Architecture / vehicles | These are the most perspective-critical subjects — ruled lines and accurate vanishing points are non-negotiable |

**Sources:** Ctrl+Paint library (source-academic-5.md): Drawing section — "Perspective Drills", "Perspective Drawing isn't Scary", "Horizon Line", "Perspective Sketching"; manga-source-16.md (panel perspective for establishing shots vs. close-ups); manga-source-17.md (background perspective in manga context)

---

### Step 06 — Value / Line Hierarchy

**Purpose:** Establish that the tonal or line-weight structure of the image is clear and hierarchical — the focal point has the highest contrast, secondary elements have medium contrast, and background elements have low contrast.

**Primary outputs:**
- **Painted / greyscale work:** A greyscale value study where the three value families (light, midtone, shadow) are clearly separated and the focal point has the highest contrast.
- **Line art / inking:** A line hierarchy plan — which lines are heavy (outlines of foreground forms, shadow sides), which are thin (highlight sides, secondary details, background elements).
- **B&W drawing:** A hatching direction and density plan — where the darkest and lightest areas sit before detail work begins.

**Governing fundamentals:** `fundamentals/light-and-value.md`

**Failure modes from skipping:**
- Painted work: no clear focal point; every area at the same contrast level; the eye has nowhere to rest
- Line art: all lines the same weight; image reads as flat and ambiguous; near and far objects are indistinguishable
- B&W drawing: shadow areas not planned; hatching applied randomly rather than building a coherent value structure

**Medium variants:**

| Medium | Value / line hierarchy method |
|---|---|
| Painted work (full colour) | Greyscale value study on a separate layer; value families separated (light, midtone, shadow, cast shadow, occlusion); hierarchy check: does the focal point have the highest contrast? |
| Greyscale digital painting | The greyscale render from this step IS the final tonal work. This step and Step 07 (Colour / Tone Pass) are merged. Step 07 does not apply for greyscale work. |
| Pure line art (black line on white) | Line hierarchy plan: foreground outlines heavy; highlight sides thin; background elements lightest. Light-direction encoding: thin lines toward the light source, thick lines away from it. Inking order: traditionally ink left-to-right to avoid smudging the wet ink with the drawing hand. |
| Manga | **Spotted blacks (ベタ / beta):** Deciding where to fill solid black before any screentone is applied. Rule of thumb: "when in doubt, black it out" for strong value contrast. Line weight variation as a proxy for light direction. Feathering (parallel lines thinning from thick to thin) to create smooth tonal gradation at shadow edges. |
| B&W drawing | Hatching direction and density map — deciding where the darkest and lightest areas sit before any detail hatching is applied |

**Sources:** lineart-source-6.md / manga-source-19.md (Scott Drummond, Marvel/Image Comics: "Spotted blacks: use black fills to show values; 'when in doubt, black it out'"; "Light source affects line weight: thin lines toward light, thick lines away"; "Feathering direction: start at thin point, pull INTO the black area"); manga-source-17.md (inking stage covers line hierarchy and beta placement); lineart-source-1.md (Wikipedia Line Art: hatching and stippling as value-building techniques)

---

### Step 07 — Colour / Tone Pass

**Purpose:** Apply colour or tonal values on top of the established value structure from Step 06. The value structure must be in place before colour or tones are applied — colour does not replace value; it sits on top of it.

**Primary outputs:**
- **Full colour work:** Colour applied to the greyscale value study. Colour hierarchy and temperature established.
- **Manga / comics with tones:** Screentone or hatching pass applying mid-tones.
- **Pure line art:** This step is SKIPPED. Document explicitly.

**Governing fundamentals:** `fundamentals/colour.md`

**Failure modes from skipping:**
- Full colour work where colour and value are resolved simultaneously: the image is harder to control, and value errors are masked until late in the process
- Tone pass that contradicts the value structure established in Step 06

**Medium variants:**

| Medium | Colour / tone pass method | Skip condition |
|---|---|---|
| Full colour painted work | Colour palette applied on the established value structure. Colour hierarchy: the most saturated or highest-contrast colour sits at the focal point. Colour temperature: warm light / cool shadow (or vice versa). Saturation hierarchy: background colours desaturated relative to foreground. | — |
| Greyscale digital painting | **MERGED WITH STEP 06.** The greyscale render from Step 06 is the complete tonal work. **SKIP Step 07 for greyscale work.** Sign-off condition: greyscale render complete, full value range present, focal point at highest contrast. | SKIP — no colour pass |
| Pure line art (black line on white, no tones) | **SKIP.** There is no tone pass in pure line art. Sign-off condition: confirm with user or brief that pure line art is the intended output. Document the skip explicitly on the Stage Sign-off Condition of pipeline/07-colour-tone-pass.md. | SKIP — no tone pass |
| Line art with hatching | Hatching pass for mid-tones — parallel or cross-hatch lines build grey values between the solid blacks and the white ground | — |
| Manga B&W screentone (traditional physical) | Cut-and-paste screentone sheets. Sheet selection by LPI (lines per inch) and dot density. Standard commercial manga screentones: 60 LPI. Dangerous combination to avoid: two screentone patterns at different angles applied on top of each other (moiré). | — |
| Manga B&W grey wash | Grey ink or diluted India ink applied by brush to create smooth grey tones. Alternative to screentone. | — |
| Manga digital screentone (Clip Studio Paint) | Apply screentone from material library to a selection. Adjust dot size, angle, and density. Use layer masks for non-destructive editing. Standard screentone angle: 45° for black to minimise moiré. Convert tone layers to dot patterns before print export. Verify dot density is within safe range for the target DPI. | — |
| B&W drawing (pencil / ink / charcoal) | Crosshatching for mid-tones. Parallel hatching vs. cross hatching produce different tonal depths. | — |

**Sources:** manga-source-17.md (screentone application: "digital screentone — apply to selection, customisable dot size, angle, density, convert to dot patterns for print"); manga-source-17.md / manga-summary.md (traditional screentone: adhesive sheets, cut to shape, press, trim, moiré awareness); lineart-source-1.md (hatching and stippling for tonal value in line art)

---

### Step 08 — Form & Materials

**Purpose:** Describe the surface of every major form — how it responds to light, what it is made of, and what that material looks like. Without material description, forms remain generic and unreadable.

**Primary outputs:** Forms with readable material surfaces. The viewer can identify skin, metal, fabric, stone, glass, or organic material without being told.

**Governing fundamentals:** `fundamentals/materials-and-texture.md`, `fundamentals/form-and-construction.md`, `fundamentals/light-and-value.md`

**Failure modes from skipping:**
- All surfaces look the same regardless of material
- Highlight and shadow placement is generic (applied as a convention, not as a response to the specific material type)
- The image looks "unfinished" even when it is technically complete — this is usually because material differentiation is absent

**Medium variants:**

| Medium | Material description method |
|---|---|
| Painted work | Diffuse gradients for matte surfaces (soft bounce light, no hard specular). Hard highlight placement for specular surfaces (metal, glass, wet, eyes). Subsurface scatter approximation for translucent materials (skin, wax, petals). |
| Line art / inking | **Hatching direction follows the surface form.** Curved lines on curved surfaces; straight lines on flat planes; cross-contour lines to show 3D form. Line density encodes material: loose open hatching = soft fabric; dense parallel hatching = metal; stippling = rough stone or skin; clean crisp outlines = smooth manufactured surfaces. |
| Manga | Screentone pattern selection varies by material. Solid black fills for glossy and dark materials (leather, hair, dark metal). Line texture in the ink layer (before screentones) reinforces material type. |
| B&W drawing | Hatching angle and density encode material. Soft surfaces: open curved hatching. Hard surfaces: sharp angular parallel lines. Charcoal: pressure and smudge for smooth gradation on material surfaces. |
| Creature design | Material heterogeneity is a design requirement — a creature with only one surface type reads as less believable than one with skin, scale, membrane, and claw as distinct materials |

**Sources:** R4-source-9b.md (80.lv creature character: "I used a combination of metal, carbon fiber, and rubber, with several emissive elements"; wear and dirt pass for believability; tertiary details to texturing stage for production efficiency); lineart-source-6.md (hatching direction for material description: curved on curved, straight on flat); manga-summary.md (screentone pattern selection for materials)

---

### Step 09 — Rendering & Detail

**Purpose:** Add the specific visual information that makes each surface area look like a real thing — not more lines or marks, but the right marks in the right places. Detail is hierarchical: the focal point receives the most; edges and background receive the least.

**Primary outputs:** A rendered image where the focal point is fully resolved, secondary areas are partially resolved, and the background remains loose. The viewer's eye is directed by detail density, not just by composition.

**Governing fundamentals:** `fundamentals/light-and-value.md`, `fundamentals/composition.md`

**Failure modes from skipping:**
- Flat rendering where every area is at the same level of detail — the eye has no reason to land anywhere
- Over-rendering: spending equal effort on background bricks and the protagonist's face
- Under-rendering: leaving the focal area at the same resolution as the rest of the image

**Medium variants:**

| Medium | Rendering method |
|---|---|
| Painted work | Hard edges at the focal point; softer edges at secondary areas; lost edges where two similar-value shapes meet. Edge control is the primary attention-direction tool. Selective detail: render the eye, not every eyelash. |
| Line art / inking | Rendering through **line density, line weight variation, and texture lines** — no grey values except those built from line work. Feathering (lines starting thick and tapering to thin) for smooth tonal transitions. Cross-contour lines to build form. Detail density marks importance: the focal point has the densest, most varied linework. Tool mixing: brush for major outlines, G-pen for detail, multiliner for manufactured surfaces. |
| Manga | **Effect lines** as rendering tools: speed lines (集中線) for motion and impact, focus lines (放射線) for emotional shock or emphasis, impact lines for collision. These are not decorative — they encode motion, emphasis, and emotional state. Screentone density variations: denser tone in shadow areas. White highlights added on top of dark areas (white ink traditionally; Add/Glow/Screen layers digitally). Detail hierarchy: the main character receives denser inking than background characters. |
| Webtoon | Detail hierarchy adapted for mobile reading: fine detail at close-up panels, simplified linework in establishing shots |
| B&W drawing | Rendering through hatching density — darkest shadow areas receive the densest crosshatching. Pencil pressure and layering for smooth tonal gradation. High contrast for print reproduction (no mid-grey smear that looks correct on screen but disappears in print). |

**Sources:** lineart-source-6.md / manga-source-19.md (Scott Drummond: feathering, spotted blacks, tool mixing — "Mix-and-match tools: Brush for outlines, G-pen for details, Multiliners for manufactured surfaces"); manga-source-17.md (effect lines, digital highlights, screentone density); manga-source-18.md (webtoon detail hierarchy for mobile reading)

---

### Step 10 — Atmosphere & Polish

**Purpose:** Add spatial depth cues and then execute a final consistency pass. Atmosphere makes the image read as having depth; polish removes errors and inconsistencies. Atmosphere is applied before polish, not after.

**Primary outputs:** An image with clear spatial depth cues and no visible technical errors or inconsistencies.

**Governing fundamentals:** `fundamentals/perspective.md` (atmospheric), `fundamentals/colour.md`, `fundamentals/light-and-value.md`

**Failure modes from skipping:**
- Images that read as flat even when all individual forms are correct — depth requires atmospheric cues, not just perspective geometry
- Polish applied before atmosphere: atmosphere adjustments after polish can undo polish work and force a second polish pass

**Medium variants:**

| Medium | Atmosphere and polish method |
|---|---|
| Painted work | **Atmospheric perspective:** distant objects go lighter in value, lower in contrast, cooler or more neutral in colour. In plain English: things far away look washed out because air and dust are between you and them. Depth of field simulation: foreground slightly soft, mid-ground sharpest, far background very soft. Global colour grading: a slight colour tint applied to the whole image so every element shares the same colour atmosphere. |
| Pure line art / inking | **Atmospheric perspective through line weight reduction in the distance.** Far objects: lighter, thinner lines. Background: less hatching density. Background elements: smaller line weight variation. |
| Comics | Background simplification to emphasise foreground character action. Reducing background detail in high-action panels. Atmospheric depth through reduced line density in the distance. |
| Manga | Background simplification as a deliberate stylistic choice. Tone density gradient: denser screentone in background pushes it back visually. Final clean-up pass: white-out corrections, stray line removal. White highlight pass: specular highlights added over dark areas in the final step. Glow effects via Add or Screen layers in digital manga. |
| B&W drawing | **Tonal range audit:** confirm that the image uses the full value range from near-white to near-black. A compressed tonal range produces a flat, muddy image. Final darkening of the deepest shadow areas. Final lifting of the lightest highlights (erasing in pencil, white ink in ink work). |

**Sources:** manga-source-17.md (finishing details stage including white highlights and clean-up); manga-source-18.md (final polish pass and export preparation); lineart-source-1.md (atmospheric line weight reduction principle)

---

### Step 11 — Critique, Revision & Export

**Purpose:** Evaluate the completed image against the brief, fix only what fails, and export at the correct technical specification. This step requires active distance from the image to see it clearly.

**Primary outputs:** A revised image that passes the brief check, exported at the correct resolution and file format for the intended use.

**Governing fundamentals:** All + `digital-practices/critique-methods.md`

**Failure modes from skipping:**
- Delivering an image that does not meet the brief
- Export at wrong resolution or colour space
- Over-revision: restoring problems that were already solved, or adding new work that was not in scope

**Medium variants:**

| Medium | Critique / export method |
|---|---|
| All mediums | **Self-critique:** flip test (mirror-flip to expose asymmetry); squint test (blur to see value distribution); step-away test (look away for 30 minutes, then look at the image fresh). Fix only what fails the brief. |
| Painted work | Colour check: is the focal area still the highest-contrast, most-saturated point? Edge check. Value check. **Export:** resolution per brief (72 DPI web, 300 DPI print minimum, 600 DPI for print with fine detail). File format: JPEG for web, PSD/TIFF for print, PNG for transparency. Colour space: sRGB for web, AdobeRGB or CMYK for print. |
| Pure line art / inking | Line quality audit: no stray marks, no unintentional bleeds, no broken lines. Line weight consistency check (a thick outline stays thick along its full length). **Export:** 600 DPI minimum for print, bitmap or greyscale mode. Anti-aliasing OFF for print (anti-aliased line art looks blurry when printed). TIFF for print, PNG for web. |
| Manga (traditional and digital) | Screentone moiré check: zoom to 100% and confirm that screentone dot patterns do not produce interference patterns. **Export for print:** 600 DPI, grayscale mode. **Export for webtoon:** RGB mode, 72–150 DPI, standard width 800px. Clip Studio Paint webtoon export: File > Special Export > Export Webtoon (EX version). Lettering check: all speech bubbles legible, no text clipping. Print bleed check for physical publication (B4 manuscript paper margin and bleed zones). |
| B&W drawing | Tonal range audit: confirm true blacks and bright whites (not just dark grey and light grey). Scan quality check for traditional work: 600 DPI greyscale for pencil; 1200 DPI bitmap for ink. Level adjustment post-scan to remove scan grey and restore true black-on-white. Export resolution matched to intended use. |

**Sources:** manga-source-18.md (export settings: "1600 x 20000 with at least 300 DPI in case I want to print; webtoon page size 800 x 1280 pixels"); manga-summary.md (600 DPI for print, 72–150 DPI for webtoon, moiré avoidance on screentone export); lineart-source-6.md (600 DPI canvas, export considerations for inking)

---

## Section 3 — Mapping to the 13-Stage Reference PDF

The `Art_Theory_Digital_Practice_Reference_v5.pdf` describes a 13-stage pipeline. The teaching assistant's 11-step pipeline is a deliberate simplification. The table below maps the 11 steps to the PDF stages and documents each simplification decision.

| Pipeline step | PDF stage(s) | Simplification notes |
|---|---|---|
| 01 — Brief & Ideation | Stage 1 (Project initiation / Brief), Stage 2 (Concept exploration) | PDF separates brief receipt from concept exploration into two stages. Merged here because for self-directed learners these are a single mental step. The separate stage is appropriate for professional studio contexts where the brief is given by a client. |
| 02 — Reference Gathering | Stage 3 (Research and reference) | Direct 1:1 correspondence. |
| 03 — Thumbnailing & Composition | Stage 4 (Thumbnail sketches) | Direct 1:1 correspondence. Expanded here to include manga nēmu as a distinct sub-variant. |
| 04 — Gesture / Silhouette | Stage 5 (Gesture and proportion) | Direct 1:1 correspondence. Expanded to cover silhouette uniqueness as a design criterion for creature and vehicle design. |
| 05 — Perspective & Construction | Stage 6 (Construction and perspective) | Direct 1:1 correspondence. |
| 06 — Value / Line Hierarchy | Stage 7 (Value / tonal study) | PDF frames this as a tonal study for painted work only. Renamed to "Value / Line Hierarchy" here to include line weight hierarchy planning for line art and manga as an equivalent operation. |
| 07 — Colour / Tone Pass | Stage 8 (Colour rough / colour study) | PDF does not address manga screentone or B&W tonal passes as variants of this stage. Extended here to cover all medium variants including the explicit SKIP condition for pure line art. |
| 08 — Form & Materials | Stage 9 (Block-in and material study) | PDF presents this primarily as a painted-work stage. Extended here to cover line-texture conventions for material description in inking and manga. |
| 09 — Rendering & Detail | Stage 10 (Rendering and detail pass) | Direct 1:1 correspondence for painted work. Extended to cover effect lines in manga and feathering in inking as equivalent rendering operations. |
| 10 — Atmosphere & Polish | Stages 11 and 12 (Atmospheric effects; Final adjustments) | PDF separates atmosphere from final adjustments. Merged here as they are executed in sequence without a formal break. Atmosphere is addressed before final polish in both the PDF and this pipeline. |
| 11 — Critique, Revision & Export | Stage 13 (Review, revision, and delivery) | Direct 1:1 correspondence. Expanded here to document medium-specific export specifications (moiré check, 600/1200 DPI, webtoon export). |

---

## Section 4 — Gap Analysis Summary

The following art types and mediums were absent from the original pipeline definition (before 2026-10-02 scope expansion) and have been incorporated at each applicable step.

| Gap identified | Step(s) affected | Resolution |
|---|---|---|
| Line art / inking (all types) | 01, 03, 04, 05, 06, 07, 08, 09, 10, 11 | Medium variant added to every applicable step. Step 07 includes explicit SKIP condition for pure line art. |
| Manga (traditional and digital) | 01, 03, 04, 05, 06, 07, 08, 09, 10, 11 | Manga-specific variants added. Step 03 includes nēmu stage detail. Step 07 covers screentone (traditional and digital) with moiré avoidance. Step 11 covers moiré check and webtoon export. |
| Webtoon (vertical scroll format) | 01, 03, 09, 10, 11 | Webtoon variants added where they differ materially from standard comics. |
| B&W drawing (pencil / ink / charcoal) | 01, 06, 07, 08, 09, 10, 11 | B&W variants added to every applicable step. |
| Greyscale digital painting | 06, 07 | Step 06 and 07 merge documented explicitly for greyscale work. |
| Comics (American, European) | 03, 04, 09 | Panel layout, gesture shorthand, and effect line conventions added. |
| Creature design (silhouette as design criterion) | 04, 08 | Silhouette uniqueness added as an explicit design criterion at Step 04. Material heterogeneity added at Step 08. |

---

## Section 5 — Sources

All sources below were retrieved and are held in `docs/research/`. URL verifiability confirmed at time of research (2026-10-02).

| # | Source | URL | Held at | Relevance |
|---|---|---|---|---|
| 1 | "The Difference Between Digital Manga and Hand-Drawn Manga" — Art Rocket (Celsys/Clip Studio Paint). Author: Ishida Wakako. | https://www.clipstudio.net/how-to-draw/archives/155309 | `docs/research/manga/manga-source-17.md` | Manga creation pipeline: Storyboard > Base > Inking > Finishing Details; pen tools (G-pen, Mapping pen, Turnip pen); screentone; effect lines |
| 2 | "How to Make a Webtoon Page: Complete Guide & Video Tutorial" — Art Rocket. Author: Obliviousquill. | https://www.clipstudio.net/how-to-draw/archives/172579 | `docs/research/manga/manga-source-18.md` | Webtoon creation pipeline A-to-Z: script → character sheets → thumbnailing → speech bubbles → paneling → line art → flat colours → rendering → backgrounds → final touches → export; canvas and DPI specifications |
| 3 | "Pro Artist's Guide to Comic & Manga Layouts, Paneling, Flow" — Art Rocket. Author: Steve Ellis (Marvel/DC). | https://www.clipstudio.net/how-to-draw/archives/160963 | `docs/research/manga/manga-source-16.md` | Panel thumbnailing, panel types, gutter, reading flow, page-turn planning |
| 4 | "Inking Superhero Comics in Clip Studio Paint" — Art Rocket. Author: Scott Drummond (Marvel/Image Comics). | https://www.clipstudio.net/how-to-draw/archives/159080 | `docs/research/manga/manga-source-19.md` | Professional inking techniques: brush/G-pen/multiliner, spotted blacks, feathering, line weight for light direction, 600 DPI canvas |
| 5 | Wikipedia — "Line art". | https://en.wikipedia.org/wiki/Line_art | `docs/research/lineart/lineart-source-1.md` | Definition of line art; hatching and stippling as tonal value techniques; contour line function; pre-photography print history |
| 6 | Ctrl+Paint Free Video Library (Matt Kohr — "Digital Painting Simplified"). | https://www.ctrlpaint.com/library | `docs/research/source-academic-5.md` | Structured digital painting curriculum establishing canonical topic progression: Traditional Drawing → Drawing 2 → Composition Basics → Digital Tools → Painting Techniques → Colour → Texture → Full Studies |
| 7 | "Creating an Alien Character for a Sci-Fi Short Film with Blender & Substance 3D" — 80.lv. Artist: Artur Ledur (3D Character Artist, FornoFX). | https://80.lv/articles/creating-an-alien-character-for-a-sci-fi-short-film-with-blender-substance-3d | `docs/research/R4-source-9b.md` | Professional character/creature production workflow: reference gathering (PureRef), blockout, design decisions (silhouette, proportions), retopology, texturing (material building, wear pass), lighting (IBL, HDRI), one-week production timeline and prioritisation |
| 8 | Art Theory & Digital Practice Reference v5 (internal corpus). | — | `Art_Theory_Digital_Practice_Reference_v5.pdf` | 13-stage pipeline; classical and modern art theory; failure-mode table (§8); quality-check protocol (§7) |

---

## Owner Confirmation Required

This document is a **DRAFT**. Before any pipeline step file (#7–#17) is written, the owner must review this document and record confirmation in a comment on GitHub issue #36.

**Confirmation statement required on issue #36:**
> "I confirm the 11-step pipeline structure and scope in `docs/specs/pipeline-definition.md` as written on [date]. Issues #7–#17 are unblocked."

No agent may start writing any pipeline step file until that comment exists on issue #36. This is the gate that was bypassed before commit `ba4df99` and which caused the rollback.
