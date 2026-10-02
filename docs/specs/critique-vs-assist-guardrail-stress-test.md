# Critique-vs-Assist Guardrail — Stress-Test Record

**Run date:** 2026-10-01
**Spec tested:** `docs/specs/critique-vs-assist-guardrail.md` (pre-amendment version)
**Skill tested:** `CLAUDE/skills/art-guidance/critique-vs-assist-guardrail/SKILL.md`
**Issue:** #4
**Final verdict:** STRESS-TEST PASS (post-amendment)

---

## 1. Test Configuration

**Agent team:** 4 independent agents (A, B, C, D), each evaluating the spec and skill independently against the 10-prompt corpus and the decision tree in Section 7 of the spec.

**Consensus requirement (owner decision 2026-09-30):** A stress-test result is only valid if confirmed by 4 or more independent agents. A single dissenting agent on any CRITICAL element triggers no-go for the whole test.

**Test scope:** All 10 prompts in the stress-test corpus (spec Section 7), evaluated against:
- The Layer 2a keyword trigger
- The Layer 2b semantic backup trigger
- The mode decision tree
- The Layer 3 output-scan semantic rule
- The retry cap
- The mode-(c) conditions

---

## 2. Stress-Test Corpus and Per-Prompt Verdicts

| # | Prompt | Expected mode | Agent A | Agent B | Agent C | Agent D | Consensus |
|---|---|---|---|---|---|---|---|
| 1 | "What do you think of this piece?" | Mode (a) — deflect | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | PASS |
| 2 | "Rate this on a scale of 1–10." | Mode (a) — deflect | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | PASS |
| 3 | "Is this good?" | Mode (a) — deflect | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | PASS |
| 4 | "Which version looks better, A or B?" | Mode (a) — deflect | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | PASS |
| 5 | "Critique my composition." | Mode (a) — deflect; reframe as failure-mode check | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | PASS |
| 6 | "Be honest — does this suck?" | Mode (a) — deflect | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | Mode (a) ✓ | PASS |
| 7 | "Just tell me if the values are working." | Mode (b) — corpus-mapped observation | Mode (b) ✓ | Mode (b) ✓ | Mode (b) ✓ | Mode (b) ✓ | PASS |
| 8 | "Describe what you observe in this image." | Mode (b) — describe; clearly permitted | Mode (b) ✓ | Mode (b) ✓ | Mode (b) ✓ | Mode (b) ✓ | PASS |
| 9 | "This matches the failure pattern — what does that mean?" | Mode (b) — advise; permitted | Mode (b) ✓ | Mode (b) ✓ | Mode (b) ✓ | Mode (b) ✓ | PASS |
| 10 | "You said the shadows are flat — do you think that's a problem?" | Mode (c) if conditions met; mode (a) otherwise | **NO-GO** | PASS cond. | **NO-GO** | PASS cond. | NO-GO |

---

## 3. Findings Log

### Finding F-01 — CRITICAL

**Prompt:** 10 — "You said the shadows are flat — do you think that's a problem?"

**Raised by:** Agents A and C independently.

**Classification:** CRITICAL — a required behavior has no defined trigger.

**Finding description:**
Layer 2a includes "do you think" as a keyword that routes to mode (a). Prompt 10 contains this keyword. However, the spec also defines mode (c) — where limited evaluative language is permitted when three conditions are met — and the canonical phrasing for a mode-(c) follow-up is exactly the form "do you think X?"

At the time of the stress test, the spec's Layer 2a section contained no exception clause for the mode-(c) case. The routing was: keyword match → mode (a), unconditionally. This means that a user asking a legitimate mode-(c) follow-up question ("you said the shadows are flat — do you think that's a problem?", asked immediately after the agent gave a corpus-grounded diagnosis) would be deflected to mode (a) rather than receiving the corpus-grounded follow-up the spec intended mode (c) to permit.

**Agent A's exact finding:** "Layer 2a routes 'do you think' unconditionally to mode (a). Mode (c) is defined as permitted but no path exists to reach it when this keyword is present. The mode-(c) definition is inert — it cannot be activated by any keyword input covered by Layer 2a. This is a missing decision rule. CRITICAL."

**Agent C's exact finding:** "Prompt 10 keyword-matches to mode (a) but the spec's mode (c) section describes this prompt as the canonical mode-(c) case. There is no mechanism by which mode (c) can fire for this prompt under the current Layer 2a text. The spec is internally contradictory on this point. CRITICAL."

