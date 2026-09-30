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
