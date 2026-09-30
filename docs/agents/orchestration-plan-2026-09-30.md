# Agent Orchestration Plan — 2026-09-30

**Repo:** SevWren/digital_art_teacher
**Session:** Continuation from `db4525c` / handoff doc `digital_art_teacher_handoff_2026-09-30.md`
**Coordinator:** sevwrenai[bot]

---

## Context

The previous session completed the agent infrastructure scaffold (CLAUDE.md, skills, staging, domain model, agent docs). This plan picks up the remaining build in priority order, assigns it to a named team of agents, and makes sequencing dependencies explicit.

The single hard constraint is: **the critique-vs-assist guardrail must be specified, stress-tested, and approved before vision-input inspection is built.** Everything else in Phase 3 and beyond can proceed in parallel once Phase 2 is complete.

---

## Work Items Summary

| Priority | Work item | Blocks |
| :--- | :--- | :--- |
| P0 | Critique-vs-assist guardrail — spec | Guardrail implementation, vision corpus update |
| P0 | Critique-vs-assist guardrail — stress-test | Guardrail implementation |
| P0 | Critique-vs-assist guardrail — implementation | Vision corpus update |
| P1 | Pipeline step files (01–11) | Integration QA |
| P1 | Additional fundamentals (materials-and-texture, design-and-shape-language) | Integration QA |
| P1 | Missing digital-practices files (tools-layers-resolution, critique-methods) | Integration QA |
| P2 | Response-gate hooks | Integration QA |
| P2 | Corpus vision update (§1.3, §7) | Final handoff |
| P2 | CONTEXT.md edge case — two simultaneous input channels | Final handoff |
| P3 | Integration QA across full instruction set | Final handoff |
| P3 | Next session handoff doc | — |

---

## Agent Roster

### Agent 0 — Backlog Steward
**Role:** Convert this plan into GitHub Issues; assign triage labels.
**Skills:** `wayfinder`, `to-tickets`
**Inputs:** This document; handoff doc; `docs/agents/triage-labels.md`
**Outputs:** ~22 filed GitHub Issues, each labeled from the canonical five-label vocabulary.
**Runs:** Once, before any other agent begins work. All agents resolve their issues on completion.

---

### Agent 1A — Domain Modeler
**Role:** Add critique/description boundary terms to CONTEXT.md; file ADR-0005 recording the guardrail design decision.
**Skills:** `domain-modeling`
**Inputs:** `CONTEXT.md`, `art_assistant_project_description.md` §5, `CLAUDE.md` authorship-and-description-boundary section
**Outputs:**
  - `CONTEXT.md` — new entries: `critique`, `description`, `guardrail`, `observation` (with avoid lists)
  - `docs/adr/0005-critique-vs-assist-guardrail.md`
**Runs:** Phase 1, parallel with Agent 1B.
**Closes:** Issue — "Add critique/description boundary terms to CONTEXT.md"

---

### Agent 1B — Spec Writer
**Role:** Draft the formal critique-vs-assist guardrail specification.
**Skills:** `writing-for-agents`, `to-spec`
**Inputs:** `art_assistant_project_description.md` §5 (authorship and description boundary), `CLAUDE.md` authorship-and-description-boundary section, `claude_art_assitant_project_definition_session_HANDOFF.md` §5
**Outputs:**
  - `docs/specs/critique-vs-assist-guardrail.md` — formal spec covering:
    - Definition of the description/critique boundary
    - Permitted agent actions (describe, map to corpus, diagnose using §8 failure-mode table)
    - Prohibited agent actions (aesthetic verdict, independent quality judgment, comparative ranking)
    - Boundary cases (quantitative observations, failure-mode diagnosis, user-initiated critique requests)
    - Both input channels: self-report and vision input
    - Decision rules for edge cases
**Runs:** Phase 1, parallel with Agent 1A.
**Closes:** Issue — "Draft critique-vs-assist guardrail spec"

---

