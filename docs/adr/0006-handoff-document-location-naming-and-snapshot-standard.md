# ADR-0006 — Handoff Document Location, Naming, and Historical Snapshot Standard

**Date:** 2026-10-01
**Status:** Accepted

---

## Context

By session 4, handoff documents existed in three inconsistent states:

1. `claude_art_assitant_project_definition_session_HANDOFF.md` — root, typo in filename, mixed casing, no date, predates all build work
2. `digital_art_teacher_handoff_2026-09-30.md` — root, has date, redundant project-name prefix
3. `docs/historical/digital_art_teacher_handoff_2026-10-01.md` — correct directory, but same redundant-prefix naming

The generic `handoff` skill from the Matt Pocock skills set instructs agents to save handoff docs to the OS temp directory — incorrect for this repo-based project, where handoffs are version-controlled artifacts.

No policy existed for:
- Where handoffs belong
- What they must be named
- How agents must treat prior handoffs they encounter
- How the writing agent ensures prior docs are correctly labelled before adding a new one

Without a policy, each agent makes an independent choice, root clutter accumulates, and a new agent reading an old root-level handoff may act on stale instructions.

---

## Decision

### 1. Location — `docs/historical/` only

All handoff documents live in `docs/historical/`. No handoff document ever lives in the repo root or anywhere else.

**Root contains permanent project infrastructure only:** `CLAUDE.md`, `CONTEXT.md`, `README.md`, `AGENTS.md`, `GEMINI.md`, `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md`, `art-theory-pending.md`, and `art_assistant_project_description.md` (the permanent project description). Session handoffs are ephemeral snapshots and do not belong there.

Any handoff document found in the root is a policy violation and must be migrated immediately.

### 2. Naming — `handoff-YYYY-MM-DD.md`

The canonical filename format is:

```
handoff-YYYY-MM-DD.md
```

- Date-first: files sort chronologically without additional tooling
- No project-name prefix: the directory provides context
- Lowercase kebab-case throughout
- If two handoffs occur on the same date (rare), append a session suffix: `handoff-YYYY-MM-DD-session-2.md`

**Special case — non-session records** (project-definition docs, design records that predate the build phase): use `project-definition-YYYY-MM-DD.md` in the same directory.

### 3. Required Historical Snapshot Banner

Every document in `docs/historical/` must open with this exact banner as the first content (before the title heading):

```markdown
> **HISTORICAL SNAPSHOT — [YYYY-MM-DD]. Point-in-time record. Do not treat as current project state.**
>
> Before acting on any item in this document:
> 1. Run `git log --oneline -5` to see commits made after this date.
> 2. Check open GitHub Issues at https://github.com/SevWren/digital_art_teacher/issues for current work status.
> 3. Read the most recent handoff in `docs/historical/` for current context.
>
> **Known conflicts or superseded items at time of writing:** [list, or "None known"]
```

The banner must state the date the document was written, not the current date. Its purpose is to prevent a future agent from acting on stale instructions as if they were current.

### 4. Writing Agent Responsibilities

When an agent writes a new handoff document it must:

1. **Verify all prior docs** in `docs/historical/` already have the banner. If any are missing it, add the banner before committing the new handoff.
2. **Write to `docs/historical/handoff-YYYY-MM-DD.md`**, not to root, not to OS temp.
3. **Include the banner** as the first content of the new document, with "None known" for conflicts if the session was clean.
4. **Reference the prior handoff** by path (not by content) in the "Prior handoff" line.

### 5. Handoff Skill Override

The project-level override of the generic `handoff` skill is defined in `CLAUDE/skills/productivity/handoff/SKILL.md`. The project's `CLAUDE.md` specifies the location and naming rules. The generic skill's "save to OS temp" instruction is superseded for this project.

---

## Consequences

- The two root-level handoff documents are migrated to `docs/historical/` and renamed per the canonical scheme.
- `CLAUDE.md` gains a `## Handoff document convention` section encoding rules 1–4 above.
- The project's `handoff` skill is updated to override the generic "save to OS temp" instruction with the repo-specific rules.
- Future agents writing handoffs do not need to be told the convention — it is encoded in the instruction files they load at session start.

---

## Alternatives Considered

**Keep the most recent handoff at root as a stable entry point.** Rejected: root clutter compounds, and the convention of "always check docs/historical/ for the latest" is easy to encode in CLAUDE.md. A root-level stable pointer (e.g., `LATEST_HANDOFF.md`) would require maintenance and duplicate the path problem.

**Use git tag or commit annotation instead of a file.** Rejected: requires git knowledge to retrieve, inaccessible to agents that only read files, and breaks the plain-text search pattern.

**Let each agent choose freely.** Rejected: already tried; produces the three-inconsistent-state situation this ADR resolves.
