# Pipeline Gap Analysis — #36 Research Record

**Date:** 2026-10-02
**Branch:** research/pipeline-validation-36
**Analysed against:** `art-theory-draft/art-theory/pipeline/00-overview.md` (11-step structure)
**Purpose:** External source review required before any pipeline step file (#7–#17) is written.

---

## 1. Sources Reviewed

| # | Title | Author / Organisation | URL | Description |
|---|---|---|---|---|
| S1 | "Concept Art" | Wikipedia | https://en.wikipedia.org/wiki/Concept_art | Encyclopedic overview of the concept art profession: ideation (blue-sky stage), sketch/speed-paint phases, progressive refinement to final polish; software and medium survey |
| S2 | "Concept Artist Job Description, Salary, Skills & Software" | CGSpectrum (professional CG training institution) | https://www.cgspectrum.com/blog/what-is-concept-art | Professional training blog: brief interpretation, design iteration, fundamentals required (composition, value, colour, perspective, gesture, reference); software overview |
| S3 | "How to Become a Concept Artist — Blizzard Artist Advice & Tips" | CGSpectrum / professional artist interview | https://www.cgspectrum.com/blog/what-it-is-like-to-be-a-professional-concept-artist | Professional Blizzard artist describing their workflow: brief → rough composition passes (shotgun blast) → lighting indication → client-review cycles → polish stage |
| S4 | "Illustration Courses" | Rhode Island School of Design (RISD) | https://www.risd.edu/academics/illustration/courses | Accredited university course catalogue: composition as central concern; perspective/form drawing sequence; value/light/shadow studies; critique-based review as terminal assessment |
| S5 | "Free Video Library" | Ctrl+Paint (Matt Kohr — digital painting educator) | https://www.ctrlpaint.com/library | Structured self-study curriculum with explicit pipeline sequence: workflow overview → composition/thumbnails → reference → gesture → form/value/light → basic rendering → colour → colour correction/polish → critique |
| S6 | "Digital Painting" | Wikipedia | https://en.wikipedia.org/wiki/Digital_painting | Encyclopedic overview: digital painting software/tools, role of traditional drawing skills as pipeline foundation, grayscale-to-colour workflows |
| S7 | "Creating Alien Character for Sci-Fi Short Film with Blender" | Artur Ledur / FornoFX (professional VFX character artist) | https://80.lv/articles/creating-an-alien-character-for-a-sci-fi-short-film-with-blender-substance-3d | Professional artist breakdown: reference gathering → exploratory blockout / silhouette design → form development → materials/texturing (colour pass + detail) → presentation renders; creature design and hard-surface combination |

All 7 URLs are publicly accessible and independently produced. They represent: 2 encyclopedic reference works (S1, S6), 2 professional training institutions (S2/S3 — CGSpectrum, S4 — RISD), 1 professional self-study platform (S5 — Ctrl+Paint), 1 professional artist interview (S3 embedded), and 1 professional VFX studio breakdown (S7 — 80.lv/FornoFX).

---

## 2. Source-to-Pipeline Mapping Tables

### S1 — Wikipedia: Concept Art

| Wikipedia phase | Maps to pipeline step | Notes |
|---|---|---|
| "Blue sky" ideation stage — broad sketches, speed paints, 3D overpaints | 01 Brief & Ideation + 03 Thumbnailing | Wikipedia uses "blue sky" to describe the early broad-direction phase |
| Reference gathering (implied — "inspiration for 3D modeling is a common use of concept art") | 02 Reference Gathering | Explicit in diagram caption; reference images used throughout |
| Sketch → development → polish progression | 03 → 09 → 10 | Three-phase model confirmed |
| Stylistic range: stylized to photorealistic | N/A — scope statement | Confirms pipeline covers both ends of the style spectrum |
| Final polish / tight deadline work | 10 Atmosphere & Polish | Described as "highly polished piece needed in short time" |
| Export / delivery | 11 Critique, Revision & Export | Implied by professional delivery context |

Steps with no explicit mapping in this source: 04 Gesture/Silhouette, 05 Perspective & Construction, 06 Value/Lighting, 07 Colour & Palette, 08 Form & Materials. These are not contradicted — they are below the granularity of the Wikipedia overview.

### S2 — CGSpectrum: What Is Concept Art

| CGSpectrum element | Maps to pipeline step | Notes |
|---|---|---|
| Interpreting a design brief | 01 Brief & Ideation | Described as "the key skill for a concept artist" |
| Drawing from written briefs | 01 Brief & Ideation | Explicit requirement listed |
| Reference and observation | 02 Reference Gathering | "Show process, sketches, roughs, and reference" in portfolio advice |
| Thumbnails / roughs / sketches | 03 Thumbnailing & Composition | "Present each piece with a brief explanation; show process, sketches, roughs" |
| Gesture, pose, posture, movement | 04 Gesture / Silhouette | Listed as required skill: "solid awareness of facial expression, pose, posture, gesture and movement" |
| Perspective, composition, depth of field, proportion, spatial awareness | 05 Perspective & Construction | Listed in required visual language skills |
| Value, shade, texture | 06 Value / Lighting + 08 Form & Materials | Listed in "visual language — texture, color, dimension, scale, perspective, shade" |
| Colour, dimension, scale | 07 Colour & Palette | Listed in required visual language skills |
| Polish / presentation | 10 Atmosphere & Polish | "Highly polished piece needed in a short amount of time" (Wikipedia quote); implies polish stage |
| VFX and video game pipeline familiarity | 11 Critique, Revision & Export | "Familiarize yourself with the VFX and video game pipelines and how your work will be used" |

### S3 — CGSpectrum: Professional Artist Workflow Interview

| Artist-described phase | Maps to pipeline step | Notes |
|---|---|---|
| Understanding client expectations / brief | 01 Brief & Ideation | "It's important to understand your client's expectations" |
| First pass ("shotgun blast") — broad, loose compositions | 03 Thumbnailing & Composition | "Keep them as loose as your director will allow" |
| Rough compositions with character attitude and environment relationship | 03 Thumbnailing & Composition + 04 Gesture/Silhouette | Attitude of characters maps to gesture; composition maps to step 3 |
| Indicating lighting direction in rough stage | 06 Value / Lighting | "If I'm trying something more daring with the lighting I'll also try and indicate that in the rough stage" — confirms value/lighting is considered at thumbnail stage |
| Client review / iterative refinement | Embedded throughout; final expression is Step 11 | "With each review from the client I work tighter until at the polish stage" |
| Polish stage | 10 Atmosphere & Polish | Explicit: "until at the polish stage" |

### S4 — RISD Illustration Courses

| RISD course focus | Maps to pipeline step | Notes |
|---|---|---|
| Composition as central concern — "how elements fit within the frame and their relationship to each other" | 03 Thumbnailing & Composition | Composition is taught as a foundational, early-stage skill |
| Perspective/form — "convincing depiction of form in three-dimensional space"; observational + projected perspective systems | 05 Perspective & Construction | Dedicated course; confirms perspective is a distinct, teachable stage |
| "Effective composition and convincing light and shadow to shape expression" | 06 Value / Lighting | RISD teaches light/shadow as a compositional and expressive tool |
| Process-over-finish philosophy: "process over finish, idea over application" | Steps 01–03 | RISD explicitly trains students to prioritise early-stage process |
| Critique-based terminal assessment | 11 Critique, Revision & Export | Group critique is the assessment mechanism for each course |

### S5 — Ctrl+Paint Library (most complete pipeline mapping)

| Ctrl+Paint section | Maps to pipeline step | Severity |
|---|---|---|
| Workflow Overview videos | Preamble to all steps | N/A |
| Composition Basics / Compositional Framing Elements / Using Text in a Composition | 03 Thumbnailing & Composition | S1 confirmed |
| Using Reference Materials / Reference Process / How to Draw Anything in 3 Steps / Designing with Reference | 02 Reference Gathering | S1 confirmed |
| Gesture (Film Studies: Gesture, Quick Pose Gesture Sketching, Why Bother with Gesture Drawing?) | 04 Gesture / Silhouette | S1 confirmed |
| Form, Value, and Light | 05 Perspective & Construction + 06 Value / Lighting | S1 confirmed; Ctrl+Paint combines form/value/light — the pipeline separates them for pedagogical granularity, which is a deliberate simplification |
| Basic Rendering 1–4 | 08 Form & Materials + 09 Rendering & Detail | S1 confirmed; covers surface response to light + detail placement |
| Painting with Colour / Colour Relativity / Colour Schemes / Colour Contrast | 07 Colour & Palette | S1 confirmed |
| Colour Correction / Colour Grading / Polish | 10 Atmosphere & Polish | S1 confirmed |
| Critique section | 11 Critique, Revision & Export | S1 confirmed |

Note: Ctrl+Paint does not include a "Brief & Ideation" section. This is because Ctrl+Paint is a technical skills curriculum, not a professional workflow guide. The brief/ideation stage is a professional practice concern. The absence is not a contradiction — it is a scope difference.

### S6 — Wikipedia: Digital Painting

| Wikipedia element | Maps to pipeline step | Notes |
|---|---|---|
| Traditional drawing skills as foundation | Steps 03–06 | "Proficiency with traditional media is often paramount to a concept artist's ability to use painting software" — confirms fundamentals underpin all pipeline steps |
| Grayscale-to-colour workflow | 06 → 07 | "Grayscale to Color" workflow explicitly described via software features |
| Digital painting workflow (sketch → refine → finalise) | Steps 01–11 generally | Confirms the general direction of the pipeline |

### S7 — 80.lv / Artur Ledur (Creature Design / VFX Pipeline)

| Artist-described phase | Maps to pipeline step | Notes |
|---|---|---|
| Reference gathering (PureRef, ArtStation, Pinterest) | 02 Reference Gathering | First explicit step described: "gathered a large collection of visual references in PureRef, focusing primarily on creature design and hard-surface armor" |
| Exploratory blockout / finding visual language | 03 Thumbnailing & Composition + 04 Gesture/Silhouette | "Using exploratory sculpting to find the right visual language for the character"; silhouette design is explicit: "added an extra pair of arms, which gave the character a much more distinctive silhouette" |
| Silhouette legibility as a design criterion | 04 Gesture / Silhouette | Direct: "For one of the backlit shots, where the Alien appears mostly as a silhouette, I wanted to make its shape immediately feel more alien" |
| Form development / topology | 05 Perspective & Construction | 3D equivalent of constructing forms in space |
| First colour pass using solid colours | 07 Colour & Palette | "I usually start with a first color pass using solid colors to establish an approximate overall look" |
| Materials development (metal, carbon fiber, rubber, emissive) | 08 Form & Materials | "From there, I build the main materials" |
| Tertiary detail / roughness variation / wear | 09 Rendering & Detail | "This was probably the stage where the character really started to feel alive to me" |
| Presentation renders / studio lighting setup | 10 Atmosphere & Polish | "I posed the character in ZBrush and then sent it back to Blender, where I used a basic studio lighting setup to showcase" |
| Production-time constraints inform stage decisions | 11 Critique, Revision & Export | "Instead of trying to make everything perfect at every stage, I focused on establishing the main forms and visual language quickly" |

Note: S7 is a 3D pipeline (sculpt/retopo/texture) rather than a 2D illustration pipeline. The steps map cleanly to the 2D pipeline steps, confirming the pipeline's underlying logic applies across mediums. The 3D equivalents are: blockout = thumbnailing; sculpt = form construction; texturing = materials + colour. This is a deliberate simplification documented below.

---

## 3. Consolidated Gap Findings

### All Severity Classifications

| Finding ID | Description | Severity | Source(s) |
|---|---|---|---|
| G-01 | Brief & Ideation (Step 01): Confirmed across professional sources as the entry point. CGSpectrum names it explicitly; professional interview confirms brief interpretation is the primary skill. | **1 — CONFIRMED** | S2, S3 |
| G-02 | Reference Gathering (Step 02): Confirmed as a discrete stage. Ctrl+Paint has a dedicated section; S7 names it first. | **1 — CONFIRMED** | S2, S5, S7 |
| G-03 | Thumbnailing & Composition (Step 03): Confirmed. Ctrl+Paint, RISD, and professional interview all confirm thumbnail/rough as the first visual production stage. | **1 — CONFIRMED** | S2, S3, S4, S5 |
| G-04 | Gesture / Silhouette (Step 04): Confirmed. Ctrl+Paint has a dedicated gesture section; S7 describes silhouette as an explicit design criterion; CGSpectrum lists gesture as a required professional skill. | **1 — CONFIRMED** | S2, S5, S7 |
| G-05 | Perspective & Construction (Step 05): Confirmed. RISD has a dedicated perspective/form course; CGSpectrum lists perspective and spatial awareness as required skills; Ctrl+Paint covers form/value/light in combination. | **1 — CONFIRMED** | S2, S4, S5 |
| G-06 | Value / Lighting (Step 06): Confirmed. RISD: "effective composition and convincing light and shadow"; Ctrl+Paint: dedicated Form/Value/Light section; professional artist confirms lighting is considered from the rough stage. | **1 — CONFIRMED** | S3, S4, S5 |
| G-07 | Colour & Palette (Step 07): Confirmed. Ctrl+Paint has the most complete colour curriculum; S7 confirms first colour pass as a distinct step; CGSpectrum lists colour as a required fundamental. | **1 — CONFIRMED** | S2, S5, S7 |
| G-08 | Form & Materials (Step 08): Confirmed. S7 explicitly describes building materials after colour pass; Ctrl+Paint's Basic Rendering covers surface response to light. | **1 — CONFIRMED** | S5, S7 |
| G-09 | Rendering & Detail (Step 09): Confirmed. S7: "the stage where the character really started to feel alive" — wear, scratches, variation; Ctrl+Paint's Basic Rendering 1–4 progression. | **1 — CONFIRMED** | S5, S7 |
| G-10 | Atmosphere & Polish (Step 10): Confirmed. Professional interviews and Wikipedia both describe a polish stage as the terminal production phase before delivery. | **1 — CONFIRMED** | S1, S3, S5 |
| G-11 | Critique, Revision & Export (Step 11): Confirmed. Ctrl+Paint has a dedicated Critique section; RISD uses critique as terminal assessment; S7 artist explicitly describes final presentation as the last stage. | **1 — CONFIRMED** | S4, S5, S7 |
| G-12 | Step 01 absent from Ctrl+Paint: Ctrl+Paint does not include a "Brief & Ideation" section. This is a scope difference (technical skills curriculum vs. professional workflow guide), not a structural contradiction. | **1 — CONFIRMED** (absence is expected) | S5 |
| G-13 | Steps 05+06+08 combined in some sources: Ctrl+Paint groups Form/Value/Light together; S7 treats materials as a texturing-phase concern. The pipeline's separation of these into three steps (05, 06, 08) is a deliberate pedagogical choice for granularity. No source contradicts the separation — they simply describe them at a coarser grain. | **1 — CONFIRMED** (deliberate simplification) | S5, S7 |
| G-14 | Iterative review embedded throughout: Professional sources (S3, S7) describe review/feedback as ongoing through all stages, not just at Step 11. Step 11 is the terminal check; earlier stages include stage sign-off conditions in the step files. This is consistent with the pipeline design. | **1 — CONFIRMED** (sign-off conditions per step address this) | S3, S7 |

**Worst finding severity: 1 — CONFIRMED**

---

## 4. Art Type / Style / Subject / Medium Coverage

| Category | Coverage confirmed by sources | Notes |
|---|---|---|
| **Art types** | | |
| Digital illustration | S1, S2, S3, S4, S5, S6 | All major sources |
| Character art | S2, S3, S7 | CGSpectrum, RISD, 80.lv explicitly |
| Environment art | S1, S2, S3 | Wikipedia, CGSpectrum discuss environment as a concept art type |
| Creature design | S7 | 80.lv creature/character article; pipeline applies identically |
| **Workflow types** | | |
| Traditional-to-digital | S5, S6 | Ctrl+Paint and Wikipedia describe traditional foundation → digital application |
| Digital-only | S1, S2, S5 | Majority of sources |
| **Subject types** | | |
| Figures | S2, S7 | Character/anatomy focus; gesture explicitly |
| Environments | S1, S2, S3 | Described as a major concept art category |
| Creatures | S7 | 80.lv article; distinct silhouette concerns documented |
| Vehicles | S2 | CGSpectrum lists vehicles as a concept art category |
| Architecture | S2 | Listed as a concept art subject type |
| Abstract | Not explicitly covered | No source contradicts; abstract composition uses the same pipeline stages |
| **Style registers** | | |
| Realistic | S1, S2, S7 | Described throughout |
| Stylized | S1, S2, S3 | CGSpectrum artist describes stylistic flexibility |
| Painterly | S5, S6 | Ctrl+Paint and digital painting Wikipedia |
| Graphic/flat | Not explicitly covered | No source contradicts |
| Line art | S5 | Ctrl+Paint covers line-work as part of the library |
| **Mediums** | | |
| Grayscale | S5, S6 | Ctrl+Paint and Wikipedia both cover grayscale workflows |
| Colour | All sources | Universal |
| Line-only | S5 | Ctrl+Paint library includes line-work |
| Mixed | S5, S7 | Ctrl+Paint covers mixed approaches; S7 describes layered technique |

---

## 5. Outcome Determination

**Worst finding severity:** 1 — CONFIRMED

**Outcome class: A — Confirmed**

The current 11-step pipeline structure is confirmed by external sources. All 11 steps have external support. No step is contradicted, inapplicable, or conflated in a way that requires structural revision. The separations made in the pipeline (e.g., steps 05/06/08 rather than one combined step) are deliberate pedagogical choices not contradicted by any source.

**Conclusion:** `docs/specs/pipeline-definition.md` may be written with the current 11-step structure as confirmed.

---

## 6. Deliberate Simplifications (Mapping to 13-Stage Reference PDF)

The reference PDF (`Art_Theory_Digital_Practice_Reference_v5.pdf`) describes 13 stages. The pipeline uses 11. The simplifications are:

| Reference PDF stages (13) | Pipeline consolidation (11) | Rationale |
|---|---|---|
| Stages 1–2: Client brief + Creative exploration | Step 01: Brief & Ideation | Merged — both concern the pre-production planning and direction-finding phase |
| Stages 3–4: Reference and research + Mood board / visual language | Step 02: Reference Gathering | Merged — both concern gathering external visual information |
| Stages 5–6: Composition + Rough sketches | Step 03: Thumbnailing & Composition | Merged — composition and thumbnailing are simultaneous concerns |
| Stages 7–8: Gesture / silhouette + Form construction | Steps 04 + 05 | Kept separate — gesture/silhouette and 3D form construction address different questions |
| Stage 9: Value / lighting design | Step 06 | 1:1 |
| Stage 10: Colour | Step 07 | 1:1 |
| Stage 11: Surface / materials | Step 08 | 1:1; expanded to include materials alongside form |
| Stage 12: Rendering and detail | Step 09 | 1:1 |
| Stage 13: Final polish + critique + export | Steps 10 + 11 | Separated — atmosphere/polish (visual) and critique/export (professional/technical) are distinct concerns |

Total: 13 PDF stages → 11 pipeline steps via 3 merges and 1 split.