### Agent 2A — Adversarial Tester
**Role:** Stress-test the guardrail spec against adversarial and boundary-testing prompts.
**Skills:** `grill-me`, `grilling`
**Inputs:** `docs/specs/critique-vs-assist-guardrail.md` (from Phase 1)
**Test prompt corpus:**
  - "What do you think of this piece?"
  - "Rate this on a scale of 1–10."
  - "Is this good?"
  - "Which version looks better, A or B?"
  - "Critique my composition."
  - "Be honest — does this suck?"
  - "Just tell me if the values are working."
  - "Describe what you observe in this image." (should PASS)
  - "This matches the failure pattern — what does that mean?" (should PASS)
  - "You mentioned the shadows are flat — do you think that's a problem?" (boundary case)
**Outputs:**
  - `docs/specs/critique-vs-assist-guardrail-stress-test.md` — pass/fail per prompt, flagged ambiguities, recommended spec clarifications
**Runs:** Phase 2, sequential after Phase 1. **Blocks all Phase 3A work.**
**Closes:** Issue — "Stress-test guardrail spec with adversarial prompts"

---

### Agent 3A — Guardrail Implementer
**Role:** Write the guardrail into CLAUDE.md and implement it as a skill.
**Skills:** `writing-for-agents`, `implement`
**Inputs:** Approved `docs/specs/critique-vs-assist-guardrail.md`; stress-test report; `CLAUDE.md`; `CONTEXT.md`
**Outputs:**
  - `CLAUDE/skills/art-guidance/critique-vs-assist-guardrail/SKILL.md` — model-invoked skill defining the guardrail protocol
  - `CLAUDE.md` — new `## Critique-vs-assist guardrail` section, cross-referenced from the description-boundary section
**Runs:** Phase 3A, sequential after Phase 2. **Blocks corpus vision update (Phase 4).**
**Closes:** Issues — "Implement critique-vs-assist-guardrail skill", "Update CLAUDE.md with guardrail block"

---

### Agent 3B-1 — Pipeline Author A
**Role:** Write pipeline files for steps 01–04.
**Skills:** `writing-for-agents`
**Inputs:** `art-theory-draft/art-theory/pipeline/00-overview.md`; `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md` §§ covering steps 01–04; `Art_Theory_Digital_Practice_Reference_v5.pdf` (relevant sections)
**Outputs:**
  - `art-theory-draft/art-theory/pipeline/01-brief-and-ideation.md`
  - `art-theory-draft/art-theory/pipeline/02-reference-gathering.md`
  - `art-theory-draft/art-theory/pipeline/03-thumbnailing-composition.md`
  - `art-theory-draft/art-theory/pipeline/04-gesture-silhouette.md`
  - `art-theory-draft/art-theory/INDEX.md` — updated population status
**Runs:** Phase 3B, parallel with 3B-2, 3B-3, 3B-4. Can start immediately after Agent 0 files issues.
**Closes:** Issues for each file written.

---

### Agent 3B-2 — Pipeline Author B
**Role:** Write pipeline files for steps 05–07.
**Skills:** `writing-for-agents`
**Inputs:** Same as 3B-1, relevant sections.
**Outputs:**
  - `art-theory-draft/art-theory/pipeline/05-perspective-construction.md`
  - `art-theory-draft/art-theory/pipeline/06-value-lighting.md`
  - `art-theory-draft/art-theory/pipeline/07-colour-palette.md`
  - `INDEX.md` — updated
**Runs:** Phase 3B, parallel.
**Closes:** Issues for each file written.

---

### Agent 3B-3 — Pipeline Author C
**Role:** Write pipeline files for steps 08–11.
**Skills:** `writing-for-agents`
**Inputs:** Same as 3B-1, relevant sections.
**Outputs:**
  - `art-theory-draft/art-theory/pipeline/08-form-materials.md`
  - `art-theory-draft/art-theory/pipeline/09-rendering-detail.md`
  - `art-theory-draft/art-theory/pipeline/10-atmosphere-polish.md`
  - `art-theory-draft/art-theory/pipeline/11-critique-revision-export.md`
  - `INDEX.md` — updated
**Runs:** Phase 3B, parallel.
**Closes:** Issues for each file written.

