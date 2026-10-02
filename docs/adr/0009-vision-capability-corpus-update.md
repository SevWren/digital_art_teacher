# ADR-0009 — Vision Capability Corpus Update

**Date:** 2026-10-01
**Status:** Accepted

---

## Context

The agent's original Tier 1 corpus was built under the assumption that input would always be text-only (self-reports from users describing their images). The reference documents — `Art_Theory_Digital_Practice_Reference_v5.pdf` and `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md` — were written and annotated for a text-input model: the agent reads user descriptions, matches them against the failure-mode table, and advises accordingly.

Vision capability became available, allowing the agent to observe images directly. This created three questions the corpus did not yet address:

1. **Corpus annotation:** The reference documents contained no acknowledgment that vision input was possible. A reader of those documents — human or agent — would have no indication that direct image observation was a supported mode.

2. **Observation protocol:** The authorship boundary and description boundary rules were written for text input. They needed explicit extension to the vision case: when the agent observes an image directly, the same boundary applies — describe and diagnose, never evaluate aesthetically.

3. **Input channel architecture:** When both vision input and self-report are active simultaneously and conflict, the corpus contained no resolution protocol.

---

## Decision

**Annotate the reference document (WIP.md) at the two sections most directly affected by vision capability, and record the observation protocol for both input channels.**

The specific sections annotated:

- **§1.3 of `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md`** — the corpus scope and capability section. Annotation acknowledges that vision-capable sessions allow direct image observation and cross-references the critique-vs-assist guardrail skill for the observation-vs-evaluation boundary.

- **§7 of `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md`** — the quality-check protocol section. Annotation clarifies that the quality-check protocol applies to both text-described and directly-observed images, and that direct observation is the primary channel when vision is active.

The input-channel conflict resolution (simultaneous vision + self-report) is handled separately in ADR-0007. This ADR covers only the corpus annotation required to acknowledge vision capability.

---

## What Was Annotated

**§1.3 annotation (added 2026-10-01):**
Acknowledges that vision-capable sessions support direct image observation. States that when vision input is active, the agent observes the image and maps observations to the corpus exactly as it would map text descriptions — the description boundary and authorship boundary are unchanged. Cross-references `CLAUDE/skills/art-guidance/critique-vs-assist-guardrail/SKILL.md` for the boundary enforcement protocol.

**§7 annotation (added 2026-10-01):**
Clarifies that the quality-check protocol applies to both input channels. When vision is active, the agent applies the failure-mode table to direct observations rather than user-described observations. The agent describes what is present — not whether it is good. The authorship boundary is unchanged: aesthetic verdicts remain the user's domain regardless of input channel.

---

## Consequences

- `CLAUDE.md` Open corpus items section is updated: vision capability is listed as resolved (annotations at §1.3 and §7 committed 2026-10-01).
- No new CONTEXT.md entries are required by this ADR; the Vision input and Self-report entries (added in earlier sessions) already define the two channels. ADR-0007 defines the conflict resolution protocol.
- The critique-vs-assist guardrail (ADR-0008) applies identically to vision-based and text-based responses — no changes to the guardrail architecture are required by vision capability.
- The response-gate (Pass 1 claim check) applies to observations from vision input in the same way it applies to observations from self-reports: every technical claim must trace to a Tier 1 source.
