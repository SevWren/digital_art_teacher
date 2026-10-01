---
name: handoff
description: Write an end-of-session handoff document for this repo. Saves to docs/historical/ with canonical naming. Enforces the historical snapshot banner on all prior docs.
argument-hint: "What will the next session focus on?"
disable-model-invocation: true
---

**Project-specific override.** This repo uses `docs/historical/` for all handoff documents, not the OS temp directory. The generic handoff skill's "save to OS temp" instruction does not apply here. See `docs/adr/0006-handoff-document-location-naming-and-snapshot-standard.md` for the full policy.

---

## Step 1 — Verify prior docs

Before writing the new handoff, scan every file in `docs/historical/`. Any file that does not already open with the Historical Snapshot Banner (see format below) must have the banner added now, before the new handoff is committed.

**Historical Snapshot Banner format:**

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

---

## Step 2 — Write the new handoff

**File path:** `docs/historical/handoff-YYYY-MM-DD.md` where the date is today's date.

If two handoffs occur on the same date, append a session suffix: `handoff-YYYY-MM-DD-session-2.md`.

**The document must open with the Historical Snapshot Banner** (same format above), dated today, with "None known" for conflicts if the session was clean, or a list of specific conflicts if they exist.

**Content to include** (do not duplicate content already in other artifacts — reference by path instead):

1. **Session date, repo, branch, and most recent commit hash**
2. **Session summary** — what was done, what issues were closed, what artifacts were created
3. **Issues closed this session** — table with issue number, title, and artifact path
4. **Current state of all open issues** — grouped by epic, with the immediate next priorities called out
5. **Recommended next session order** — numbered priority list
6. **Key files reference** — table of important paths and their purposes
7. **GitHub token setup instructions** — the pip+PyJWT method for this sandbox
8. **Notes for next agent** — any non-obvious context that does not live in code

**Do not include:**
- Content already captured in CLAUDE.md, CONTEXT.md, ADRs, or specs (reference the file instead)
- Invented future plans not grounded in open GitHub Issues
- Sensitive information (API keys, credentials)

---

## Step 3 — Commit

Add both the new handoff and any banner-patched prior docs to a single commit:

```
git add docs/historical/
git commit -m "docs(handoff): session YYYY-MM-DD handoff doc (closes #26)"
```

Push immediately — the sandbox is ephemeral.