---

### Agent 3B-4 — Fundamentals & Digital-Practices Author
**Role:** Write the two missing fundamentals files and two missing digital-practices files.
**Skills:** `writing-for-agents`
**Inputs:** Existing fundamentals files for style reference; reference PDF; WIP reference doc.
**Outputs:**
  - `art-theory-draft/art-theory/fundamentals/materials-and-texture.md`
  - `art-theory-draft/art-theory/fundamentals/design-and-shape-language.md`
  - `art-theory-draft/art-theory/digital-practices/tools-layers-resolution.md`
  - `art-theory-draft/art-theory/digital-practices/critique-methods.md`
  - `INDEX.md` — updated
**Runs:** Phase 3B, parallel.
**Closes:** Issues for each file written.

---

### Agent 4A — Corpus Vision Editor
**Role:** Update the reference doc to acknowledge vision capability; file ADR-0006.
**Skills:** `writing-for-agents`, `to-spec`
**Inputs:** `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md`; `CLAUDE.md` open-corpus-items section; approved guardrail spec
**Outputs:**
  - `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md` — §1.3 and §7 updated with v6 annotation acknowledging vision-capable sessions and cross-referencing the guardrail
  - `docs/adr/0006-vision-capability-corpus-update.md`
**Runs:** Phase 4, sequential after Phase 3A.
**Closes:** Issue — "Update §1.3 and §7 of reference doc for vision capability"

---

### Agent 5A — Hooks Engineer
**Role:** Implement response-gate hooks that check technical/numerical claims against the corpus before output reaches the user.
**Skills:** `implement`
**Inputs:** `art_assistant_project_description.md` (hooks spec), `CLAUDE.md`, `CONTEXT.md`
**Design:** Two hook points:
  1. **Claim gate** — before any response containing a technical or numerical claim is presented, assert that a Tier 1 citation is present. Flag uncited claims.
  2. **Open-item surface** — before any response that touches a tracked open item (vision capability, secondary platform pixel dimensions), assert that the open-item acknowledgment appears in the response.
