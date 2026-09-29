# CLAUDE.md as single source of truth; AGENTS.md and GEMINI.md as thin wrappers

All core agent instructions live in CLAUDE.md. AGENTS.md (for Codex/OpenAI) and GEMINI.md (for Gemini CLI) contain only a pointer to CLAUDE.md and genuine tool-specific overrides. They do not duplicate the core rules.

This was chosen over maintaining three full independent instruction files because duplicated content drifts: a rule change made in CLAUDE.md would need to be made in two other files, and any missed update would silently produce inconsistent behavior across tools.

## Why this is surprising without context

A developer picking up AGENTS.md or GEMINI.md expects to find full instructions there. Finding only "read CLAUDE.md" looks incomplete. It is not incomplete — it is the intended structure.

## Consequences

Any tool that cannot read CLAUDE.md (e.g., a tool that only loads its own named file and cannot follow a cross-file pointer) will be underspecified. If such a tool is added, its wrapper file must be expanded to include the full instruction set, accepting the maintenance burden of duplication for that tool alone.
