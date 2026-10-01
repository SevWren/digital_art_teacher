---
name: response-gate
description: Two-pass ICL gate that runs after drafting a response and before delivery. Pass 1 is the claim gate (every technical/numerical claim must trace to Tier 1). Pass 2 is the open-item surface (responses touching tracked open items must include the correct acknowledgment).
disable-model-invocation: true
---

# Response Gate

Run this skill after drafting a response and **before** delivering it to the user. Both passes are ICL-only — nothing from this skill ever appears in user-facing output except the prescribed acknowledgment text in Pass 2.

---

## Pass 1 — Claim Gate

**Trigger:** Any drafted response that contains a technical or numerical claim.

A **technical or numerical claim** is any of the following in the response:
- A specific pixel dimension, DPI, colour profile value, or resolution figure
- A percentage or ratio tied to a technique (e.g. "80% of your shadows should…")
- A technique prescription stated as fact (e.g. "you must always use three light sources")
- Any comparative or absolute assertion about art practice that is not common knowledge

**Procedure:**

1. Scan the drafted response for technical and numerical claims.
2. For each claim found, trace it internally to a Tier 1 source:
   - `Art_Theory_Digital_Practice_Reference_v5.pdf`
   - `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md`
   - A file in `art-theory-draft/art-theory/` (confirmed in INDEX.md)
3. For each claim that **has a trace:** proceed. The trace is internal — the source path never surfaces in the response.
4. For each claim that **has no trace:**
   - Re-check Tier 1. If the trace is found on re-check, proceed.
   - If no trace found after re-check: **remove the claim from the response.** Replace it with a technique step grounded in what Tier 1 does say, or omit it entirely.
5. For any claim that came from web retrieval: confirm the web-source caveat is present immediately adjacent to that claim:
   > *[Web source: [URL(s)] — not yet verified against the three-source standard.]*
   If the caveat is absent, add it before delivering.

**Exit condition:** Every technical and numerical claim in the response either (a) traces to Tier 1, or (b) carries the web-source caveat. No uncited technical claim reaches the user.

---

## Pass 2 — Open-Item Surface

**Trigger:** Any drafted response that touches a tracked open item.

**Tracked open items (current):**

| Item | Condition that triggers acknowledgment |
| :--- | :--- |
| Secondary platform pixel dimensions | Response contains any platform-specific pixel dimension for social media, print-on-demand, or app stores |

**Procedure:**

1. Scan the drafted response for content matching the trigger conditions above.
2. If a trigger condition is met, verify that the response **does not fabricate a platform-specific dimension** and **does direct the user to verify against the platform's current official documentation**.
3. Correct form — include in the response:
   > "Platform specifications change — check the platform's current help centre for the exact dimensions before you export."
   (UCL register: plain English, no internal workflow terms.)
4. If the response already contains a direction to verify against official documentation, no addition is needed.

**Exit condition:** No fabricated platform-specific pixel dimension reaches the user. Any response touching this item directs the user to the platform's official documentation.

---

## Gate summary

| Pass | What it checks | Failure action |
| :--- | :--- | :--- |
| 1 — Claim gate | Every technical/numerical claim traces to Tier 1 or carries a web-source caveat | Remove the uncited claim or add the caveat |
| 2 — Open-item surface | Responses touching tracked open items include the correct acknowledgment | Add the prescribed acknowledgment text |

Both passes are invisible to the user. Only the corrected response is delivered.
