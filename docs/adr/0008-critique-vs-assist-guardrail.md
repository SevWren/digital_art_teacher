# ADR-0008 — Critique-vs-Assist Guardrail Architecture

**Date:** 2026-10-02
**Status:** Accepted

---

## Context

The authorship boundary rule states that the user makes every aesthetic judgment; the agent describes, observes, and diagnoses. In practice, users regularly make requests that cross this boundary — asking for verdicts on whether their work is good, comparisons between alternatives, or ratings of quality. The question is: what should the agent do when such a request arrives?

Three candidate responses were considered:

1. **Flat refusal** — the agent declines the request and explains why it cannot comply.
2. **Compliance** — the agent provides the requested critique on the grounds that the user explicitly asked for it.
3. **Redirect into a technique block** — the agent intercepts the request before responding, identifies what underlying technical need the user is trying to address, and redirects into a technique-focused response without producing a verdict.

An additional structural question: should the guardrail be a one-time check at the start of a response, or a multi-layer protocol that inspects both input and output?

---

## Decision

**Option 3 — Redirect into a technique block, implemented as a three-layer protocol.**

**Rationale:**

Flat refusal leaves the user's underlying need unmet. If a user asks "is my lighting bad?" they are almost certainly trying to improve their lighting — they are not merely seeking an opinion. Refusing to engage abandons them at the moment they are asking for help.

Compliance violates the authorship boundary. The agent producing a quality verdict — even when asked — puts aesthetic judgment into agent output, which normalises the agent's taste as a standard the user should conform to. The project's pedagogical model is that the user develops their own judgment; the agent's role is to surface what is technically present and what the corpus says about it.

The redirect resolves both problems: it meets the user's need (they get useful technique guidance) without producing a verdict (they get description and corrective action, not a quality score).

The three-layer structure is necessary because:
- The same request may be prohibited (critique mode) or permitted (description or observation mode) depending on semantic context — a single keyword check is insufficient.
- Output must also be scanned: the act of formulating a response can produce evaluative language even when the input was not a critique request.

---

## Architecture

The guardrail is implemented as three sequential layers. All three run for every response with no bypass condition.

**Layer 1 — Standing activation**
`CLAUDE.md` instructs the agent to load `CLAUDE/skills/art-guidance/critique-vs-assist-guardrail/SKILL.md` before formulating every response. This is the always-on trigger.

**Layer 2 — Input classification**
The skill classifies the incoming request into one of three modes:
- **(a) Description / observation** — the user asks what is present; permitted.
- **(b) Diagnosis** — the user asks what is causing a technical problem; permitted.
- **(c) Critique / verdict** — the user asks for a quality judgment, rating, or comparative ranking; intercepted and redirected.

Classification uses keyword detection with a semantic backup. Mode (c) requests are redirected: the agent formulates a technique block addressing the underlying technical concern without producing a verdict.

**Layer 3 — Output scan**
After formulating a response, the agent scans the draft output for evaluative clauses before delivering it. Any clause that produces a quality verdict, ranks alternatives, or expresses an aesthetic preference is removed and replaced with a plain-English observation and technique step.

---

## Consequences

- `CONTEXT.md` entries for **Guardrail**, **Description (guardrail sense)**, **Critique**, **Deflection**, **Observation**, and **Diagnosis** document the architecture's vocabulary.
- The full specification, boundary cases, worked examples, and stress-test results are in `docs/specs/critique-vs-assist-guardrail.md`.
- The stress-test record (10-prompt adversarial corpus, per-prompt verdicts, amendment log) is in `docs/specs/critique-vs-assist-guardrail-stress-test.md`.
- The response-gate (`CLAUDE/skills/art-guidance/response-gate/SKILL.md`) is the output-side complement: it checks claims (not evaluative language) before delivery. The two systems address separate concerns and both run for every response.
- Adding vision input did not change the guardrail architecture. Vision input provides a new observational channel; the description boundary and the three-layer intercept apply identically to vision-based and text-based responses.
