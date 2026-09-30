# ADR-0005 — Output Register and Pedagogical Translation Layer

**Date:** 2026-09-30
**Status:** Accepted

---

## Context

The project's corpus and knowledge base files are written in professional art-school vocabulary: *notan*, *simultaneous contrast*, *planar analysis*, *ASIS*, *foreshortening*, *value hierarchy*, *specular reflection*, *sRGB*, *station point*, *cone of vision*. This is appropriate for a verified technical corpus.

The target user is a hobbyist digital artist — recreational, early-to-intermediate level, drawing for enjoyment. They use tools like Procreate, Clip Studio, Krita, or Photoshop. They have not taken formal art classes.

At the time this ADR was filed, no instruction file in the project specified:
- What register (academic vs. plain English) the agent should use for user-facing output
- Which processing steps are internal-only vs. user-visible
- How corpus citations, §8 row references, and workflow terms should be translated before reaching the user

As a result, ICL (Internal Compliance Layer) outputs were wired directly to UCL (User Communication Layer) output in three specific places:

1. **Citations**: CLAUDE.md required citing `fundamentals/light-and-value.md` and `§8` directly in responses. These references have no meaning to a hobbyist.
2. **Failure-mode diagnosis format**: The prescribed form surfaced §8 row references and academic failure-mode labels verbatim.
3. **Pending workflow prompts**: Users were asked to "defer", "approve", "reject" — CONTEXT.md workflow terms opaque to hobbyists.

---

## Decision

1. **Two-layer output model is adopted.** All agent processing is formally divided into:
   - **Internal Compliance Layer (ICL):** routing, evidence checks, six-checks, gap detection, expiry calculations, failure-mode table matching. Never surfaced verbatim to the user.
   - **User Communication Layer (UCL):** everything the user reads. Governed by plain-English mandate and the Pedagogical Translation Matrix.

2. **Plain-English mandate for all UCL output.** Every user-facing response uses plain, accessible English. Technical terms may appear but must be followed immediately by a plain-language explanation and a concrete example on first use. The Pedagogical Translation Matrix (PTM) at `docs/pedagogy/translation-matrix.md` is the canonical reference for translations.

3. **Citations are internal traceability, not UCL output.** The evidence rule (every claim traces to a Tier 1 source) is an ICL integrity gate. Passing that gate is the precondition for the advice appearing in a response — but the citation itself (file path, §8 reference) does not appear in the user-facing response. If source transparency is contextually appropriate, the agent uses a plain-language form: "this is standard lighting theory" rather than "per §8 of the reference doc."

4. **UCL translation table for workflow prompts.** The terms defer, approve, reject, resolve, and promote are internal workflow vocabulary. When the agent must prompt the user for a pending-entry decision, it uses plain language from the UCL translation table defined in the CLAUDE.md output-register section.

5. **Pedagogical Translation Matrix (PTM) created.** A dedicated file at `docs/pedagogy/translation-matrix.md` maps every corpus/academic term to: plain name, plain definition, concrete digital-painting example, and use-in-output sample sentence.

