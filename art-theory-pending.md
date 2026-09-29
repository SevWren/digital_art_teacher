# art-theory-pending.md — Staged Knowledge Entries

This file is the quarantine area for subject-specific knowledge retrieved from web sources during sessions. No entry here is part of the verified Tier 1 corpus until it is explicitly promoted with user approval.

---

## Rules governing this file

**Session start check (mandatory, every session):**
Read this file at the start of every session. Find every entry where `created` is more than 3 days before today's date. Present each overdue entry to the user and collect a decision **before any other work begins**:

1. **Defer** — update the `created` field to today's date. The 3-day clock resets.
2. **Promote** — follow the `grounded-art-guidance` skill to run checks and move the entry into the corpus.

This check cannot be skipped or deferred. It runs before the user's first question is answered.

**When a new entry is written:**
- Set `created` to today's date in `YYYY-MM-DD` format.
- Set `status` to `PENDING`.
- Fill every field before saving.
- Save the file immediately after writing the entry.

**When an entry is promoted:**
- Set `status` to `PROMOTED`.
- Fill `promoted_to` with the corpus file path the content was written to.
- Save.

**When an entry is rejected:**
- Set `status` to `REJECTED`.
- Add a `rejection_reason` line under the User decision section.
- Save.

**When an entry is deferred:**
- Update `created` to the date the deferral was given (today).
- Leave all other fields unchanged.
- Save.

---

## Entry format

Every new entry must follow this structure exactly. Do not omit fields.

```
## Entry [sequential number] — [Subject]

| Field | Value |
| :--- | :--- |
| created | YYYY-MM-DD |
| status | PENDING |
| prompted_by | [user's question, verbatim or close paraphrase] |
| promoted_to | — |

### Sources
1. [URL] — [publisher or institution]
2. [URL] — [publisher or institution]
3. [URL] — [publisher or institution]

### Retrieved content
[Concise summary of the subject-specific knowledge retrieved — construction landmarks,
anatomical masses, proportional relationships, surface behavior, or other motif-specific
guidance found during the web search]

### Check results
| Check | Result | Note |
| :--- | :--- | :--- |
| Source count | PASS / FAIL | [n sources found] |
| Source quality | PASS / FAIL / FLAG | [note any sources that fail the quality threshold] |
| Independence | PASS / FLAG | [note any shared origin if present] |
| Conflict | PASS / FLAG | [name the contradicting claim and its Tier 1 location if flagged] |
| Language | PASS / FLAG | [name any overstated claims if flagged] |
| Scope | PASS / FLAG | [name the adjacent domain if flagged] |

### User decision
[pending / approved YYYY-MM-DD / rejected YYYY-MM-DD / deferred until YYYY-MM-DD]
```

---

## Check definitions (reference)

| Check | Pass condition | Fail / Flag condition |
| :--- | :--- | :--- |
| Source count | 3 or more independent published sources | Fewer than 3 |
| Source quality | All sources are academic, professional, or institutional | Any source is a personal blog, forum, social media, or unverified wiki |
| Independence | Each source arrived at its content through separate research | Two or more sources share the same single document as their primary origin |
| Conflict | Retrieved content does not contradict any Tier 1 claim | Contradiction found — must be named and resolved before promotion |
| Language | Consensus-practice claims use non-absolute language ("commonly," "typically," "often") | Any consensus-practice claim uses "always," "must," or "universally" |
| Scope | Content is about art theory, construction, or digital art practice | Content extends into an adjacent domain not within the project's purpose |

---

*No entries yet. This file is initialized empty at project setup.*