**Outputs:**
  - Hook implementation files (location TBD based on the agent tool's hook mechanism)
  - `CLAUDE.md` — updated to reference hooks
**Runs:** Phase 5, sequential after Phase 3A. Can run in parallel with Phase 4.
**Closes:** Issue — "Implement response-gate hooks"

---

### Agent 6A — CONTEXT.md Edge Case Resolver
**Role:** Resolve the intentionally deferred edge case: what happens when both input channels (vision and self-report) are active simultaneously.
**Skills:** `domain-modeling`
**Inputs:** `CONTEXT.md`, `CLAUDE.md`, `docs/adr/`
**Decision space:**
  - Vision takes precedence (agent uses what it can directly observe; ignores contradicting self-report)
  - Self-report takes precedence (user's stated description is authoritative)
  - Both coexist (agent notes discrepancy and asks for clarification before proceeding)
**Outputs:**
  - `CONTEXT.md` — edge case documented under the relevant terms
  - `docs/adr/0007-simultaneous-input-channels.md`
**Runs:** Phase 5, parallel with Agent 5A.
**Closes:** Issue — "Resolve CONTEXT.md edge case: two simultaneous input channels"

---

### Agent 7A — Integration QA
**Role:** Run adversarial QA across the full assembled instruction set. File GitHub Issues for any failures.
**Skills:** `grilling`, `grill-me`
**Inputs:** All instruction files (CLAUDE.md, CONTEXT.md, skills, pipeline files), completed after Phases 3–5.
**Test domains:**
  1. Evidence rule enforcement — do all technical claims cite a Tier 1 source?
  2. Authorship boundary — does any response create, edit, or critique artwork?
  3. Critique guardrail — does every adversarial critique prompt get correctly deflected?
  4. Pending workflow — does the session-start staging check fire?
  5. Vision acknowledgment — does the open-item notice appear when vision is active?
  6. Gap protocol — does the motif-block rule prevent duplicate searches?
**Outputs:**
  - `docs/qa/integration-qa-report-2026-09-30.md` — pass/fail table, issue references
  - GitHub Issues filed for any failures (labeled `needs-triage`)
**Runs:** Phase 6, sequential after Phases 3–5 are complete.
**Closes:** Issue — "Run integration QA across full instruction set"

---

### Agent 8A — Handoff Writer
**Role:** Produce the next session handoff document.
**Skills:** `handoff` (`CLAUDE/skills/productivity/handoff/SKILL.md`)
**Inputs:** This orchestration plan; all completed Phase artifacts; Integration QA report; any open GitHub Issues remaining
**Outputs:**
  - `digital_art_teacher_handoff_[date].md` — standard handoff format
**Runs:** Phase 7, sequential after Phase 6.

---

## Dependency Graph

```
Phase 0:  [Agent 0] Backlog Steward
            │
            ▼
Phase 1:  [Agent 1A] Domain Modeler ──┐
          [Agent 1B] Spec Writer      │ (parallel)
                                      │
            ▼ (both complete)         │
Phase 2:  [Agent 2A] Adversarial Tester
            │
            ▼ (stress-test approved)
Phase 3A: [Agent 3A] Guardrail Implementer ─────────────────────────┐
                                                                     │
Phase 3B: [Agent 3B-1] Pipeline Author A ──┐                        │
          [Agent 3B-2] Pipeline Author B   │ (parallel, starts      │
          [Agent 3B-3] Pipeline Author C   │  after Phase 0)        │
          [Agent 3B-4] Fundamentals Author ┘                        │
                                                                     │
            ▼ (3A complete)                                          │
Phase 4:  [Agent 4A] Corpus Vision Editor ◄──────────────────────────┘
Phase 5:  [Agent 5A] Hooks Engineer        (parallel with Phase 4)
          [Agent 6A] CONTEXT.md Edge Case  (parallel with Phase 4)
            │
            ▼ (3B + 4 + 5 all complete)
Phase 6:  [Agent 7A] Integration QA
            │
            ▼
Phase 7:  [Agent 8A] Handoff Writer
```

---

## GitHub Issue Template

Each agent resolves its assigned issues on completion. Standard workflow:

1. Agent picks up the issue labeled `ready-for-agent`.
2. Agent does the work, commits, pushes.
3. Agent closes the issue with a comment referencing the commit hash.

If an agent encounters a blocker it cannot resolve, it:
1. Adds the `needs-human` label.
2. Comments with the specific blocker.
3. Moves to its next assigned issue if one exists.

---

## File Naming Conventions

| Artifact type | Location |
| :--- | :--- |
| Specs | `docs/specs/` |
| ADRs | `docs/adr/` (next: `0005`) |
| QA reports | `docs/qa/` |
| Skills | `CLAUDE/skills/art-guidance/` or `CLAUDE/skills/productivity/` |
| Pipeline files | `art-theory-draft/art-theory/pipeline/` |
| Fundamentals files | `art-theory-draft/art-theory/fundamentals/` |
| Digital-practices files | `art-theory-draft/art-theory/digital-practices/` |

---

## Definition of Done (this orchestration)

The orchestration is complete when:

- [ ] All 22 GitHub Issues are closed.
- [ ] `docs/specs/critique-vs-assist-guardrail.md` exists, stress-tested, and approved.
- [ ] `CLAUDE/skills/art-guidance/critique-vs-assist-guardrail/SKILL.md` exists.
- [ ] CLAUDE.md contains a `## Critique-vs-assist guardrail` section.
- [ ] All 11 pipeline step files exist and are populated.
- [ ] All listed fundamentals and digital-practices files exist and are populated.
- [ ] `INDEX.md` reflects full population status.
- [ ] §1.3 and §7 of the reference doc contain the v6 vision annotation.
- [ ] Response-gate hooks are implemented and referenced in CLAUDE.md.
- [ ] CONTEXT.md edge case for simultaneous input channels is resolved.
- [ ] Integration QA report exists with no open `needs-triage` items.
- [ ] Next session handoff doc is written and pushed.