6. **All knowledge base files gain a Plain-English Guide section.** Existing files are retrofitted (issue #29). All new pipeline and fundamentals files include the section from the start (amended briefs for issues #7–21).

---

## Consequences

- CLAUDE.md gains a `## Output register` section (issue #27).
- `docs/pedagogy/translation-matrix.md` is created (issue #28).
- All existing knowledge base files gain a `## Plain-English Guide` section (issue #29).
- All new pipeline and fundamentals files (#7–21) require the Plain-English Guide section and are blocked by #27 and #28.
- The guardrail spec (#3) must include user-facing deflection language in UCL register.
- Integration QA (#25) gains a 7th test domain covering output register.
- The corpus files (academic content) are not modified; the PTM is an additive translation layer.

---

## Alternatives considered

**Alternative A: Rewrite corpus files in plain English.**
Rejected. The corpus is the verified, citeable source of truth. Academic precision in the corpus is a feature, not a problem. Rewriting corpus files in plain English would compromise their role as a stable reference and make citation harder. The translation layer is the correct architectural split.

**Alternative B: Per-response inline translation only (no PTM file).**
Rejected. Without a stable reference, translations will be inconsistent across agents and sessions. The PTM makes the translation a first-class corpus artifact with the same version discipline as the rest of the project.

**Alternative C: Add plain-English sections to corpus files only, no CLAUDE.md output rule.**
Partially adopted (plain-English sections are added to knowledge files). But insufficient on its own: the output-register rule and UCL translation table in CLAUDE.md are necessary to govern workflow prompts, citation format, and failure-mode diagnosis language, which don't live in knowledge files.

---

## Amendment — PTM Example Quality Standard

**Date:** 2026-09-30

Initial PTM examples were reviewed and found to still fail for hobbyists. Identified failure pattern: examples were written one step plainer than the corpus but still inside the art world. Three specific failure modes:

1. **Art vocabulary used to explain art vocabulary** — e.g., "your highlights and lit ground" to explain "light group." A user who doesn't know what a light group is also doesn't know what a highlight is.
2. **Physically inaccurate analogies** — e.g., "think of a cheek as flat panels." A cheek is visibly curved; the analogy breaks on inspection and teaches incorrect intuition.
3. **Abstract nouns substituted for other abstract nouns** — e.g., replacing "Gestalt" with "unit." "Unit" is equally opaque without a physical anchor.

### Three mandatory example quality tests (now part of the PTM spec)

Every PTM example must pass all three before acceptance:

**Test 1 — Zero art vocabulary.** No art-specific terms in the example. The example must stand alone without them.

**Test 2 — Physically accurate analogy.** The analogy must be factually consistent with the concept. A wrong physical analogy teaches wrong intuition.

**Test 3 — No abstract nouns without a physical anchor.** Words like "unit", "element", "form", "structure", "region", "space" must each be replaced with or immediately followed by something physical and touchable.

### Required example pattern

**Everyday anchor first → then connect to the painting.**

Start with a physical, everyday object or observable phenomenon requiring zero art knowledge (a cardboard box, a black-and-white photo, a flock of birds, sunlight through a window). Describe what happens. Then connect to the painting in one sentence.

### Reference corrected examples

| Concept | Corrected example |
|---|---|
| Light group / shadow group | "In a black-and-white photo, everything is either bright or dark. A good painting keeps all the bright things in one 'team' and all the dark things in another team. The moment those teams mix everywhere into the same muddy grey, the image looks flat and hard to read." |
| Flat-face thinking (planar analysis) | "Think of a cardboard box sitting in sunlight. The top face is bright. The front face is medium. The side is dark. Even though a nose or an arm is curved, your brain reads it the same way — bright side, medium side, dark side. When painting anything rounded, start by asking: which 'face of the box' is this part?" |
| How eyes smoosh things (gestalt) | "A flock of birds looks like one moving smudge, not 500 separate birds — your eyes automatically lump nearby things into one blob before you see the details. In a painting, three characters standing close together will read as 'a group of people' before the viewer looks closely enough to count them." |

These examples are the authoritative quality bar for all PTM authoring. Issue #28 brief amended accordingly.

---

## Amendment — Coaching Response Format (issue #30)

**Date:** 2026-09-30

Two validated example outputs were reviewed in full (spaceship drawing, depth advice scenario and reference-image match scenario). Both follow an identical structure that is not yet specified anywhere in the project. Issue #30 captures this as a formal Response Format Specification (`docs/specs/response-format.md`).

### The pattern

```
Goal statement (one sentence, plain English, no theory terms)

Technique blocks (2–5):
  - Heading: plain-English name (never academic term)
  - Current state: what is in THIS image right now (specific, descriptive, not evaluative)
  - Steps: numbered, software-level, tool-named
  - Why it works: one plain-English sentence describing the observable change

Quick exercise: tool + setting + action + observable result. Low-risk, fast, reversible.
```

For reference-image comparisons: "In your reference, X. Right now, your image has Y." + gap-closing steps. If the user's image offers better opportunities than the reference, the agent notes and builds on them.

### The corpus-as-engine principle

This is the key architectural consequence: the corpus (theory, §8 failure modes, fundamentals) is the reasoning behind every technique block. It never surfaces on the response side. The evidence rule (every claim traces to a Tier 1 source) is enforced at the ICL layer. The user sees technique steps, not citations or section numbers.

### Downstream effects

- #27 (output register): must reference the response format spec and state the corpus-as-engine principle explicitly
- #3 (guardrail spec): deflections redirect into a technique block, not a flat refusal
- #28 (PTM): scope expanded to include software tool vocabulary used in steps
- #7–21 (knowledge files): Plain-English Guide sections are the raw material for technique blocks; write them with the response format in mind
