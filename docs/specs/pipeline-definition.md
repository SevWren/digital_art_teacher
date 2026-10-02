# Pipeline Definition — Confirmed Specification

**Date confirmed:** 2026-10-02
**Status:** Revised — Scope expanded and line art / manga / B&W variants fully documented (hold response 2026-10-02)
**Blocks:** Issues #7–#17 (pipeline step files may now be written — pending owner confirmation)
**Gap analysis:** `docs/specs/pipeline-gap-analysis.md`
**Primary line art / manga research:** `docs/research/grok/` (3 documents, 30+ sources, 6 pipeline variants)
**Sources:** 14 independent professional sources — see Section 5

> **Owner confirmation required.** Pipeline step files (#7–#17) must NOT be started until the owner has confirmed the structure in a comment on GitHub issue #36.

---

## 1. Confirmed Pipeline Structure

The pipeline consists of **11 steps** in the following sequence. Steps apply to all covered art types and mediums. Where the execution differs by medium, the step specification (Section 2) documents the exact variant.

| # | Step name | Primary question answered | Governing fundamental(s) |
|---|---|---|---|
| 01 | Brief & Ideation | What must this image achieve and for whom? | Design / Shape language, Composition |
| 02 | Reference Gathering | What visual evidence do I need? | All fundamentals (observation) |
| 03 | Thumbnailing & Composition | What is the strongest arrangement of major shapes and panels? | Composition, Design |
| 04 | Gesture / Silhouette | Does the pose or major form read clearly at a distance? | Anatomy & Gesture, Form |
| 05 | Perspective & Construction | Do the forms sit convincingly in space? | Perspective, Form & Construction |
| 06 | Value / Line Hierarchy | Is the light design (or line weight plan) clear and hierarchical? | Light & Value |
| 07 | Colour / Tone Pass | Do the colours or tones support hierarchy and mood? | Colour |
| 08 | Form & Materials | Do surfaces respond correctly to the light? | Materials & Texture, Form |
| 09 | Rendering & Detail | Where does the eye rest and where does it travel? | Composition, Light & Value |
| 10 | Atmosphere & Polish | Are depth, focus, and final adjustments coherent? | Perspective (atmospheric), Colour, Light |
| 11 | Critique, Revision & Export | Does the image meet the brief and technical requirements? | All + Critique methods |

---

## 2. Per-Step Specifications

Each step includes a **Medium variants** block where the execution differs meaningfully by medium. "Painted" covers all colour and greyscale digital or traditional painted work. "Line art / comics" covers pen-and-ink illustration in any style. "Manga" covers both traditional (analog paper + tools) and digital manga production. "B&W drawing" covers pencil, charcoal, and similar tonal drawing media.

---

### Step 01 — Brief & Ideation

**Purpose:** Establish a clear, written goal for the image before any visual production begins. For illustration: the client brief, intended use, and visual direction. For manga and comics: the story concept, characters, panel script or notes, and visual style references.

**Primary outputs:**
- Written brief: who will see the image, what it must achieve, what the single most important visual element is
- At least two directional approaches explored before one is chosen
- *For manga (consumer):* story outline, characters, rough plot, and panel-by-panel script or detailed notes including dialogue and key actions
- *For manga (commercial):* story concept and sample pages submitted to editor; detailed plot outline and character designs locked after editorial approval

**Failure modes from skipping:**
- Image drifts mid-production with no written reference point to return to
- For manga: character inconsistencies across pages because no reference sheets were locked
- For commercial work: scope creep and unbounded revision cycles

---

### Step 02 — Reference Gathering

**Purpose:** Collect visual evidence for every claim the image makes. For line art and manga, reference includes anatomy, architecture, props, clothing, and gesture sources that the inking will interpret — not copy.

**Primary outputs:**
- Reference set covering: subject anatomy and proportions; lighting situation; materials and surfaces; environment
- *For manga / comics:* character reference sheets (front/side view, expression studies) locked before penciling begins — required for consistency across pages in sequential work
- *For commercial work:* style references from client brief incorporated

**Failure modes from skipping:**
- Anatomy and proportions drift toward approximations
- For manga: character proportions change between pages because no locked reference sheet exists

---

### Step 03 — Thumbnailing & Composition

**Purpose:** Explore arrangement options at small scale before committing to full-size work. For manga and comics, this step is the layout/storyboard phase — the most important decision point in sequential narrative work.

**Medium variants:**

- *Painted illustration:* Coin-sized or postage-stamp-sized rough sketches testing dark/light shape arrangement. Select the strongest before scaling up.

- *Line art / single-image comics:* Same as painted — rough shapes testing composition and silhouette hierarchy before inking begins.

- *Manga (consumer / doujinshi):* Produce the **nēmu** (also called "name" — rough storyboard). Rough page layouts on scrap paper showing panel divisions, character placement as stick figures, balloon positions, pacing, and reading flow. Multiple iterations until narrative flow feels correct. No detailed rendering at this stage.

- *Manga (commercial / professional):* Produce the **name** — a complete rough page-by-page storyboard with panels, rough figures, dialogue, and pacing. **Submit to editor for approval before penciling begins.** This is the primary revision stage. Major changes happen here; changes after inking are expensive.

- *Sequential / panel-based work (all):* Panel layout, gutter width, reading order (left-to-right for Western; right-to-left for Japanese manga), and eye-flow path are all established at this step before any character drawing occurs.

**Primary outputs:**
- A set of rough layouts / thumbnails
- One approved layout confirmed before proceeding to Step 04
- *For commercial manga:* editor sign-off on the name before penciling begins (documented in issue or communication record)

**Failure modes from skipping:**
- For manga: narrative pacing problems discovered after inking, requiring full page redraws
- For illustration: composition chosen by default rather than by selection from options

---

### Step 04 — Gesture / Silhouette

**Purpose:** Establish the overall action, weight, and readable outer form of every figure, creature, or major object before internal construction begins. For manga and comics, silhouette legibility is particularly critical because print at small sizes eliminates internal detail — the outer shape must carry the reading.

**Medium variants:**

- *All media:* The gesture pass is identical regardless of medium. The first mark for any figure is the whole-body action line — one flowing stroke before any individual part. For objects: the outermost bounding shape established first.

- *Line art / manga / comics specific:* Silhouette legibility test is especially important. At inking stage, the outer contour is the thickest line in the drawing. If the silhouette is vague or self-merging (arm blends with body, overlapping limbs become unreadable), no amount of internal hatching will fix it.

**Primary outputs:**
- Gesture or major form roughed in at full working size (loose; no detail)
- Silhouette test passed: outer shape reads clearly as a distinct blob when squinted at

---

### Step 05 — Perspective & Construction

**Purpose:** Build the underlying geometric structure confirming all forms sit convincingly in three-dimensional space. For line art and manga, this is the **detailed pencil underdrawing** (penciling stage) — the structural foundation the inking will trace.

**Medium variants:**

- *Painted work:* Block in major objects as simple geometry (boxes, cylinders, spheres). Fix structural problems at this stage, not after rendering.

- *Traditional analog line art / comics (consumer):* Transfer or redraw the chosen thumbnail composition at final size using light graphite (H or 2H pencil, or non-photo blue). Establish construction lines, proportions, perspective, major contours, and key internal structures. Keep lines light and structural — not detailed. Optional subject studies on scrap paper for complex forms.

- *Traditional analog line art / comics (commercial):* Transfer approved thumbnail sketch to final art surface (illustration board or heavy Bristol) using light graphite or non-photo blue. Construction is precise and production-ready. Client approval of the pencil stage is a formal gate before inking begins.

- *Traditional analog manga (consumer):* Transfer nēmu to final manga manuscript paper (genkō yōshi or equivalent B4/A4 with printed panel guides). Draw accurate panel borders with ruler. Detailed graphite (or non-photo blue) drawings of characters, backgrounds, props, and dialogue balloons. Focus on anatomy, perspective, and composition.

- *Traditional analog manga (commercial):* Mangaka draws full-size pencil underdrawing. Assistants may begin backgrounds. Panel borders, balloons, and key elements precisely placed. Optional editorial review at this stage for complex chapters.

- *Digital (all types):* Rough sketch layer (often blue or low-opacity grey pencil brush). Establish construction, proportions, and composition. Multiple refinement layers common (rough → tighter sketch). Perspective tools, rulers, and reference overlays available.

**Primary outputs:**
- Full-size construction drawing or underdrawing on working surface (paper or digital canvas)
- Perspective consistent throughout
- All forms at correct scale relative to each other
- Nothing floating, leaning incorrectly, or off-scale

---

### Step 06 — Value / Line Hierarchy

**Purpose:** In painted work: design the light-and-dark structure in greyscale before any colour. In line art and manga: plan and establish which lines carry heavy weight (indicating shadow sides, foreground edges, and focal contours) and which carry thin weight (indicating lit sides, secondary lines, and background detail). Both are equivalent operations — both encode where visual emphasis falls before surface detail is added.

**Medium variants:**

- *Painted work:* Produce a greyscale value study. Light source established: direction, intensity, type. Clear value hierarchy — focal area has highest contrast. Image squint-test: major shapes read clearly without colour.

- *Traditional analog line art (consumer and commercial):* **Line hierarchy planning** — decide before inking which lines receive heavy weight (main contours, foreground edges, focal outlines) versus thin secondary lines (interior details, textures, backgrounds). Two distinct uses of line weight:
  1. **Light-direction encoding:** thin lines on surfaces facing the light source; thick lines on surfaces facing away. This indicates three-dimensional form and a consistent light direction.
  2. **Outline emphasis:** heavier lines for foreground subjects and focal elements; thinner lines for background and secondary elements. This creates depth hierarchy independent of lighting.
  Both approaches are valid and are often combined.
  For commercial work: inking order is planned to avoid smudging — typically large forms first, then secondary details, then textures and hatching last.

- *Digital line art:* Choose pen tool with pressure sensitivity. Plan vector vs. raster layers — vector preferred for editable line weight and scalability. The line weight hierarchy decision is the same as analog; the execution uses brush pressure curves and post-edit width tools.

- *Manga (all):* Spotted blacks (solid filled black areas, called **beta** in Japanese production) are placed on the shadow sides of forms and in large dark areas. Spotted blacks encode the same value information that flat dark paint would encode — they are not decoration. Planning their placement before inking begins is the equivalent of the painted value study.

**Primary outputs:**
- *Painted:* Greyscale value study that squint-tests cleanly
- *Line art / manga:* Line hierarchy plan confirmed; spotted black placement decided; inking order determined

---

### Step 07 — Colour / Tone Pass

**Purpose:** Apply colour (for full-colour work) or tonal indication (for B&W work) in a way that supports the value hierarchy from Step 06. Tone or colour adds mood, atmosphere, and material identity.

**Medium variants — no ambiguity:**

| Medium variant | What happens at Step 07 | Key constraints |
|---|---|---|
| Full colour | Colour palette applied on top of greyscale value study. Grey version kept visible for comparison to confirm value hierarchy is preserved. | Highest saturation reserved for focal area |
| Greyscale painted | Step 07 merges into Step 06 — greyscale rendering pass is the complete tonal work | No separate colour pass |
| **Pure line art (no tones)** | **Step 07 is SKIPPED.** Line weight and spotted blacks from Step 06 carry all value information. | No hatching, no screentone, no grey fill added |
| **Line art with hatching** | Hatching pass: parallel lines drawn over shadow areas to create mid-tones. Works from Step 06 spotted blacks outward. | Hatching direction follows surface curvature (wrap-around lines); uniform line spacing = uniform tone |
| **Line art with crosshatching** | Crosshatching pass: two or more sets of parallel lines at different angles overlay for darker mid-tones. Added in layers on top of single hatching. | Each layer darkens the area; use to distinguish material textures |
| **Traditional analog manga (consumer)** | Adhesive screentone sheets applied: cut to shape, burnished flat onto the paper. Scratching or cutting creates gradients or special effects. Speed lines, impact effects, and solid blacks added as needed. | Consumer flexibility: can skip tones entirely; no LPI constraints |
| **Traditional analog manga (commercial)** | Same screentone application as consumer. **Critical constraint:** screentone density (LPI — lines per inch) must be chosen to avoid moiré when the page is photographically reproduced or printed at the final reduced size (typically B5 or smaller). Coarser screentones (lower LPI) are safer for heavy printing reduction. | Editor final check for clarity and continuity at this stage |
| **Digital manga / comics** | Digital screentone layers or dot-pattern fills on dedicated layers. Density control adjustable. Layer masks used for clean edges. Print-safe density must still be verified for commercial work. Speed lines, effect tones, and solid fills on separate layers. | Non-destructive: all on layers, nothing flattened until delivery |
| **B&W drawing (pencil/pen)** | Hatching and crosshatching. Same principles as line art with hatching. Pencil additionally allows smudging/blending for soft tones. | Pencil: blendable; pen and ink: not blendable, rely on line density only |

---

### Step 08 — Form & Materials

**Purpose:** Add surface information that distinguishes materials and reinforces three-dimensional form. In painted work: painted light response. In line art: hatching direction, line density, and texture strokes.

**Medium variants:**

- *Painted work:* Surface response to light — shiny surfaces have sharp highlights; rough surfaces scatter light; skin subsurfaces are soft.

- *Line art / comics (traditional and digital):* Hatching indicates material:
  - Close parallel lines = dark, smooth surface
  - Crosshatching = rough or heavily textured surface
  - Spaced parallel lines = mid-tone smooth surface
  - Stippling (dots) = soft texture, skin, stone
  - Line direction follows the surface curve — lines that wrap around a cylinder confirm it is cylindrical, not flat
  - Feathering (lines going from thin to thick) is used at shadow edges — always pulled FROM the thin outer edge INTO the spotted black area, not outward from the black. Outward-pulled feathering produces inconsistent line ends.

- *Manga:* Screentone pattern selection distinguishes materials — fine dot patterns for skin, coarser patterns for fabric, diagonal line patterns for shadow areas. Combined with hatching or G-pen work for emphasis.

- *B&W drawing:* Hatching, crosshatching, and stippling carry all material information.

**Failure modes from skipping:**
- All surfaces look like the same uniform black-and-white with no material identity
- Light direction is not readable from the surface treatment

---

### Step 09 — Rendering & Detail / Final Inking

**Purpose:** Apply fine detail selectively at the focal point. In painted work: texture, edge sharpening. In line art and manga: the clean final inking pass, with detail concentrated at focal areas.

**Medium variants:**

- *Painted work:* Fine texture, edge sharpening at focal point, soft lost edges at periphery.

- *Traditional analog line art — inking pass (consumer and commercial):*
  Execute final permanent ink lines over the pencil underdrawing using chosen tools (dip pens with G-nib, mapping nib, or crow-quill; technical pens/fineliners; brush pens).
  **Systematic inking order to prevent smudging:**
  1. Main contours first
  2. Large interior shapes
  3. Secondary details
  4. Textures and hatching last
  Vary pressure and angle for expressive line weight. For mistakes: white correction fluid or opaque white applied after drying. Erase remaining graphite once ink is fully dry. Reinforce weak lines; add final spotted blacks where planned.
  *Commercial:* Consistent, reproducible line quality required for printing reproduction. Corrections minimized.

- *Traditional analog manga — inking:*
  Mangaka inks primary figures and key elements using G-pen (flexible, variable weight) and mapping pen (fine details). Assistants handle panel borders, simple backgrounds, mechanical details, and some spotted blacks.
  After inking: erase pencils once ink dries; apply white correction fluid for fixes; spot-check all panel borders are ruled cleanly.

- *Digital line art / manga — clean line pass:*
  New vector or dedicated raster layer above sketch. Deliberate strokes using pressure-sensitive pen with configured stabilization. Undo freely. Adjust line weight via pressure or post-edit width tools. For manga: transparent swatch technique — use the inking brush in eraser mode (transparent color) to carve back into inked areas while preserving ink texture, rather than using a plain eraser (which may not match brush texture). Separate layers for different elements (character lines vs. background lines) for collaborative work.

- *Commercial digital manga:*
  Vector or high-resolution raster line layers. Professional brush settings emulate G-pen or mapping-pen behavior. Assistants may receive separate layer files or cloud-shared documents for backgrounds.

**Export resolution note:** For commercial print line art and manga, minimum **600 DPI** (dots per inch) in monochrome or greyscale mode. Consumer personal work: 300 DPI minimum for print potential.

---

### Step 10 — Atmosphere & Polish

**Purpose:** Final adjustments for unity, depth, and coherence. For painted work: atmospheric depth, colour unity. For line art and manga: cleanup pass, final spotted-black consistency check, overall value balance review.

**Medium variants:**

- *Painted work:* Atmospheric perspective (far objects lighter and less saturated), colour unity pass, thumbnail re-check.

- *Line art / comics (traditional):* Cleanup pass — erase all remaining graphite once ink is fully dry. Optional light spray fixative to protect the surface. Final check: are all spotted blacks consistently dark? Are any lines too thin (will drop out in printing)? Are there accidental tangents (shapes that just barely touch an edge)?

- *Line art / comics (digital):* Hide or delete sketch/underdrawing layer. Clean stray marks. Final zoomed review and flipped view check (reversal reveals problems invisible in normal orientation). Adjust contrast if needed.

- *Manga (consumer):* Check overall readability, contrast, and consistency across all pages. Verify screentone edges are burnished cleanly (no lifting corners for analog). Optional light cleanup.

- *Manga (commercial):* Internal quality check against print simulation (if digital) or at final print scale (if traditional). Verify screentone density is print-safe. Editor or internal quality check before manuscript delivery.

---

### Step 11 — Critique, Revision & Export

**Purpose:** Check the finished work against the original brief. Make required revisions. Export at technical specifications appropriate for the intended output.

**Export specifications by medium and context:**

| Context | Resolution | Format | Colour mode | Notes |
|---|---|---|---|---|
| Consumer personal digital | 300 DPI minimum | PNG, TIFF, or PSD with layers | RGB or greyscale | Personal preference; no external specification |
| Commercial illustration (digital) | 300–600 DPI (as specified by client) | TIFF or PSD; flattened plus layered masters | CMYK or greyscale | Bleed included if specified; usage license documented |
| Commercial line art (digital) | 600+ DPI | TIFF or flattened PNG | Monochrome (1-bit) or greyscale | Client brief specifies file organisation requirements |
| Commercial line art (traditional analog) | 600+ DPI scan of original | TIFF or greyscale JPG | Greyscale or monochrome | Physical original retained by artist unless buyout agreed |
| Consumer manga (personal / doujinshi) | 300–600 DPI | PNG or TIFF | Greyscale or monochrome | Ready for photocopying, scanning, or small-run printing |
| Commercial manga (digital) | 600+ DPI | Layered working files + flattened high-res finals | Monochrome (1-bit black-and-white) | Publisher pre-press pipeline receives files; typically printed reduced to B5 magazine or tankōbon size |
| Commercial manga (traditional analog) | Publisher handles scanning after manuscript delivery | Physical pages submitted to publisher by deadline | — | Publisher handles further cleanup, typesetting, and printing; originals archived by artist |

**Brief check:**
Before export, verify the finished work achieves the goal stated in Step 01. For manga: verify the pages achieve the narrative goal described in the name/nēmu.

**Revision note:**
- *Consumer work:* Revisions are personal and unconstrained.
- *Commercial illustration:* Revisions are limited to contracted rounds; major revision requires negotiation.
- *Commercial manga:* Major revisions to penciled or inked pages are expensive; the name/nēmu approval gate (Step 03) is where large changes should occur.

---

## 3. Scope Statement

This pipeline applies to the following, with no ambiguity about inclusion or exclusion.

---

### Art types covered

- Digital illustration (single images)
- Character art (figures, portraits, character design sheets)
- Environment art (landscapes, interiors, architectural illustration)
- Creature design
- Manga (Japanese-style sequential comic art) — consumer and commercial
- Comics / graphic novels (Western style, BD/European style)
- Line art illustration (pen-and-ink, brush-and-ink, technical illustration)
- B&W drawing (pencil, charcoal, pen-and-ink, stipple)
- Webtoon / digital scroll-format comics

### Art types NOT covered

- 3D modelling (beyond its use as a 2D painting underlay)
- Motion / animation
- Photography
- Lettering and typesetting (covered by separate production workflows outside this pipeline)
- Panel scripting / writing (Stage 01 covers the brief; the full scriptwriting process is not a visual art pipeline stage)

---

### Workflow types covered

- Traditional analog only (paper + physical tools, all stages)
- Digital only (all stages in software)
- Hybrid: traditional pencil underdrawing scanned and inked digitally
- Hybrid: digital sketch printed as blue-line reference and inked traditionally
- Traditional-to-digital finish (pencil/ink on paper, then scanned and tones/colour applied digitally)

### Mediums and how the pipeline adapts

See Step-level **Medium variants** sections in Section 2 above for precise detail.

Summary table:

| Medium | Step 06 | Step 07 | Step 08 | Step 09 | Step 11 export |
|---|---|---|---|---|---|
| Full colour painted | Greyscale value study | Colour pass | Painted surface response | Painted detail | 300+ DPI, RGB/CMYK |
| Greyscale painted | Value study (merges into Step 07) | Greyscale render | Greyscale surface detail | Greyscale detail | 300+ DPI greyscale |
| Pure line art (no tones) | Line weight + spotted blacks | **SKIPPED** | Hatching / crosshatching | Final inking pass | 600+ DPI monochrome |
| Line art with hatching | Line weight plan | Hatching pass | Additional hatching for materials | Fine hatching at focal | 600+ DPI monochrome/greyscale |
| Manga B&W (screentone) | Line weight + spotted blacks | Screentone placement (LPI-aware for commercial) | Screentone material patterns | Final inking + detail | 600+ DPI monochrome |
| Manga grey wash | Line weight + grey wash | Grey wash tones applied | Wash + ink material detail | Final inking | 600+ DPI greyscale |
| B&W drawing (pencil) | Hatching for value structure | Crosshatching for mid-tones | Texture hatching / stippling | Fine stippling at focal | 300–600 DPI greyscale |
| Colour manga | Screentone + line weight | Colour pass | Colour + material response | Colour + inking detail | 600+ DPI, RGB or CMYK |

---

### The six pipeline variants and their mapping

The Grok research (docs/research/grok/) documents six discrete pipeline variants. The table below shows how each variant maps to the 11 steps. Stage names in quotes are the terms used in those documents.

| Grok stage | Grok variant | Maps to pipeline step |
|---|---|---|
| "Concept and Planning" | All 6 variants | Step 01 |
| "Brief, Scope, and Contract" | Commercial variants | Step 01 |
| "Thumbnail Exploration" | Consumer line art | Step 03 |
| "Concept Exploration / Thumbnails" | Commercial line art | Step 03 |
| "Nēmu / Name (Storyboard)" | All manga variants | Step 03 |
| "Name — editor submission" | Commercial manga | Step 03 (with editorial gate) |
| "Refined Pencil Underdrawing / Construction" | Analog line art | Step 05 |
| "Final Pencil Underdrawing" | Commercial analog | Step 05 |
| "Penciling (Detailed Underdrawing)" | Manga analog | Step 05 |
| "Rough Sketch / Construction layers" | Digital variants | Step 05 |
| "Line Hierarchy Planning" | All line art variants | Step 06 |
| "Line Hierarchy and Stabilization Setup" | Digital line art | Step 06 |
| "Inking / Final Line Application" | Analog line art | Steps 06 + 09 (value plan then execution) |
| "Inking" | All manga variants | Steps 06 + 09 |
| "Clean Line Art" | Digital line art | Step 09 |
| "Screentoning / Finishing" | Manga analog | Step 07 |
| "Toning, Effects, Lettering" | Commercial manga | Step 07 |
| "Tonal treatment" | Commercial line art | Step 07 or 08 |
| "Cleanup and Finishing" | Analog line art | Step 10 |
| "Cleanup, Effects, Finishing" | Digital line art | Step 10 |
| "Review and Archival" | Consumer variants | Step 11 |
| "Delivery and Archival" | Commercial variants | Step 11 |
| "Export and Archival" | Digital variants | Step 11 |

---

## 4. Mapping to 13-Stage Reference PDF

The reference PDF (`Art_Theory_Digital_Practice_Reference_v5.pdf`) describes 13 stages. The pipeline uses 11 via the following deliberate simplifications:

| Reference PDF stages | Pipeline step | Simplification |
|---|---|---|
| Stages 1–2: Client brief + Creative exploration | Step 01: Brief & Ideation | Merged |
| Stages 3–4: Reference/research + Mood board | Step 02: Reference Gathering | Merged |
| Stages 5–6: Composition + Rough sketches | Step 03: Thumbnailing & Composition | Merged; includes manga nēmu |
| Stage 7: Gesture / silhouette | Step 04: Gesture / Silhouette | 1:1 |
| Stage 8: Form construction | Step 05: Perspective & Construction | 1:1; includes penciling stage |
| Stage 9: Value / lighting | Step 06: Value / Line Hierarchy | 1:1; expanded to include line hierarchy planning |
| Stage 10: Colour | Step 07: Colour / Tone Pass | 1:1; expanded to include tone variants |
| Stage 11: Surface / materials | Step 08: Form & Materials | 1:1; includes hatching/screentone material indication |
| Stage 12: Rendering and detail | Step 09: Rendering & Detail / Final Inking | 1:1; includes final inking pass |
| Stage 13: Final polish + critique + export | Steps 10 + 11 | Split; includes medium-specific export specs |

Net: 13 → 11 via 3 merges, 1 split, 1 expansion.

---

## 5. Sources

**Original 10 sources (from gap analysis):**

1. Wikipedia. "Concept Art." https://en.wikipedia.org/wiki/Concept_art — Retrieved 2026-10-02.
2. CGSpectrum. "Concept Artist Job Description, Salary, Skills & Software." https://www.cgspectrum.com/blog/what-is-concept-art — Retrieved 2026-10-02.
3. CGSpectrum / professional artist interview. "How to Become a Concept Artist." https://www.cgspectrum.com/blog/what-it-is-like-to-be-a-professional-concept-artist — Retrieved 2026-10-02.
4. Rhode Island School of Design (RISD). "Illustration Courses." https://www.risd.edu/academics/illustration/courses — Retrieved 2026-10-02.
5. Ctrl+Paint (Matt Kohr). "Free Video Library." https://www.ctrlpaint.com/library — Retrieved 2026-10-02.
6. Wikipedia. "Digital Painting." https://en.wikipedia.org/wiki/Digital_painting — Retrieved 2026-10-02.
7. Artur Ledur / FornoFX via 80.lv. "Creating Alien Character for Sci-Fi Short Film with Blender." https://80.lv/articles/creating-an-alien-character-for-a-sci-fi-short-film-with-blender-substance-3d — Retrieved 2026-10-02.
8. Wikipedia. "Line Art." https://en.wikipedia.org/wiki/Line_art — Retrieved 2026-10-02. Covers hatching, stippling, screentone techniques.
9. Scott Drummond via Clip Studio Art Rocket. "Inking Superhero Comics in Clip Studio Paint." https://www.clipstudio.net/how-to-draw/archives/156630 — Retrieved 2026-10-02. Professional inking workflow: pencil rough → brush/G-pen/multiliner → line weight for light → spotted blacks → feathering → 600 DPI export.
10. Clip Studio Art Rocket. "The Difference Between Digital Manga and Hand-Drawn Manga." https://www.clipstudio.net/how-to-draw/archives/155309 — Retrieved 2026-10-02. Canonical manga workflow: Storyboard → Base → Inking → Finishing Details.

**Additional sources from Grok line art research (selected verifiable URLs):**

11. VIZ Media. "Manga Creation 101." https://www.viz.com/blog/posts/manga-creation-101 — Retrieved 2026-10-02. Publisher-side documentation of professional manga production stages.
12. CGSpectrum. "The 5 Stages of Digital Illustration." https://www.cgspectrum.com/blog/5-stages-of-digital-illustration — Retrieved 2026-10-02. Professional training institution pipeline documentation.
13. LitMemo Blog. "The Complete Manga Production Workflow: From Storyboard to Finished Page in 7 Steps." https://litmemo.com/en/blog/manga-production-workflow — Retrieved 2026-10-02. Synthesised from multiple professional sources; documents consumer and commercial manga pipelines.
14. Manga with Stef. "Workflow and Equipment for Making a Manga." https://manga-with-stef.com/workflow-and-equipment-for-making-a-manga — Retrieved 2026-10-02. Practitioner documentation of the analog consumer manga pipeline including nēmu, penciling, inking, screentone stages.

**Full bibliography (30+ sources):** See `docs/research/grok/grok-line-art-formatted.md` for the complete bibliography used to synthesise Sections 2 and 3 of this document.
