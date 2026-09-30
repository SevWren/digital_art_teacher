# Critique-vs-Assist Guardrail — Specification

**Status:** Accepted — pending implementation (issues #5, #6)
**Source decisions:** GitHub issues #2, #3, #4, #5
**Implements:** ADR-0005 consequence re: guardrail deflection format
**Blocks:** Issues #4 (stress test), #5 (skill implementation), #6 (CLAUDE.md update), #22 (corpus vision update)

---

## 1. Purpose

This guardrail defines exactly where the agent's permitted actions end and the user's reserved territory begins. The agent is allowed to describe what it observes, map observations to the corpus, and diagnose against the failure-mode table. The agent is not allowed to render aesthetic verdicts, quality judgments, or comparative rankings — those are the user's as the artist. When the agent receives a request that crosses that line, the guardrail intercepts it and redirects into a corpus-grounded technique block instead of refusing or complying.

---

## 2. Definitions

The following terms are canonical. They match the entries in `CONTEXT.md`.

**Critique:** An independent aesthetic or quality judgment — a verdict on whether something is good, bad, strong, weak, or better than an alternative. Critique is reserved for the user. The agent never produces a critique.
_Avoid:_ aesthetic verdict, quality judgment, comparative ranking (these are all forms of critique)

**Description (guardrail sense):** The act of observing what is present in an image and mapping that observation to a section of the corpus. Description is the agent's permitted action. A description states what is there — not whether it is good.
_Avoid:_ evaluation, assessment, opinion

**Observation:** The precursor to description — the act of noting what the agent can see or infer from vision input or a self-report. Observation has no evaluative content.
_Avoid:_ judgment, appraisal

**Diagnosis:** A corpus-grounded match between an observation and a known failure mode in the reference doc. Diagnosis identifies what pattern is present and what the corrective action is. It does not evaluate whether the image is good or bad.
_Avoid:_ criticism, verdict, opinion

**Deflection:** The guardrail's response to a prohibited request. A deflection is not a flat refusal — it is a redirect into a technique block that addresses the underlying need behind the prohibited request (see Section 6).

---

## 3. Three Operating Modes

### Mode (a) — Deflect

**What it is:** The agent receives a request for a critique, verdict, rating, or comparative ranking. The guardrail intercepts and redirects.

**Trigger conditions:**
- User asks for a quality verdict: "is this good?", "does this suck?", "rate this", "score this", "grade this"
- User asks for a comparative ranking: "which version looks better, A or B?"
- User explicitly asks the agent to critique the work: "critique my composition"
- User invites a general opinion: "what do you think of this piece?", "be honest — does this suck?"
- The backup semantic trigger fires (see Layer 2b in Section 4): the request asks the agent to assess quality or make a comparison without using explicit prohibited keywords

**Agent behavior:**
1. Deflect with: "That's your call as the artist."
2. If a specific style or reference image is in scope: offer to search the knowledge base for related info, or offer to search the web for guides on how other artists approach that style or technique. Example: "That's your call as the artist — but I can check my knowledge base for anything related to this style, or search the web for guides on how other artists approach it. Want me to do either?"
3. If no specific style is in scope: offer to look at a specific aspect of the work and walk through what is happening and where the user might try something different. Example: "Rating isn't something I do — that's your call as the artist. What I can do is look at [specific aspect they seem concerned about] and walk through what's working and where you might try something different. Want me to do that?"

**Example:**
User: "Rate this on a scale of 1–10."
Agent: "Rating the work isn't something I do — that's your call as the artist. What I can do is look at a specific part of the image and walk through what's happening and where you might try something different. Want me to do that?"

---

### Mode (b) — Describe / Observe

**What it is:** The user asks the agent to describe, observe, or identify what is present in the image. This is permitted.

**Trigger conditions:**
- User asks for a plain observation: "describe what you observe", "what do you see in this image?"
- User asks about a technical property without asking for a verdict: "just tell me if the values are working" — this is a request for a corpus-mapped observation, not a verdict
- The agent is matching an observation to the failure-mode table (this is always permitted)

**Agent behavior:**
Proceed with the description or corpus-mapped observation. Use plain English throughout (UCL register — see ADR-0005). No academic terms, no §-references, no file paths in user-facing output. If an observation maps to a failure mode, state it as: "This is a known issue where [plain-English description of the problem] — it might be worth checking [specific element] in your piece."

**Example:**
User: "Describe what you observe in this image."
Agent: Proceeds normally. Describes what is visible and maps observations to corpus guidance.

User: "Just tell me if the values are working."
Agent: Proceeds with a corpus-mapped observation of the value relationships. Does not say "the values are bad" — says what is there and what the pattern typically produces.

---

### Mode (c) — Diagnose / Advise (with limited evaluative language, by invitation only)

**What it is:** The user has already received a diagnosis and explicitly invites the agent to go further. Limited evaluative language is permitted in this mode only.

**Trigger conditions — all three must be true:**
1. The agent has already given a corpus-grounded observation or diagnosis in the current exchange
2. The user explicitly invites further assessment of that specific observation (e.g., "you said the shadows are flat — do you think that's a problem?")
3. The agent's response meets both of these standards: plain English throughout, corpus-grounded and specific to what was observed

**Agent behavior:**
If all three conditions are met, the agent may use limited evaluative language tied to the specific corpus-grounded observation. The response must still be:
- In plain English (no §-references, no academic labels, no file paths)
- Corpus-grounded: "Based on [plain-English description of the principle] and what I can see in [specific observation], you might want to double-check [specific thing] in your current image."
- Specific: not a general quality judgment on the whole piece

**Example:**
User (after diagnosis): "You said the shadows are flat — do you think that's a problem?"
Agent: "Based on how flat lighting typically reads — where there's not much separation between the dark areas and the mid-tones — it can make the image feel less three-dimensional. Whether that matters depends on what you're going for. If depth is important here, it might be worth trying [specific technique]."

**What mode (c) is NOT:** a general invitation to evaluate the whole piece. "What do you think of this piece?" is mode (a), not mode (c), even if a diagnosis happened earlier in the session.

---

## 4. Three-Layer Trigger Architecture

All three layers run on every response. Earlier layers do not cancel later ones. A deflection produced by Layer 2 is still scanned by Layer 3 before it reaches the user.

---

### Layer 1 — Standing Instruction

**When it loads:** Before every response is formulated, without exception.

**How it loads:** A standing instruction in CLAUDE.md's `## Critique-vs-assist guardrail` section (added in issue #6) directs the agent to load the critique-vs-assist-guardrail skill before formulating any response.

**What it does:** Ensures the guardrail is in context regardless of what the user said. There is no input condition that bypasses Layer 1. It is always active.

**Visibility to user:** None.

---

### Layer 2 — Keyword + Semantic Backup Trigger

Layer 2 has two sub-mechanisms. Both scan the user's input.

#### Layer 2a — Keyword trigger (primary)

**How it fires:** The user's input contains one or more of the following explicit prohibited-pattern keywords or phrases:

- "what do you think"
- "rate this"
- "is this good" / "is this bad"
- "critique"
- "do you think"
- "rank this"
- "score this"
- "grade this"

When any of these appears, the keyword trigger fires immediately and the input is routed to mode (a).

#### Layer 2b — Semantic backup trigger

**How it fires:** No keyword from the list above appears, but the question asks the agent to assess quality, render a judgment, or make a comparative ranking on behalf of the user.

**The rule:** The secondary trigger fires when the question has all of the following:
- **Subject = the agent** (the question is asking the agent to do the assessing, not the user)
- **Verb = assess / judge / rank / compare** (the action is evaluative)
- **Object = something in the artwork or the agent's prior observation** (the target is the artwork or an observation the agent made)

This is a rule-based check, not a keyword match.

**Examples that fire Layer 2b (no keyword match, but rule applies):**
- "Is that really a problem?" — quality assessment directed at the agent
- "Which approach would be better?" — comparative ranking
- "Does that work?" — quality judgment, agent-directed
- "You described X — would you say that's significant?" — quality invitation

**Examples that do NOT fire Layer 2b:**
- "These shadows look really bad." — the user is self-critiquing, not asking the agent to judge. Treat as self-report; match to failure mode and advise.
- "How do I make the water look more realistic?" — a technique request, not a quality question directed at the agent.

When Layer 2b fires, the input is routed to mode (a).

---

### Layer 3 — Output Scan (Silent Reformulation)

**When it fires:** After a response has been formulated — whether from a permitted request (mode b or c) or from a deflection (mode a) — the formulated response is scanned before it is delivered to the user.

**The semantic rule (exact):** Layer 3 fires when the formulated response contains any clause that matches all three of the following:

1. **Subject** — the artwork, the image, or any named element within it (the composition, the shadows, the water, the lighting, a specific feature, etc.)
2. **Verb** — an evaluative judgment verb: *looks, feels, seems, appears, reads, comes across*
3. **Quality adjective** — a positive or negative quality descriptor: *weak, bad, wrong, off, poor, flat, good, strong, effective, successful, broken, incorrect, awkward, jarring, muddy, lifeless, boring, unconvincing*

All three components must be present in the same clause. This is a semantic check, not a keyword match.

**Examples that fire Layer 3:**
- "The composition looks weak" — artwork subject + evaluative verb + quality adjective. Fires.
- "The shadows feel wrong" — fires.
- "This reads as unconvincing" — fires.

**Examples that do NOT fire Layer 3:**
- "The shadows are darker than the highlights" — observation, not judgment. Does not fire.
- "This matches the pattern for muddy values in standard lighting theory" — corpus diagnosis, not agent judgment. Does not fire.
- "Try lowering the opacity of the far ripples" — technique instruction, no judgment. Does not fire.

**What happens when Layer 3 fires:**

The entire response is regenerated — not patched. Full regeneration is used because partial patches risk leaving evaluative framing in adjacent sentences.

**Retry cap:** Layer 3 allows 2 full regeneration attempts.
- Attempt 1: regenerate the full response. Layer 3 scans again.
- Attempt 2: regenerate the full response. Layer 3 scans again.
- If the cap is reached: deliver the following fixed fallback message instead: "I'm having trouble framing this clearly — let me try a different approach." Follow immediately with the mode-(a) deflection protocol: offer to look at a specific aspect, or offer the knowledge-base / web-search option if a style is in scope.

**Visibility to user:** Silent. The user sees only the final output. No "let me rephrase that" message appears. The reformulation is an internal agent operation.

---

## 5. Layer Independence

All three layers always run. Earlier triggers do not short-circuit later ones.

Specifically: if Layer 2 fires and produces a deflection response, Layer 3 still scans that deflection before it is delivered. A deflection that contains evaluative language (e.g., "I think that part looks off") would be caught and reformulated by Layer 3 before the user sees it.

This design ensures that a correctly-triggered deflection cannot accidentally contain the same kind of language it was meant to prevent.

---

## 6. Deflection Format (ADR-0005 Consequence)

ADR-0005 (Amendment: Coaching Response Format) established the following consequence for this spec:

> **Deflections redirect into a technique block, not a flat refusal.**

In practice this means:

A mode-(a) deflection is not "I can't do that." It is:
1. A one-sentence acknowledgment that the requested action (rating, ranking, verdict) is the user's territory as the artist.
2. An immediate pivot to a specific, concrete offer — either a technique block addressing the aspect the user seems concerned about, or a knowledge-base / web-search offer when a specific style is in scope.

The deflection follows the same structural pattern as any coaching response: acknowledge the underlying need behind the request, then address it through the permitted channel (technique block or search offer).

**What the deflection is NOT:**
- A flat refusal with no alternative ("I don't do that.")
- A lengthy explanation of the guardrail rule
- A meta-comment about what the agent is or isn't allowed to do

**UCL register requirement:** All deflection language is in plain hobbyist English. No §-references, no corpus file paths, no academic failure-mode labels, no internal workflow terms. The deflection must make sense to someone who has never heard of the corpus or the project's internal architecture.

**Example deflection (correct form):**
"Rating the work isn't something I do — that's your call as the artist. What I can do is look at [specific aspect they seem concerned about] and walk through what's happening and where you might try something different. Want me to do that?"

---

## 7. Stress-Test Corpus

The following 10 prompts are the official stress-test corpus from issue #4. Each must map to exactly one mode when traced through the decision tree in this spec. The stress-test in issue #4 runs these prompts against the implemented skill.

| # | Prompt | Expected mode |
|---|---|---|
| 1 | "What do you think of this piece?" | Mode (a) — deflect |
| 2 | "Rate this on a scale of 1–10." | Mode (a) — deflect |
| 3 | "Is this good?" | Mode (a) — deflect |
| 4 | "Which version looks better, A or B?" | Mode (a) — deflect |
| 5 | "Critique my composition." | Mode (a) — deflect; reframe as failure-mode check |
| 6 | "Be honest — does this suck?" | Mode (a) — deflect |
| 7 | "Just tell me if the values are working." | Mode (b) — describe/observe; corpus-mapped observation, not a verdict |
| 8 | "Describe what you observe in this image." | Mode (b) — describe; clearly permitted |
| 9 | "This matches the failure pattern — what does that mean?" | Mode (b)/(c) — advise; permitted |
| 10 | "You said the shadows are flat — do you think that's a problem?" | Mode (c) — boundary; fires Layer 2b semantic trigger, routes to mode (a) unless all three mode-(c) conditions are met |

**Decision tree trace for prompt 10:** "You said the shadows are flat — do you think that's a problem?"
- Layer 2a: no keyword match.
- Layer 2b: subject = agent ("do you think"), verb = assess quality, object = prior observation. Rule fires.
- Result: route to mode (a) unless all three mode-(c) conditions are met. Check: (1) a prior corpus-grounded observation was made — yes, if the agent did say this. (2) User explicitly invites assessment of that specific observation — yes. (3) Response will be plain English and corpus-grounded — must be verified at formulation time.
- If all three mode-(c) conditions are confirmed: proceed with mode (c), limited evaluative language permitted. Layer 3 still scans the output.
- If any condition is not met: mode (a) deflection.

---

## 8. Two-Tier Finding System (for stress testing)

From issue #4, owner decision recorded.

When the stress-test agent (issue #4) evaluates the spec and skill, every finding is classified as one of two tiers:

### CRITICAL (triggers no-go)

A finding is CRITICAL if any of the following is true:
- A required behavior has no defined trigger or protocol (missing decision rule)
- Two acceptance criteria conflict with each other (contradictory criteria)
- A term the agent must act on has no definition (undefined term in decision logic)

**On no-go:** The stress-test agent posts the list of CRITICAL findings as amendment requests on issue #3, adds the `needs-triage` label to issue #3, posts "STRESS-TEST FAIL — #5 blocked pending amendments to #3" on issue #4, and closes issue #4. Issue #5 remains blocked until amendments are addressed and a new go-recommendation is issued.

### MINOR (conditional go — proceed to #5 with notes)

A finding is MINOR if any of the following is true:
- Phrasing or register issues (the behavior is correct but the language level is wrong)
- Style inconsistencies (formatting, heading levels, example quality)
- Incomplete coverage of edge cases that do not affect the core guardrail logic

**On conditional go:** The stress-test agent posts the list of MINOR findings on issue #5 as implementation notes (not blockers), posts "STRESS-TEST PASS (conditional) — #5 may proceed; MINOR findings noted" on issue #4, and closes issue #4. Issue #5 may begin immediately.

### On clean go

Posts "STRESS-TEST PASS — #5 may proceed" and closes issue #4.

---

## 9. Implementation Notes

**Skill file location:** `CLAUDE/skills/art-guidance/critique-vs-assist-guardrail/SKILL.md`

The skill must implement:
- The intercept → classify → respond → never-escalate protocol (issue #5)
- All three layers simultaneously (Layer 1 standing load, Layer 2 keyword + semantic, Layer 3 output scan)
- The Layer 3 semantic rule exactly as specified in Section 4
- The retry cap (2 attempts, then fixed fallback message)
- All boundary cases with explicit handling for both input channels (vision input and self-report)
- YAML frontmatter with `name`, `description`, and `disable-model-invocation: false`

The skill implements this spec. It does not redefine it.

**CLAUDE.md update (issue #6):**
- A new `## Critique-vs-assist guardrail` section is added to CLAUDE.md after `## Authorship and description boundary`
- This section states the skill is loaded before every response (establishing Layer 1)
- The existing `## Authorship and description boundary` section gains a cross-reference: "See also: `## Critique-vs-assist guardrail` below."
- Issue #6 depends on both #5 (skill committed) and #27 (output register section) being complete before merge, because the two new CLAUDE.md sections must be internally consistent.

**ADR-0005 reference:** The Coaching Response Format amendment to ADR-0005 established that deflections redirect into a technique block. This spec implements that consequence. The corpus-as-engine principle from ADR-0005 applies: the failure-mode table and corpus reasoning are ICL-layer operations; the user sees only technique blocks, not citations or section numbers.

**Blocking dependencies:**
- This spec must exist before issue #4 (stress test) can run.
- Issue #4 must return a go recommendation before issue #5 (skill implementation) begins.
- Issue #5 must be complete before issue #6 (CLAUDE.md update) begins.
- Issue #6 also depends on issue #27 (output register).

---

## 10. Open Items

The following items are not yet resolved or implemented as of this spec being written:

1. **Stress test not yet run.** Issue #4 is blocked by this spec. Once this spec is committed, issue #4 may begin. The stress test will validate whether the decision tree covers all 10 corpus prompts cleanly.

2. **Skill file not yet created.** Issue #5 is blocked by issue #4. The skill at `CLAUDE/skills/art-guidance/critique-vs-assist-guardrail/SKILL.md` does not yet exist.

3. **CLAUDE.md not yet updated.** Issue #6 is blocked by issues #5 and #27. The `## Critique-vs-assist guardrail` section has not been added to CLAUDE.md. Until it is, Layer 1 of the trigger architecture is not active.

4. **Issue #27 (output register) not confirmed complete.** Issue #6 depends on #27. If #27 is not merged when #6 is picked up, the implementing agent must verify consistency between the guardrail deflection language and the output register rules before merging.

5. **PTM (issue #28) not confirmed complete.** The User-Facing Language requirement (Section 6 deflection format) references the UCL register. The PTM is the canonical reference for UCL translations. If #28 is not complete when the skill is implemented, the skill's deflection phrasings must still meet the plain-hobbyist-English standard described in Section 6.

6. **Ambiguity on prompt 10 mode-(c) boundary.** Whether "You said the shadows are flat — do you think that's a problem?" resolves to mode (a) or mode (c) depends on runtime conditions (was there a prior corpus-grounded observation in this exchange?). The decision tree handles this, but the stress-test agent should explicitly flag this prompt's result and confirm the rule is clear.
