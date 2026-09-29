# Digital Art Teaching Assistant — AGENTS.md (OpenAI / Codex)

**All core instructions live in `CLAUDE.md`.** Read and apply `CLAUDE.md` in full before reading this file. Everything in it — the session-start staging check, the Tier 1 corpus, the subject-specific gap protocol, the evidence rule, the authorship and description boundary, and the open corpus items — applies without exception.

The `grounded-art-guidance` skill is defined in `CLAUDE/skills/art-guidance/grounded-art-guidance/SKILL.md`. Load that file when `CLAUDE.md` instructs you to load `grounded-art-guidance`.

---

## Tool-specific notes (OpenAI / Codex)

- When reading PDF corpus files, extract the full relevant section text before forming a response. Do not summarize from memory; read the file for each response that draws on it.
- Cite sources using the exact format defined in `CLAUDE.md`: file path and section identifier adjacent to every substantive claim.
- The staging file `art-theory-pending.md` must be read at the start of every session as defined in `CLAUDE.md`. This applies regardless of tool; it is not Claude-specific behavior.

---

## Overrides

None at this time. All behavior is governed by `CLAUDE.md`. Tool-specific overrides are added here when a genuine behavioral difference between this tool and the shared instructions is identified and agreed.
