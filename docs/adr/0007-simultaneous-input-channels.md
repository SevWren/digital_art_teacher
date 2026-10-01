# ADR-0007 — Simultaneous Input Channels: Vision and Self-Report

**Date:** 2026-10-01
**Status:** Accepted

---

## Context

The domain model defines two input channels:

- **Vision input:** the user uploads an image; the agent observes it directly.
- **Self-report:** the user describes their image in text; the agent works from the description.

In normal usage these channels are independent. The unresolved edge case is: what should the agent do when **both channels are active simultaneously** — i.e. the user uploads an image *and* describes it in text, and the two sources of information conflict?

Example conflict: the user uploads a painting and writes "my shadows look too warm," but the agent observes from the image that the shadows are in fact cool-toned. The self-report and the visual evidence disagree.

Three candidate resolutions were considered:

1. **Vision takes precedence** — the agent uses what it can directly observe; the self-report is treated as supplementary context.
2. **Self-report takes precedence** — the user's stated description is authoritative; the agent does not override the user's own account of their work.
3. **Both coexist with discrepancy flagging** — the agent treats vision as the observational channel and self-report as the intentional/contextual channel; when they conflict, the agent flags the discrepancy and asks the user to clarify before proceeding.

---

## Decision

**Option 3 — Both coexist with discrepancy flagging.**

**Rationale:**

Vision provides the most reliable observational data but cannot capture the user's intent. Self-report may reflect intent, expectation, or focus area rather than an objective description — the user saying "my shadows look too warm" may mean "I intended warm shadows and they don't feel right" rather than describing a literal warmth that is visible in the image.

The authorship principle requires that the agent never override the user's judgment. Silently discarding self-report in favour of vision would do exactly that, and could cause the agent to misrepresent the user's stated concern.

At the same time, the agent has a responsibility to describe what is actually observed — not to validate a description that contradicts direct visual evidence.

The resolution: **use both channels together**, treating vision as the primary observational channel and self-report as context for intent and focus area. When the two conflict materially — i.e. when the observational finding from vision is inconsistent with the user's stated description — the agent **flags the discrepancy plainly** and **asks the user to clarify** before proceeding. This keeps the user in control of their own account while surfacing the mismatch rather than silently choosing one channel over the other.

---

## Protocol

When both input channels are active in the same turn:

1. **Use vision as the observational channel.** Describe what is observed in the image.
2. **Use self-report as the intentional/contextual channel.** It tells the agent where the user's attention is and what they expect to find.
3. **If vision and self-report agree:** proceed normally.
4. **If vision and self-report conflict materially:**
   - Describe what the agent observes from the image.
   - Note plainly that this differs from the user's description.
   - Ask the user to clarify before the agent proceeds with advice.
   - Example form: "From the image I can see [observation]. You mentioned [self-report], which is different — could you point out the area you're looking at? I want to make sure I'm responding to the right thing."
5. **Never silently discard either channel.** The discrepancy itself is information.

A material conflict is one where acting on the wrong channel would produce incorrect or misleading technique guidance. Trivial mismatches (e.g. the user says "the tree" and there are two trees in the image) are resolved by asking a targeted clarification question, not treated as a full discrepancy.

---

## Consequences

- `CONTEXT.md` entries for **Vision input** and **Self-report** are updated to document this resolution.
- The critique-vs-assist guardrail skill is unaffected — the discrepancy-flagging step produces an observation and a clarifying question, not a critique.
- The response-gate (claim gate) applies to any advice produced after clarification in the normal way.
