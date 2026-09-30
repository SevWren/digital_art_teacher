# Domain Docs

How the engineering skills should consume this repo's domain documentation when exploring the codebase.

## Before exploring, read these

- **`CONTEXT.md`** at the repo root: 22 canonical terms covering corpus, Tier 1/2, pending workflow, motif vs subject, pipeline step, authorship boundary, and more.
- **`docs/adr/`** at the repo root: four architecture decisions recorded. Read ADRs that touch the area you're about to work in.

If any of these files don't exist, **proceed silently**. Don't flag their absence; don't suggest creating them upfront.

## File structure

Single-context repo:

```
/
├── CONTEXT.md
├── docs/adr/
│   ├── 0001-open-scope-for-subject-specific-knowledge.md
│   ├── 0002-claims-inventory-excluded-from-repo.md
│   ├── 0003-claude-md-as-single-source-of-truth.md
│   └── 0004-quarantine-and-promote-for-web-retrieved-knowledge.md
└── ...
```

## Use the glossary's vocabulary

When your output names a domain concept (in an issue title, a refactor proposal, a hypothesis, a test name), use the term as defined in `CONTEXT.md`. Don't drift to synonyms the glossary explicitly avoids.

Key terms to watch: use **pending entry** not "staged entry"; **pipeline step** not "pipeline stage"; **approve** for the user's action and **promote** for the agent's act; **motif** for a recognizable subject category, **subject** for what a specific piece depicts.

If the concept you need isn't in the glossary yet, that's a signal: either you're inventing language the project doesn't use (reconsider) or there's a real gap (note it for `/domain-modeling`).

## Flag ADR conflicts

If your output contradicts an existing ADR, surface it explicitly rather than silently overriding:

> _Contradicts ADR-0003 (CLAUDE.md as single source of truth), but worth reopening because…_
