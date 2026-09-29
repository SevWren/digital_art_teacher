---
name: grounded-art-guidance
description: Subject-specific gap: user asks about anatomy, construction landmarks, markings, or surface systems for a motif type not found in Tier 1. Load for the full retrieval, staging, six-check review, and corpus-promotion protocol.
---

Two-tier retrieval protocol for subject-specific knowledge absent from Tier 1. Complete every step in sequence. Do not skip to promotion before checks are run and results presented to the user.

---

## 1. Confirm the gap

Name each Tier 1 file checked. State the specific subject the user is asking about. Confirm the knowledge is absent.

**Done when:** the response contains: "Checked [file(s)]. [Subject] [anatomy / construction landmarks / surface systems] is not present in Tier 1."

---

## 2. Request search permission

Say to the user:

> "I don't have [subject-specific knowledge] in the corpus. I can search the web for it — want me to?"

Wait for an explicit yes or no. Do not proceed to step 3 without a yes.

- **No:** State the gap clearly. Surface any adjacent universal-principle guidance from the corpus that partially applies — construction from primary forms (`fundamentals/form-and-construction.md`), gesture (`fundamentals/anatomy-and-gesture.md`), value structure (`fundamentals/light-and-value.md`). End the skill.
- **Yes:** Proceed to step 3.

**Done when:** user has given an explicit yes or no.

---

## 3. Search and retrieve

Search the web for the subject-specific knowledge. Prioritize sources in this order:
1. Academic or educational institution publications
2. Authoritative professional or industry documentation (established publishers, accredited curricula)
3. Established art-instruction resources with clear authorship and institutional backing

Collect source URLs. Aim for three or more. Record the publisher or institution for each source.

**Done when:** at least one result is retrieved and source URLs are recorded. (Source count is checked in step 5 — a low count does not stop this step.)

---

## 4. Write staging entry

Append a new entry to `art-theory-pending.md`. Use this exact structure. Fill every field. Leave check results and user decision as shown until step 5 fills them.

```
## Entry [next sequential number] — [Subject]

| Field | Value |
| :--- | :--- |
| created | [today's date YYYY-MM-DD] |
| status | PENDING |
| prompted_by | [user's question, verbatim or close paraphrase] |
| promoted_to | — |

### Sources
1. [URL] — [publisher or institution]
2. [URL] — [publisher or institution]
3. [URL] — [publisher or institution]

### Retrieved content
[Concise summary of the subject-specific knowledge found — construction landmarks, anatomical masses, proportional relationships, surface behavior, or other motif-specific guidance retrieved]

### Check results
| Check | Result | Note |
| :--- | :--- | :--- |
| Source count | | |
| Source quality | | |
| Independence | | |
| Conflict | | |
| Language | | |
| Scope | | |

### User decision
pending
```

Save `art-theory-pending.md` immediately after writing.

**Done when:** entry exists in the file with all fields populated and the file is saved.

---

## 5. Run the six checks

Evaluate each check against the staged entry. Write PASS, FAIL, or FLAG and a note into the check results table. Then save the file.

| Check | Criterion | Pass | Fail / Flag |
| :--- | :--- | :--- | :--- |
| **Source count** | Number of independent published sources retrieved | 3 or more | Fewer than 3 — record exact count |
| **Source quality** | Each source is academic, professional, or institutional | All sources qualify | Any source is a personal blog, forum post, social media, or unverified wiki — name it |
| **Independence** | Sources arrived at their content through separate research paths; no two share the same single document as their primary origin | No shared origin found | Two or more sources trace to one origin — name the shared source |
| **Conflict** | Retrieved content does not contradict any claim in Tier 1 | No contradiction | Name the specific contradicting claim and its Tier 1 location — this must be resolved before promotion |
| **Language** | Consensus-practice claims use non-absolute language | "Commonly," "typically," "in many professional workflows," "often," etc. | "Always," "must," "universally," or "never" applied to what is practiced convention, not physical law — name the claim |
| **Scope** | Content is about art theory, construction, visual practice, or digital art workflow | Clearly within the domain | Extends into an adjacent domain (typography, cartography, 3D software-specific node settings, medical anatomy beyond artistic application, etc.) — name the domain |

**Done when:** all six checks have a PASS, FAIL, or FLAG result recorded in the staging entry, and the file is saved.

---

## 6. Present and collect decision

Show the user in sequence:

1. The retrieved content (from the staging entry's "Retrieved content" field)
2. The check results table
3. Plain-language explanation of any FAIL or FLAG: what it means and why it matters
4. This prompt: "Do you want to **approve** this for the knowledge base, **reject** it, or **defer** the decision?"

**Done when:** user has given one of the three responses: approve, reject, or defer.

---

## 7. Act on the decision

### Approve

1. Write the retrieved content to the appropriate file in `art-theory-draft/art-theory/`:
   - If a fitting file exists (e.g., `fundamentals/anatomy-and-gesture.md` for figure/creature anatomy): add a clearly headed section for the new subject.
   - If no fitting file exists: create a new file under `fundamentals/` or the most appropriate subdirectory. Update `art-theory-draft/art-theory/INDEX.md` to list the new file.
2. Add each source URL to `art-theory-draft/art-theory/sources.md` under a new heading for the subject.
3. Add each source URL to the Bibliography in `ART THEORY & DIGITAL PRACTICE REFERENCE WIP.md` (Section 10), numbered sequentially.
4. Update the staging entry in `art-theory-pending.md`: set `status` to PROMOTED and `promoted_to` to the corpus file path.
5. Save all changed files.

**Done when:** corpus file updated, sources updated in both locations, staging entry marked PROMOTED, all files saved.

### Reject

1. Update the staging entry: set `status` to REJECTED.
2. Add a `rejection_reason` line under the User decision field with the user's stated reason.
3. Save `art-theory-pending.md`.

**Done when:** staging entry is marked REJECTED with a reason recorded and the file is saved.

### Defer

Leave the staging entry unchanged. The 3-day check in `CLAUDE.md` surfaces it at the next session start.

**Done when:** no changes needed — confirm to the user that the entry remains in staging and will surface again in 3 days.
