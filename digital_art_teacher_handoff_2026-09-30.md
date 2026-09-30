> **HISTORICAL SNAPSHOT — Point-in-time record. Do not treat as current project state.**
>
> This document reflects repo state at commit `db4525c` (2026-09-30). As of the same date, HEAD advanced to `f4116e5` — five additional commits were made after this document was written:
> - `a5897dc` — Enterprise agent orchestration plan added (`docs/agents/orchestration-plan-2026-09-30.md`)
> - `11c6727` — ADR-0005 (Output Register and Pedagogical Translation Layer) filed
> - `9e3bd85` — ADR-0005 Amendment 1
> - `f003884` — ADR-0005 Amendment 2
> - `f4116e5` — Validated response examples committed (`docs/specs/validated-response-examples.md`)
>
> **Before acting on any item in this document:**
> 1. Read `docs/agents/orchestration-plan-2026-09-30.md` — this is the authoritative work plan.
> 2. Check GitHub Issues at https://github.com/SevWren/digital_art_teacher/issues for current open/closed status.
> 3. Run `git log --oneline -10` to see commits made after this snapshot.
>
> **Key post-handoff changes not reflected here:**
> - ADR-0005 (accepted): Output register + Pedagogical Translation Matrix architecture. CLAUDE.md must gain an `## Output register` section (issue #27 — open).
> - "What is NOT done" / "Suggested skills" sections are materially stale — the orchestration plan covers all of this.
> - The "two input channels simultaneously — intentionally left to agent judgment" entry in the Key Decisions table is superseded: issue #24 has a formal resolution path (vision takes precedence; discrepancy surfaced to user).
> - The guardrail is now fully designed in issues #3 and #5; only the committed spec file is missing.

# Session Handoff — Digital Art Teacher (Agentic Art-Theory Assistant)

**Date:** 2026-09-30 **Repo:** [https://github.com/SevWren/digital\_art\_teacher](https://github.com/SevWren/digital_art_teacher) **Branch:** main — current commit: `db4525c` (at time of handoff; see below for additions made this session)

---

## What this project is

A portable agentic coding environment — usable across Claude Code, Codex, Gemini CLI, Grok, and similar tools — that turns a verified art-theory reference document into a stage-aware digital-art teaching assistant. The agent advises from a verified corpus; the user retains all creative authorship and aesthetic judgment.

Full project definition: `art_assistant_project_description.md` in the repo root. Prior session handoff (project-definition phase): `claude_art_assitant_project_definition_session_HANDOFF.md` in the repo root.

---

## What was built this session

All files are committed and pushed to `main`. References below are repo-relative paths.

### Agent instruction files

- `CLAUDE.md` — main instruction file. Session-start pending check, Tier 1 corpus table, subject-specific gap protocol (with pending-entry block: existing PENDING entry for a motif blocks new search; user has exactly two options: defer or resolve), evidence rule, authorship/description boundary, open corpus items.
- `AGENTS.md` — thin wrapper for Codex/OpenAI pointing to CLAUDE.md.
- `GEMINI.md` — thin wrapper for Gemini CLI pointing to CLAUDE.md.

### Skills

- `CLAUDE/skills/art-guidance/grounded-art-guidance/SKILL.md` — model-invoked. Full retrieval → pending-write → six-check → present-to-user → approve/reject/defer protocol. Conflict check is a soft warning; user can override but must receive the warning before promotion proceeds.
- `CLAUDE/skills/productivity/handoff/SKILL.md` — this handoff skill (moved into repo this session).

### Staging infrastructure

- `art-theory-pending.md` — pending area for web-retrieved subject-specific knowledge. Contains: motif-block rule (existing PENDING entry blocks new search), session-start 3-day expiry check, entry format, all six check definitions, defer/approve/reject update rules.

### Reference document (revised)

- `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md` — all changes from this session:
  - Subject rule row removed; "Subject-Agnostic" tagline removed
  - Knowledge tiers row added to header table
  - §1.5 added: two-tier knowledge system, six checks, 3-day expiry
  - §3.4 routing statement added
  - All "stage" (production step sense) replaced with "step" (9 replacements)
  - Claims Inventory removed from all operational references
  - Final paragraph fixed

### Domain model

- `CONTEXT.md` — 22 canonical terms: corpus, Tier 1/2, pending entry, approve/promote/defer/reject, gap, motif vs subject, universal principles, pipeline step, authorship boundary, description boundary, vision input, self-report, session.
- `docs/adr/0001` — open scope for subject-specific motifs
- `docs/adr/0002` — Claims Inventory excluded from repo by design
- `docs/adr/0003` — CLAUDE.md as single source of truth / thin wrapper pattern
- `docs/adr/0004` — quarantine-and-promote for web-retrieved knowledge

### Agent setup (added this session)

- `docs/agents/issue-tracker.md` — GitHub Issues via `gh` CLI
- `docs/agents/domain.md` — single-context layout rules
- `docs/agents/triage-labels.md` — five canonical triage labels
- `CLAUDE.md` updated with `## Agent skills` block
- GitHub labels created on the repo: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`

### Draft knowledge base (from earlier session, not modified this session)

- `art-theory-draft/art-theory/` — modular knowledge base. See `INDEX.md` for population status. Universal principles files exist; most pipeline step files are not yet written.

---

## Key decisions (with ADR/commit references)

| Decision | Record |
| :---- | :---- |
| Open scope for subject-specific motifs | `docs/adr/0001` |
| Claims Inventory PDF excluded from repo | `docs/adr/0002` |
| CLAUDE.md as single source of truth | `docs/adr/0003` |
| Quarantine-and-promote model | `docs/adr/0004` |
| "step" replaces "stage" for pipeline steps | commit `883478a` |
| "approve" \= user action; "promote" \= agent action | commit `883478a` |
| Conflict check is soft warning, user can override | commit `883478a` |
| Existing PENDING entry for a motif blocks new search | commit `db4525c` |
| Edge case: two input channels simultaneously | ~~intentionally left to agent judgment; not a hard rule~~ — superseded by issue #24: vision takes precedence; discrepancy surfaced to user; ADR-0007 to be filed |

---

## Open items in the corpus (tracked in CLAUDE.md)

1. **Vision capability contradiction** — §1.3 and §7 of the reference doc still say "AI cannot see your image." This has been flagged in CLAUDE.md as a tracked open item, but the corpus text itself has not been updated to reflect the confirmed in-scope capability. Requires a v6 annotation or explicit override.
2. **Secondary platform pixel dimensions** — explicitly not hardcoded; user must verify at export time.

---

## What is NOT done — queued work for next session

### Highest priority (explicitly queued before this session, still not started)

**Critique-vs-assist guardrail** — The single most important queued item. Must be defined before vision-input inspection is built. Reasoning: without vision, the AI can only respond to what the user typed — an accidental circuit-breaker against unrequested opinions. Vision removes that circuit-breaker. The guardrail spec must define the line between *description* (reporting what's observed — permitted) and *critique* (independent aesthetic/quality judgment — reserved for the user). This governs both input channels.

Full reasoning: `claude_art_assitant_project_definition_session_HANDOFF.md` §5.

### Medium priority

- **Remaining pipeline step files** — `art-theory-draft/art-theory/INDEX.md` lists 11 pipeline step files (01 through 11\) and 2 additional fundamentals (`materials-and-texture.md`, `design-and-shape-language.md`). Only `00-overview.md` is written.
- **Hooks** — `art_assistant_project_description.md` mentions hooks to gate every response before it reaches the user (check claims against bibliography, block untraced numbers). Not yet implemented.
- **Corpus vision update** — update §1.3 and §7 of `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md` once the guardrail spec is settled.

---

## Suggested skills for next session

- **`grill-me` or `grilling`** — stress-test the critique-vs-assist guardrail draft against adversarial prompts once written ("what do you think of this?", "rate this piece", "is this good?")
- **`to-spec`** — turn the guardrail decision into a formal spec committed to the repo
- **`writing-for-agents`** — use when drafting the guardrail's instruction file content (CLAUDE.md additions, skill file)
- **`wayfinder`** — map the remaining build (guardrail, pipeline files, hooks) as decision tickets in GitHub Issues before diving into any one piece
- **`domain-modeling`** — CONTEXT.md has one unaddressed edge case: two input channels simultaneously (intentionally left to agent judgment; revisit if inconsistent behavior is observed)
