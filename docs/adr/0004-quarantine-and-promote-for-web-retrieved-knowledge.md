# Quarantine-and-promote for web-retrieved knowledge

Web-retrieved subject-specific knowledge is not used directly as corpus knowledge and is not discarded after the session. It is written immediately to a persistent pending file, subjected to a six-check review, presented to the user with check results, and only moved into the corpus upon explicit user approval. This is the quarantine-and-promote model.

## Considered options

**Session-only:** Retrieved content is used in the current session response with a caveat, then discarded. Clean — no persistent state — but the same retrieval must happen again next session. The corpus never grows from web retrieval.

**Direct corpus addition:** Retrieved content passes checks and is written to the corpus without a separate user approval step. Faster, but removes human judgment from the loop for what enters the verified knowledge base.

**Quarantine-and-promote (chosen):** Content is stored, checked, and requires explicit user approval before it enters the corpus. Slower per interaction, but the corpus remains human-curated and the three-source standard is applied consistently.

## Consequences

The pending file accumulates entries over time. The 3-day expiry rule is the mechanism that prevents it from becoming a permanently growing queue. If the expiry rule is not enforced, the pending file will silently accumulate stale entries that block session-start and create user friction.
