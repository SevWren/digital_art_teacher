# Pipeline Definition — Confirmed Specification

**Date confirmed:** 2026-10-02
**Status:** Confirmed — Outcome A (all findings Severity 1)
**Blocks:** Issues #7–#17 (pipeline step files may now be written)
**Gap analysis:** `docs/specs/pipeline-gap-analysis.md`
**Sources:** 7 independent professional sources — see Section 5

> **Owner confirmation required.** This document presents the confirmed pipeline structure and findings from external research. Pipeline step files (#7–#17) must NOT be started until the owner has reviewed this document and confirmed the structure in a comment on GitHub issue #36.

---

## 1. Confirmed Pipeline Structure

The pipeline consists of **11 steps** in the following sequence:

| # | Step name | Primary question answered | Governing fundamental(s) |
|---|---|---|---|
| 01 | Brief & Ideation | What must this image achieve and for whom? | Design / Shape language, Composition |
| 02 | Reference Gathering | What visual evidence do I need? | All fundamentals (observation) |
| 03 | Thumbnailing & Composition | What is the strongest arrangement of major shapes? | Composition, Design |
| 04 | Gesture / Silhouette | Does the pose or major form read clearly at a distance? | Anatomy & Gesture, Form |
| 05 | Perspective & Construction | Do the forms sit convincingly in space? | Perspective, Form & Construction |
| 06 | Value / Lighting | Is the light design clear and hierarchical? | Light & Value |
| 07 | Colour & Palette | Do the colours support hierarchy and mood? | Colour |
| 08 | Form & Materials | Do surfaces respond correctly to the light? | Materials & Texture, Form |
| 09 | Rendering & Detail | Where does the eye rest and where does it travel? | Composition, Light & Value |
| 10 | Atmosphere & Polish | Are depth, focus, and final adjustments coherent? | Perspective (atmospheric), Colour, Light |
| 11 | Critique, Revision & Export | Does the image meet the brief and technical requirements? | All + Critique methods |

This structure is unchanged from `pipeline/00-overview.md`. External research confirmed all 11 steps. No additions, removals, or renumbering are required.

---

## 2. Per-Step Specifications

### Step 01 — Brief & Ideation

**Purpose:** Establish a clear, written goal for the image before any visual production begins. Explore directional options at word-level (notes, written descriptions, rough concept sketches) before committing to one.

**Primary outputs:**
- Written brief: one or two sentences stating who will see the image, what mood it should create, and what the single most important element is
- At least two directional concepts explored (may be written descriptions, not necessarily sketches)
- One chosen direction confirmed as the working brief

**Governing fundamentals:** Design & Shape Language (goal clarity, visual hierarchy intent), Composition (early thinking about layout priorities)

**Failure modes from skipping:**
- Image drifts mid-production when the artist loses track of the original goal
- Rework at late stages when the image technically succeeds but serves the wrong purpose
- No reference point against which to judge whether Step 11 (critique) passes or fails

**Connections to other steps:**
- Informs Step 02 (what specific reference is needed depends on the brief)
- Informs Step 03 (composition choices depend on the image's purpose)
- Is the primary check item in Step 11 (does the finished image meet the brief?)

---

### Step 02 — Reference Gathering

**Purpose:** Collect visual evidence grounding every claim the image makes. References are kept visible alongside the canvas throughout production — they are not copied, but used to ensure shapes, proportions, and materials are grounded in observable reality rather than guesswork.

**Primary outputs:**
- A curated reference set visible alongside the working canvas
- References covering: the subject(s) and their anatomy/construction; the lighting situation; the materials/surfaces present; the environment (if applicable)

**Governing fundamentals:** All fundamentals (observation-based)

**Failure modes from skipping:**
- Anatomy, proportion, and surface detail drift toward generic approximations
- Lighting direction and surface response become internally inconsistent
- Feedback of "it doesn't look real" is difficult to address without reference grounding

**Connections to other steps:**
- Feeds into Steps 03–09 continuously; reference remains active throughout the pipeline
- Specific reference for materials is most needed at Step 08

---

### Step 03 — Thumbnailing & Composition

**Purpose:** Explore layout options at small scale (coin-sized or postage-stamp-sized) before committing to full-canvas work. Identify the strongest arrangement of major shapes. A strong thumbnail reading at small scale is a reliable indicator that the composition will hold at full size.

**Primary outputs:**
- A set of at least 3–5 thumbnail arrangements (rough dark/light shapes; no internal detail)
- One selected thumbnail: the approved compositional direction
- The approved thumbnail stored as a locked reference for comparison throughout the pipeline

**Governing fundamentals:** Composition (grouping, figure/ground, visual hierarchy, leading lines), Design & Shape Language (major shape relationships)

**Failure modes from skipping:**
- Composition chosen by default (whatever fills the canvas first) rather than by deliberate selection
- Rework of composition at late rendering stages — the most expensive rework possible
- Layout that is technically well-executed but compositionally weak

**Connections to other steps:**
- Step 04 (gesture/silhouette): the chosen thumbnail's major shapes become the silhouette tested in Step 04
- Step 09 (rendering/detail): the thumbnail's focal area determines where detail is added in Step 09
- Step 10 (atmosphere/polish): the thumbnail is checked again at final stage to confirm the composition has been maintained
- Step 11: the thumbnail is a primary locked reference for the final check

---

### Step 04 — Gesture / Silhouette

**Purpose:** Verify that the pose (for figures) or the major form (for environments, objects, creatures) reads clearly as a legible silhouette before any internal detail is added. The silhouette test: imagine cutting the shape out of black paper — does the cutout communicate the subject and its pose or character clearly at a distance?

**Primary outputs:**
- Gesture or major form laid in at full canvas scale (loose, no detail)
- Silhouette pass confirming the outer edge is clear and readable
- Any corrections to proportion or pose made at this stage before internal work begins

**Governing fundamentals:** Anatomy & Gesture (figure rhythm, weight, movement), Form & Construction (primary form reading)

**Failure modes from skipping:**
- Stiff, unclear, or vague outer form that internal rendering cannot fix
- Proportions locked in with detail on top — expensive to correct
- Creature, character, or object that looks the same as many others because the distinctive silhouette was never designed

**Connections to other steps:**
- Follows from Step 03 (the approved thumbnail defines the major shapes being tested)
- Step 05 (perspective/construction) is built on top of the gesture/silhouette pass

---

### Step 05 — Perspective & Construction

**Purpose:** Build the underlying geometric structure that confirms all forms sit convincingly in three-dimensional space. Block in major objects as simple geometric approximations (boxes, cylinders, spheres) before any surface detail. Fix structural problems — floating, leaning, inconsistent scale — at this stage, not after rendering.

**Primary outputs:**
- Construction drawing or block-in showing major forms as simple geometry
- Perspective consistent (implied or explicit horizon line; forms receding correctly)
- Nothing floating, leaning, or off-scale relative to the established space

**Governing fundamentals:** Perspective (1-point, 2-point, atmospheric depth), Form & Construction (building complex forms from primary forms)

**Failure modes from skipping:**
- Structural problems buried under rendered detail — extremely expensive to fix
- Forms that look flat, floating, or inconsistently scaled
- Lighting in Step 06 applied to forms that do not have a convincing three-dimensional structure to respond to

**Connections to other steps:**
- Built on top of Step 04 gesture/silhouette
- Step 06 (value/lighting) requires solid construction to apply lighting convincingly
- Step 08 (form/materials) requires construction for surfaces to respond to light correctly

---

### Step 06 — Value / Lighting

**Purpose:** Design the light-and-dark structure of the image in greyscale before any colour is introduced. A grey version of the image that reads clearly when squinted at is the most reliable foundation for the colour pass — problems in value are not fixable by colour.

**Primary outputs:**
- Greyscale value study at reduced size (does not need to be full-canvas detail)
- Light source established: direction, intensity, type (ambient, directional, point source)
- Clear value hierarchy: lightest values at the focal area, darker values receding
- Image squint-tests: major shapes read clearly in greyscale

**Governing fundamentals:** Light & Value (value families, form shadows, cast shadows, reflected light, edge control)

**Failure modes from skipping:**
- Colour applied to a weak value structure: individual colours may look individually correct but the image reads as flat or chaotic
- Muddy, indistinct colour work that is actually a value problem masquerading as a colour problem
- No clear focal hierarchy: the eye has nowhere to land

**Connections to other steps:**
- Built on Step 05 construction (light responds to form)
- Step 07 (colour) is applied on top of the value structure; the grey version remains visible for comparison
- Step 10 (atmosphere/polish): atmospheric depth is a value relationship (distant planes lighter and less contrasty)

---

### Step 07 — Colour & Palette

**Purpose:** Apply colour in a way that supports the existing value hierarchy established in Step 06. Colour adds mood, temperature, and identity without fighting the dark-and-light plan already built.

**Primary outputs:**
- Colour applied across the image with the grey version visible for comparison
- A colour palette limited to 3–5 dominant colours (or a clear temperature relationship: warm/cool)
- Colour hierarchy aligned with value hierarchy: focal area has the most saturated or contrasting colour; supporting areas are less saturated

**Governing fundamentals:** Colour (hue, saturation, temperature, simultaneous contrast, limited palette)

**Failure modes from skipping:** (applies to artists who add colour directly without a value study)
- Saturated colours attract the eye to the wrong areas, overriding value-based hierarchy
- No colour mood consistency: colours feel arbitrary rather than deliberate
- Retouching value problems by adjusting colour — the mismatch between the two layers creates muddy results

**Connections to other steps:**
- Dependent on Step 06 value structure; must not override it
- Step 08 (form/materials) adds surface colour variation on top of the base colour pass
- Step 10 (atmosphere/polish) makes final colour adjustments for depth and unity

---

### Step 08 — Form & Materials

**Purpose:** Add the surface detail that shows how each material responds to the light source established in Step 06. Smooth surfaces reflect sharply; rough surfaces scatter light diffusely; metal reflects the environment; skin subsurfaces scatter light softly.

**Primary outputs:**
- Surface response to light present on all major materials (not decoration — structural light behaviour)
- Material distinction visible: at least one clear difference between the primary materials (e.g., skin vs. fabric vs. metal)
- Secondary values (reflected light, ambient occlusion at form joins, cast shadows from secondary forms) present where relevant

**Governing fundamentals:** Materials & Texture (surface properties, light response), Form & Construction (how form determines shadow terminator and reflected light)

**Failure modes from skipping:**
- All materials look like the same shiny or matte paint
- Lighting feels generic because surfaces do not respond differently to the same light source
- Image feels flat despite correct value hierarchy in Step 06 — the surfaces are not carrying three-dimensional information

**Connections to other steps:**
- Built on Step 05 construction and Step 06 lighting
- Step 09 (rendering/detail) adds fine detail on top of the material base

---

### Step 09 — Rendering & Detail

**Purpose:** Apply fine detail selectively to reinforce the focal hierarchy established in Steps 03 and 06. Detail at the focal point draws the eye; detail everywhere cancels the focal point. This step adds texture, edge refinement, and surface micro-variation — it does not add new forms.

**Primary outputs:**
- High-detail rendering at the focal area (established in Step 03 thumbnail)
- Reduced detail toward the edges and secondary areas
- Edge quality varied: sharp edges on focal foreground elements; soft, lost edges on peripheral or background elements

**Governing fundamentals:** Composition (focal hierarchy, edge control), Light & Value (sharp highlights at focal points, soft edges receding)

**Failure modes from skipping or over-applying:**
- Uniform detail across the image: the eye tours the surface instead of landing on the subject
- Soft or vague focal area obscured by detailed background
- Detail added to compensate for structural or compositional weakness — detail on a weak foundation makes the foundation harder to fix, not easier

**Connections to other steps:**
- Built on Step 08 materials; adds detail on top of the material base
- Step 10 (atmosphere/polish) may soften detail in distant planes for atmospheric depth

---

### Step 10 — Atmosphere & Polish

**Purpose:** Final adjustments for unity, depth, and coherence. Atmospheric perspective (distant planes lighter, less saturated, lower contrast), focus softening for depth, colour unity pass, and correction of anything that felt slightly off at the rendering stage.

**Primary outputs:**
- Atmospheric depth present if the image has spatial depth (far objects lighter and less saturated)
- Overall colour unity (no colours that feel unrelated to the palette established in Step 07)
- Thumbnail re-check: image read at small scale matches or improves on the approved thumbnail from Step 03
- Final soft-focus on secondary planes if the image uses depth of field

**Governing fundamentals:** Perspective (atmospheric depth), Colour (colour unity, colour grading), Light & Value (contrast reduction with depth)

**Failure modes from skipping:**
- Image feels unfinished at a technical level even when rendering is complete
- Focal area competes with background because atmospheric separation was not applied
- Colour drift across the pipeline: individual stages introduced colours that look correct locally but create disunity overall

**Connections to other steps:**
- Final visual pass before Step 11
- Uses the approved thumbnail from Step 03 as the check reference

---

### Step 11 — Critique, Revision & Export

**Purpose:** Check the finished image against the original brief from Step 01 and the locked references from earlier stages. Make any revisions required. Export at the technical specifications appropriate for the intended use.

**Primary outputs:**
- Brief check complete: does the image achieve the goal stated in Step 01? Specific, observable answer (not "I think so")
- Revision list addressed (or explicitly accepted as-is with reasoning)
- File exported at the correct resolution, format, and colour profile for the intended output

**Governing fundamentals:** All fundamentals (holistic check); Critique Methods (structured self-critique against brief)

**Failure modes from skipping:**
- Image delivered without confirming it meets the brief — client or viewer receives work that misses the stated goal
- Export at wrong resolution or format — technical failure on delivery
- No record of the decision point: revisions requested after export have no reference for what was approved

**Connections to other steps:**
- Step 01 brief is the primary check item
- Step 03 thumbnail is the secondary check item (did the composition hold?)
- Closes the pipeline; output feeds back into Step 01 of the next piece (lessons learned)

---

## 3. Scope Statement

This pipeline applies to the following:

**Art types:** Digital illustration, character art, environment art, creature design.

**Workflow types:** Traditional-to-digital (foundation skills from Steps 03–06 apply equally to traditional media before going digital); digital-only.

**Subject types:** Figures, environments, creatures, vehicles, architecture. Abstract compositions follow the same pipeline but Steps 04 (gesture) and the figurative aspects of Step 05 (construction) apply to abstract form relationships rather than anatomical forms.

**Style registers:** Realistic, stylized, painterly, graphic/flat, line art. The pipeline steps are medium-neutral; the specific techniques within each step vary by style, but the questions each step answers ("does the composition work?", "does the value structure hold?", etc.) apply regardless of style register.

**Mediums:** Greyscale, colour, line-only, mixed. For line-only work, Steps 06 (value) and 07 (colour) are reduced in scope but the compositional and structural steps apply in full. For greyscale work, Step 07 is omitted; Steps 06 and 08 merge.

**What this pipeline does NOT cover:**
- 3D modelling workflows beyond the 2D-to-3D reference use noted in source S7
- Motion/animation production
- Photography

---

## 4. Mapping to 13-Stage Reference PDF

The reference PDF (`Art_Theory_Digital_Practice_Reference_v5.pdf`) describes 13 stages. The pipeline uses 11 via the following deliberate simplifications:

| Reference PDF stages | Pipeline step | Simplification |
|---|---|---|
| Stages 1–2: Client brief + Creative exploration | Step 01: Brief & Ideation | Merged — both concern pre-production goal-setting |
| Stages 3–4: Reference/research + Mood board / visual language | Step 02: Reference Gathering | Merged — both concern gathering external visual material |
| Stages 5–6: Composition + Rough sketches | Step 03: Thumbnailing & Composition | Merged — composition and thumbnailing happen simultaneously |
| Stage 7: Gesture / silhouette | Step 04: Gesture / Silhouette | 1:1 |
| Stage 8: Form construction | Step 05: Perspective & Construction | 1:1; expanded to include perspective alongside form |
| Stage 9: Value / lighting | Step 06: Value / Lighting | 1:1 |
| Stage 10: Colour | Step 07: Colour & Palette | 1:1; expanded to include palette planning |
| Stage 11: Surface / materials | Step 08: Form & Materials | 1:1 |
| Stage 12: Rendering and detail | Step 09: Rendering & Detail | 1:1 |
| Stage 13: Final polish + critique + export | Steps 10 + 11 | Split — atmosphere/polish (visual) and critique/export (professional) are different concerns |

Net: 13 → 11 via 3 merges, 1 split, 1 expansion.

---

## 5. Sources

1. Wikipedia. "Concept Art." https://en.wikipedia.org/wiki/Concept_art — Retrieved 2026-10-02.
2. CGSpectrum. "Concept Artist Job Description, Salary, Skills & Software." https://www.cgspectrum.com/blog/what-is-concept-art — Retrieved 2026-10-02.
3. CGSpectrum / Professional artist interview. "How to Become a Concept Artist." https://www.cgspectrum.com/blog/what-it-is-like-to-be-a-professional-concept-artist — Retrieved 2026-10-02.
4. Rhode Island School of Design (RISD). "Illustration Courses." https://www.risd.edu/academics/illustration/courses — Retrieved 2026-10-02.
5. Ctrl+Paint (Matt Kohr). "Free Video Library — Digital Painting Simplified." https://www.ctrlpaint.com/library — Retrieved 2026-10-02.
6. Wikipedia. "Digital Painting." https://en.wikipedia.org/wiki/Digital_painting — Retrieved 2026-10-02.
7. Artur Ledur / FornoFX via 80.lv. "Creating Alien Character for Sci-Fi Short Film with Blender." https://80.lv/articles/creating-an-alien-character-for-a-sci-fi-short-film-with-blender-substance-3d — Retrieved 2026-10-02.
