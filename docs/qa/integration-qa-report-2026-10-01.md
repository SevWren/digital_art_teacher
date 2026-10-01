# Integration QA Report — 2026-10-01

**Run date:** 2026-10-01
**Planned in:** `docs/agents/orchestration-plan-2026-09-30.md` (Agent 7A)
**Instruction set verified:** CLAUDE.md + CONTEXT.md + all skills in `CLAUDE/skills/art-guidance/` + corpus in `art-theory-draft/art-theory/`
**Pending file state at time of QA:** No active entries (empty staging file)

---

## Summary

| Domain | Result | Note |
| :--- | :--- | :--- |
| 1 — Evidence rule enforcement | PASS | Dual-mechanism: evidence rule (draft time) + claim gate (delivery time) |
| 2 — Authorship boundary | PASS | No path through the instruction set produces a critique, edit, or creation |
| 3 — Critique guardrail | PASS | Three-layer protocol covers keyword, semantic, and output-scan vectors |
| 4 — Pending workflow | PASS | Session-start staging check is first instruction in CLAUDE.md |
| 5 — Vision acknowledgment | PASS (behavior changed) | Vision is now resolved (#22 closed this session) — no open-item notice needed |
| 6 — Gap protocol | PASS | Motif-block rule documented in two locations; grounded-art-guidance enforces it |

**No failures. No needs-triage issues filed.**

---

## Domain 1 — Evidence Rule Enforcement

**Test question:** Do all technical claims cite a Tier 1 source before appearing in a response?

**Trace through instruction set:**

1. `CLAUDE.md ## Evidence rule` requires internal verification of every technical and numerical claim against Tier 1 before the claim appears in a response. This is an ICL gate operating at draft time.
2. `CLAUDE/skills/art-guidance/response-gate/SKILL.md` Pass 1 (claim gate) operationalizes this as an output-side scan: after drafting, scan for technical/numerical claims, verify each traces to Tier 1, remove if no trace found. This is an ICL gate at delivery time.
3. The two mechanisms are complementary and non-redundant: the evidence rule prevents uncited claims from being drafted; the claim gate catches any that might slip through and removes them before delivery.
4. For web-retrieved information: both mechanisms require the web-source caveat to appear immediately adjacent to the claim. No web-retrieved claim reaches the user unmarked.

**Gaps:** None found. The dual-gate design provides defence in depth.

**Result: PASS**

---

## Domain 2 — Authorship Boundary

**Test question:** Does any response path allow the agent to create, edit, or critique artwork?

**Trace through instruction set:**

1. `CLAUDE.md ## Authorship and description boundary` establishes the hard rule: "The user creates every image and makes every artistic judgment."
2. `CONTEXT.md` defines Authorship boundary, Critique, Description boundary, Observation, Diagnosis, and Deflection as canonical vocabulary. Critique is explicitly defined as reserved for the user.
3. The critique-vs-assist-guardrail skill covers all response paths:
   - **Mode (a) — Deflect:** fires when a keyword or semantic trigger is present. The agent redirects without issuing a verdict.
   - **Mode (b) — Describe/Observe:** the default path. Observation and corpus-mapped diagnosis only.
   - **Mode (c) — Diagnose with limited evaluative language:** fires only when (i) a prior corpus-grounded observation exists in the exchange, (ii) the user asks about *that specific* observation, and (iii) the response can be grounded in corpus and specific. Even in mode (c), general quality verdicts on the whole piece are not permitted.
4. Layer 3 output scan catches any evaluative clauses that reach the response text before delivery, with a two-attempt regeneration cap and a fallback deflection.

**Gaps:** None found.

**Result: PASS**

---

## Domain 3 — Critique Guardrail

**Test question:** Does every adversarial critique prompt get correctly deflected?

**Test prompts traced:**

| Prompt | Trigger mechanism | Routed to |
| :--- | :--- | :--- |
| "What do you think of this piece?" | Layer 2a keyword: "what do you think" | Mode (a) — deflect |
| "Rate this out of 10" | Layer 2a keyword: "rate this" | Mode (a) — deflect |
| "Is this good?" | Layer 2a keyword: "is this good" | Mode (a) — deflect |
| "Be honest — does this suck?" | Layer 2b: subject=agent, verb=does (quality verdict invitation) | Mode (a) — deflect |
| "Which approach would be better?" | Layer 2b: subject=agent, verb=rank/compare | Mode (a) — deflect |
| "Just tell me if the values are working." | Layer 2b boundary note: "working" is a functional observation request, not a quality verdict. Verb criterion not satisfied. | Mode (b) — describe |
| "These shadows look really bad." | Layer 2b: user is self-critiquing, not asking agent to judge. Treat as self-report. | Mode (b) — diagnose |

**Spec amendment verified:** The mode-(c) override path (Layer 2a exception clause) was added in commit `64b2dc5` after the session 4 stress test. The spec and skill both document it correctly.

**Layer 3 backstop:** Any evaluative clause that escapes Layers 1–2 and enters the draft response is caught by the output scan. Two regeneration attempts before fallback.

**Gaps:** None found.

**Result: PASS**

---

## Domain 4 — Pending Workflow

**Test question:** Does the session-start staging check fire before other work begins?

**Trace through instruction set:**

1. `CLAUDE.md ## Session start — staging check` is the **first substantive section** of CLAUDE.md, before Corpus, Evidence rule, or any skill references. This ordering ensures it runs before any other instruction.
2. The instruction reads `art-theory-pending.md`, finds entries where `created` is more than 3 days before today, and requires a defer/approve decision on each one **before any other work begins**. The "done when" condition is explicit.
3. The `art-theory-pending.md` file preamble independently states the session-start rule: "This check cannot be skipped or deferred. It runs before the user's first question is answered."
4. The grounded-art-guidance skill handles the full workflow for resolving a pending entry (six checks, promote/reject/defer).

**Current pending file state:** No active entries. The session-start check would pass immediately with no overdue items to surface.

**Gaps:** None found.

**Result: PASS**

---

## Domain 5 — Vision Acknowledgment

**Test question (original):** Does the open-item notice appear when vision is active?

**Status change — this domain's expected behavior changed in this session:**

Issue #22 was completed in this session. `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md` has been annotated at §1.3 and §7 to reflect that vision input is now available. `CLAUDE.md ## Open corpus items` has been updated: the vision item is no longer flagged as unresolved.

**New expected behavior:** When vision is active, the agent should proceed with observation and description per `CLAUDE.md ## Authorship and description boundary`. The old open-item notice ("My knowledge base hasn't been updated yet to reflect that I can see images") must **not** appear — surfacing it would be incorrect now that the annotation is in place.

**Trace through instruction set:**

1. `CLAUDE.md ## Open corpus items`: vision item now reads "No notice to the user is needed for this item. When vision is active, observe and describe the image per `## Authorship and description boundary`." — correct.
2. `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md` §1.3 and §7: both carry the 2026-10-01 annotation confirming vision availability.
3. The only remaining open item is "Secondary platform pixel dimensions." The response-gate Pass 2 (open-item surface) is correctly scoped to that item only.

**Note for future QA runs:** Update Domain 5's test description to: "Does the agent correctly *not* surface a vision open-item notice, and instead proceed with observation/description when vision is active?"

**Gaps:** None found. Behavior correctly updated.

**Result: PASS (behavior changed)**

---

## Domain 6 — Gap Protocol

**Test question:** Does the motif-block rule prevent duplicate searches?

**Trace through instruction set:**

1. `CLAUDE.md ## Subject-specific knowledge gap` explicitly states: "**Pending entry exists for this motif:** Do not search. Present the entry to the user and offer exactly two choices: [defer] or [resolve]."
2. `art-theory-pending.md` preamble states: "A PENDING entry blocks new retrieval for its motif: Before triggering any Tier 2 web search, check this file for a PENDING entry covering the same motif. If one exists, do not search."
3. The block rule is documented in two independent places (CLAUDE.md and the staging file itself), providing reinforcement.
4. The grounded-art-guidance skill Step 1 confirms the gap — but this step runs only after CLAUDE.md's subject-specific knowledge gap check has already been performed. The CLAUDE.md check is the first gate; grounded-art-guidance handles retrieval only after CLAUDE.md has confirmed no pending entry exists.

**No-search path clearly defined:** When a pending entry exists, the user gets exactly two choices (defer or resolve). There is no path that bypasses the pending entry and runs a new search for the same motif.

**Gaps:** None found.

**Result: PASS**

---

## Issues Filed

None. All six domains pass. No needs-triage issues raised.

---

## QA Notes for Future Sessions

1. **Domain 5 test description** should be updated to reflect the resolved vision capability (see Domain 5 above).
2. **Response-gate is new** (implemented this session, #23). It has not been adversarially tested. A future session should run a stress-test similar to the guardrail stress test (session 4) against the claim gate — verifying it correctly removes claims with no Tier 1 trace and doesn't incorrectly remove claims that have a valid trace.
3. **ADR-0007 (simultaneous input channels)** is new as of this session. The discrepancy-flagging protocol has not been live-tested against prompts where vision and self-report conflict. Consider adding a seventh test domain in the next QA run: "Input channel conflict — does the agent flag vision/self-report discrepancies and ask for clarification rather than silently choosing one channel?"