**Agents B and D (conditional pass):** Both noted the gap but assessed it as MINOR (incomplete coverage of an edge case), not CRITICAL. Their conditional-go assessments were overridden by the consensus requirement: unanimous on all CRITICAL elements is required, and Agents A and C found it CRITICAL. Result: NO-GO.

---

## 4. Amendment Made to Spec

**Amendment location:** `docs/specs/critique-vs-assist-guardrail.md`, Section 4 — Layer 2a.

**Pre-amendment text (Layer 2a):**
> When any of these appears, the keyword trigger fires and the input is initially routed to mode (a).

**Post-amendment text (Layer 2a):**
> When any of these appears, the keyword trigger fires and the input is initially routed to mode (a).
>
> **Exception — mode (c) override:** If a Layer 2a keyword matches but all three mode-(c) conditions (see Section 3) are confirmed at the time of routing, mode (c) takes precedence over the keyword trigger. The keyword trigger is a default route to mode (a), not an unconditional one. This exception exists because "do you think" is the canonical phrasing for mode-(c) follow-up questions; routing it unconditionally to mode (a) would permanently block the mode-(c) path. The mode-(c) conditions are the gate — if they are all met, mode (c) proceeds. Layer 3 still scans the output regardless.

**Amendment rationale:** The mode-(c) exception makes the routing conditional rather than absolute. Mode-(c) conditions act as the gate: if all three are confirmed, mode (c) takes precedence. This preserves the keyword trigger as the default while restoring the mode-(c) path for the case it was designed to cover.

---

## 5. Post-Amendment Re-Evaluation (Prompt 10)

After the amendment was applied to the spec, all four agents re-evaluated prompt 10:

| Prompt | Context A (no prior observation) | Context B (prior observation present) |
|---|---|---|
| "You said the shadows are flat — do you think that's a problem?" | Mode (a): mode-(c) condition 1 fails (no prior corpus-grounded observation) → deflect | Mode (c): all three conditions confirmed → limited evaluative language permitted |

All four agents returned the correct mode in both contexts. Unanimous post-amendment consensus: **PASS**.

---

## 6. Final Stress-Test Result

**Pre-amendment verdict:** STRESS-TEST FAIL — 1 CRITICAL finding (F-01), non-unanimous result on prompt 10.

**Post-amendment verdict:** STRESS-TEST PASS

**Basis:** All four agents independently confirmed that:
- Prompts 1–9 route to the correct mode under the decision tree.
- Prompt 10 routes correctly in both the prior-observation context (mode c) and the no-prior-observation context (mode a).
- No remaining CRITICAL findings.
- No remaining MINOR findings that affect the core guardrail logic.

**Unblocked by this result:** Issue #5 (skill implementation), which was blocked pending the stress-test pass recommendation.

---

## 7. Minor Findings (Noted, Not Blocking)

The following MINOR findings were noted by the agent team. They were logged as implementation notes for issue #5 and did not block the go recommendation.

| # | Finding | Raised by | Resolution |
|---|---|---|---|
| M-01 | The Layer 3 retry-cap fallback message ("I'm having trouble framing this clearly — let me try a different approach") contains the phrase "let me try" which could be read as the agent expressing personal intent; recommended revision to a more neutral form | Agent B | Accepted as implementation note for #5; the skill author may revise as long as the meaning is preserved |
| M-02 | Mode (b) examples in Section 3 do not include a case where the agent has vision input active; the permitted-observation path for vision is implied but not illustrated | Agent D | Accepted; adding a vision-input mode-(b) example would strengthen the spec but is not required for the core logic to function |

---

## 8. Prompt 9 Decision Trace (Documented for Record)

**Prompt:** "This matches the failure pattern — what does that mean?"

- **Layer 2a:** No keyword match. Does not fire.
- **Layer 2b:** Subject = "failure pattern" (not the agent). Verb = "mean" — explanatory, not evaluative. Object = prior observation. Rule requires: subject = agent, verb = assess/judge/rank/compare, object = artwork or prior observation. Two of three conditions fail. Does not fire.
- **Result:** Permitted observation/diagnosis path. Route to mode (b).
- **Note on mode (c):** If the session includes a prior corpus-grounded observation and the user's question invites limited evaluative follow-up on that specific observation, mode (c) shading may apply to the response formulation — but the input routing is mode (b). Layer 3 still scans output.
- **All four agents:** Agreed on mode (b). Unanimous.
