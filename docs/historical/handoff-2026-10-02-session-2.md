> **HISTORICAL SNAPSHOT — 2026-10-02. Point-in-time record. Do not treat as current project state.**
>
> Before acting on any item in this document:
> 1. Run `git log --oneline -5` to see commits made after this date.
> 2. Check open GitHub Issues at https://github.com/SevWren/digital_art_teacher/issues for current work status.
> 3. Read the most recent handoff in `docs/historical/` for current context.
>
> **Known conflicts or superseded items at time of writing:**
> - `docs/historical/handoff-2026-10-02.md` (Session 1 handoff from earlier today) is superseded by this document. It listed `docs/research/` untracked and `docs/specs/pipeline-definition.md` missing. Both are now resolved.
> - `docs/specs/pipeline-definition.md` is now **DRAFT, pending owner confirmation** on issue #36. Issues #7–#17 remain blocked until the owner comments on issue #36. No agent may start a pipeline step file before that comment exists.

# Digital Art Teacher — Session Handoff 2026-10-02 (Session 2)

**Date:** 2026-10-02
**Repo:** https://github.com/SevWren/digital_art_teacher
**Branch:** `main`
**HEAD commit at time of writing:** `1ec4de5`
**Prior handoff:** `docs/historical/handoff-2026-10-02.md` (superseded by this document)

---

## Part 1 — What Happened This Session (Session 2 of 2026-10-02)

### Inherited from Session 1 handoff (`handoff-2026-10-02.md`)

The Session 1 handoff (commit `073108e`) identified three critical items:
1. `docs/research/` (130 files) — untracked in git
2. `docs/specs/pipeline-definition.md` — did not exist
3. Issues #7–#17 — all 11 GitHub issue bodies were stale (no expanded scope, wrong research paths)

Session 1 had already fixed items 1 (committed research) and 3 (updated issue bodies). This session resolved item 2 and also corrected a problem with the research directory that was not called out in Session 1.

### This session

**Commit `df3ceb4` — Sterilised `docs/research/` (removed 113 junk files)**

The research directory committed in Session 1 (`073108e`) contained 130 files, the majority of which had no art research content: failure logs, 404 error notes, homepage navigation dumps, disambiguation pages, blog index listings, and duplicate Wikipedia articles.

Each file was individually audited against the criterion: *does this file contain actual art theory, technique guidance, pipeline steps, workflow descriptions, or professional practice information applicable to the digital art teaching project?*

113 files deleted. 17 files retained:

| Retained file | Content |
|---|---|
| `lineart/lineart-source-1.md` | Wikipedia Line Art — hatching, stippling, contour line definitions |
| `lineart/lineart-source-6.md` | Clip Studio inking (Marvel/Image artist) — spotted blacks, feathering, line weight for light |
| `lineart/lineart-summary.md` | Line art research synthesis |
| `manga/manga-source-16.md` | Pro artist guide to comic layouts, paneling, gutter, page flow |
| `manga/manga-source-17.md` | Digital vs hand-drawn manga — full pipeline: Storyboard > Base > Inking > Finishing Details |
| `manga/manga-source-18.md` | How to Make a Webtoon Page — A-to-Z pipeline including export specs |
| `manga/manga-source-19.md` | Inking Superhero Comics in CSP — professional inking techniques |
| `manga/manga-summary.md` | Manga research synthesis |
| `R1-summary.md` | Concept art pipeline synthesis |
| `R2-summary.md` | Character design pipeline synthesis |
| `R3-summary.md` | Environment art pipeline synthesis |
| `R4-summary.md` | Creature design pipeline synthesis |
| `R5-summary.md` | Academic digital painting synthesis |
| `R1-source-3.md` | Tyler James (Blizzard) interview — concept art process brief-to-delivery |
| `R4-source-9b.md` | 80.lv creature character production workflow — blockout → retopo → texturing → lighting |
| `source-academic-5.md` | Ctrl+Paint structured curriculum (full topic progression) |
| `source-character-design-2.md` | Concept Art Empire — character design thumbnailing and brief process |

**Commit `1ec4de5` — Created `docs/specs/pipeline-definition.md`**

The primary missing artifact for issue #36 was created. Contents:

- **Section 1 — Scope:** Explicit declaration of all art types (digital illustration, character art, environment art, creature design, comics, manga, webtoon, B&W illustration, line art, mixed workflows), subject types, workflow types, style registers, and mediums covered by the pipeline.
- **Section 2 — 11 Pipeline Steps:** Each step has: purpose statement, primary outputs, governing fundamentals, failure modes from skipping, and a medium variants table covering painted work / line art+comics / manga / B&W drawing / greyscale — with explicit skip conditions documented for Step 07 (pure line art = SKIP; greyscale = merges with Step 06).
- **Section 3 — Mapping to 13-stage Reference PDF:** Table mapping each of the 11 steps to the corresponding PDF stage(s), with explicit simplification notes.
- **Section 4 — Gap Analysis Summary:** Table of all expanded art types added (line art, manga, webtoon, B&W, greyscale) and the steps they affect.
- **Section 5 — Sources:** 8 verifiable sources with full URLs, held-at paths in `docs/research/`, and relevance notes. All URLs confirmed accessible at time of research.

**Status of `pipeline-definition.md`:** DRAFT — owner confirmation required on issue #36 before any pipeline step file is written.

---

## Part 2 — Current State of All Open Issues (16 open)

### Issue #36 — [P0] Comprehensive pipeline review and verification

**Status:** Open. Not closeable by an agent. Pending owner confirmation.

**What is done:**
- [x] Research completed (17 substantive files in `docs/research/`)
- [x] Pipeline scope expanded (line art, manga, webtoon, B&W added to all applicable steps)
- [x] `docs/specs/pipeline-definition.md` exists with all required sections (created `1ec4de5`)
- [x] Step names updated in `pipeline/00-overview.md` and `INDEX.md`

**What is not done (requires owner action):**
- [ ] Owner confirms pipeline structure by commenting on GitHub issue #36
- [ ] `INDEX.md` updated to reflect "pending authoring" (not "removed") — do after owner confirmation

**The exact confirmation statement the owner must leave on issue #36:**
> "I confirm the 11-step pipeline structure and scope in `docs/specs/pipeline-definition.md` as written on [date]. Issues #7–#17 are unblocked."

**What blocks issues #7–#17:** That comment. Nothing else.

---

### Issues #7–#17 — Pipeline step files

**Status:** All 11 open. **All blocked on owner confirmation on #36.** No pipeline step file may be started before that comment exists.

**All 11 issue bodies were updated this session.** Each now has:
- Correct file path
- Step name
- Full medium-variant coverage requirements (painted / line art / manga / B&W)
- Correct 4-source hierarchy with `docs/specs/pipeline-definition.md` as PRIMARY
- Correct research file references (`docs/research/lineart/lineart-summary.md`, `docs/research/manga/manga-summary.md`)

**Writing order when unblocked:** 01 → 02 → 03 → 04 → 05 → 06 → 07 → 08 → 09 → 10 → 11 (sequential — each file's `## Connections to Other Stages` section references earlier files that must already exist).

**Required sections in every pipeline step file:**
1. `## Plain-English Guide` — placed BEFORE first `##` technical heading; 4 elements: "What this is", "Why it matters for your painting", "The one thing to remember", "Common beginner pitfall"; zero art jargon in examples; everyday physical anchor first
2. Overview paragraph
3. `## What You Do at This Stage`
4. `## Stage Sign-off Condition`
5. `## Common Failure Modes`
6. `## Connections to Other Stages`

**Step 07 special requirement:** Must explicitly document the SKIP condition for pure line art and the merge condition for greyscale — both with sign-off statements. This is documented in `pipeline-definition.md` Section 2, Step 07.

---

### Issue #33 — [Epic C] Knowledge Base — Corpus Content

**Status:** Open. Blocked on #36 confirmation → #7–#17.

Children status:
- #7–#17: Open (blocked on #36 owner confirmation)
- #18–#21: Closed and verified
- #29: Closed and verified (Plain-English Guide sections moved to before technical content, correct 4-element structure, glossary.md processed)

---

### Issue #38 — [P1] Update INDEX.md

**Status:** Open. Blocked on #7–#17 completion.

**Current INDEX.md state:** Pipeline 01–11 shown as "Removed — pending #36". Must be updated to "Pending authoring" after owner confirms on #36, then updated again to "Written + Plain-English Guide" as each step file is completed.

---

### Issue #25 — [Phase 6] Integration QA

**Status:** Open. Blocked on #7–#17, #18–#21, #29, #22 all complete.

Existing QA report (`docs/qa/integration-qa-report-2026-10-01.md`) is stale — it tested a system with pipeline files that have since been rolled back. New report required after pipeline step files are committed.

---

### Issue #35 — [Epic E] QA & Handoff

**Status:** Open. Blocked on #25.

---

## Part 3 — Verified Closed Issues (do not re-open)

All issues listed as "verified closed" in `handoff-2026-10-02.md` (Session 1) remain valid. Additional verification this session:

| Issue | Verification |
|---|---|
| #2 | `CONTEXT.md` lines 91 (`Description (guardrail sense)`) and 107 (`Guardrail`) confirmed present |
| #4 | `docs/specs/critique-vs-assist-guardrail-stress-test.md` confirmed exists |
| #22 | `docs/adr/0009-vision-capability-corpus-update.md` confirmed exists |
| #29 | `glossary.md` has Plain-English Guide at top with 12 plain-language glosses; 8 fundamentals/digital-practices files have Plain-English Guide before first `##` heading with correct 4-element structure |
| #37 | `CLAUDE/skills/art-guidance/grounded-art-guidance/SKILL.md` Step 1 done-when says "is not in my knowledge base" |
| ADRs 0001–0009 | All exist |

---

## Part 4 — Repository File State at HEAD (`1ec4de5`)

### Key file changes since `handoff-2026-10-02.md`

| Path | Previous state | Current state |
|---|---|---|
| `docs/research/` | 130 files (untracked at Session 1 time; committed in Session 1) | 17 files — only substantive art research retained |
| `docs/specs/pipeline-definition.md` | DID NOT EXIST | EXISTS — DRAFT, 420 lines, awaiting owner confirmation |
| Issues #7–#17 (GitHub) | Stale bodies (old format, wrong research paths) | Updated with expanded scope, correct source hierarchy |

### `docs/research/` — final inventory (17 files)

```
docs/research/
├── R1-source-3.md                     Tyler James (Blizzard) concept art process interview
├── R1-summary.md                      Concept art pipeline synthesis
├── R2-summary.md                      Character design synthesis
├── R3-summary.md                      Environment art synthesis
├── R4-source-9b.md                    80.lv creature character production workflow
├── R4-summary.md                      Creature design synthesis
├── R5-summary.md                      Academic digital painting synthesis
├── lineart/
│   ├── lineart-source-1.md            Wikipedia Line Art (hatching, stippling, contour)
│   ├── lineart-source-6.md            CSP inking article — Scott Drummond (Marvel/Image)
│   └── lineart-summary.md             Line art research synthesis
├── manga/
│   ├── manga-source-16.md             Pro artist guide: comic layouts, paneling, flow
│   ├── manga-source-17.md             Digital vs hand-drawn manga full pipeline walkthrough
│   ├── manga-source-18.md             How to Make a Webtoon Page A-to-Z
│   ├── manga-source-19.md             Inking Superhero Comics in CSP — professional techniques
│   └── manga-summary.md               Manga research synthesis
├── source-academic-5.md               Ctrl+Paint full structured curriculum
└── source-character-design-2.md       Concept Art Empire — character design process
```

---

## Part 5 — Recommended Next Session Order

### Step 0 — Token setup (do every session)

```bash
pip install PyJWT cryptography -q

python3 -c "
with open('/home/vercel-sandbox/gh_app_token.py') as f:
    content = f.read()
content = content.replace('sevwrenai.2026-08-22.private-key.pem', 'sevwrenai.private-key.pem')
with open('/tmp/gh_token_fixed.py', 'w') as f:
    f.write(content)
"

TOKEN=$(python3 /tmp/gh_token_fixed.py)
cd /home/vercel-sandbox/digital_art_teacher
git remote set-url origin "https://x-access-token:${TOKEN}@github.com/SevWren/digital_art_teacher.git"
git config user.name "sevwrenai[bot]"
git config user.email "319983417+sevwrenai[bot]@users.noreply.github.com"
git log --oneline -5
```

Expected HEAD: `1ec4de5` or later.

Token expires after ~9 minutes. Refresh:
```bash
TOKEN=$(python3 /tmp/gh_token_fixed.py)
git remote set-url origin "https://x-access-token:${TOKEN}@github.com/SevWren/digital_art_teacher.git"
```

### Step 1 — Present `docs/specs/pipeline-definition.md` to owner; await confirmation on issue #36

The file exists at `docs/specs/pipeline-definition.md`. The owner must review it and leave a confirmation comment on GitHub issue #36.

**An agent's role here:** Read the file, present a summary to the owner, and ask for confirmation. Do not modify the pipeline-definition.md unless the owner requests specific changes. Do not start any pipeline step file.

**What to present:**
1. The 11 confirmed step names
2. The scope (all art types, mediums, style registers)
3. The two confirmed SKIP conditions in Step 07 (pure line art, greyscale)
4. Ask: "Does this pipeline structure and scope look correct to you? If so, please comment on issue #36 to unblock the pipeline step files."

### Step 2 — After owner confirmation on #36: update INDEX.md and close #36

1. Edit `art-theory-draft/art-theory/INDEX.md` — change pipeline file entries from "Removed — pending #36" to "Pending authoring — unblocked by #36"
2. Commit and push
3. Close issue #36 (the owner comment IS the confirmation; the agent closes after verifying all acceptance criteria are met)

### Step 3 — Write pipeline step files #7–#17 (sequential, one at a time)

Order: 01 → 02 → 03 → 04 → 05 → 06 → 07 → 08 → 09 → 10 → 11

For each step, before closing the issue, verify ALL of the following:
1. `docs/specs/pipeline-definition.md` commit is older than this file's commit (confirm via `git log`)
2. File exists at the exact path named in the issue
3. File content matches the step definition in `pipeline-definition.md` Section 2
4. File has all 6 required sections (Plain-English Guide first, then the 5 technical sections)
5. Plain-English Guide uses zero art jargon in examples; everyday physical anchor first
6. Every stage referenced in `## Connections to Other Stages` exists on disk at time of closing
7. `INDEX.md` updated to mark this file as populated

**No issue may be closed by an agent** — issues are left open for owner review and manual closure.

### Step 4 — Update INDEX.md (#38)

After all 11 pipeline step files are committed, update INDEX.md to mark all as "Written + Plain-English Guide". Commit and push. Leave #38 open for owner to close.

### Step 5 — Integration QA (#25)

After Steps 1–4 complete. Run across all 6 test domains. Produce `docs/qa/integration-qa-report-YYYY-MM-DD.md`. Leave #25 open for owner.

### Step 6 — Epic close and final handoff (#35)

After #25 passes. Write next handoff to `docs/historical/handoff-YYYY-MM-DD.md`. Leave epics open for owner.

---

## Part 6 — Non-Obvious Context for Next Agent

**No agent closes issues — ever.** The owner has explicitly stated that no issue may be closed by an agent. All issue close decisions belong to the owner. An agent's job is to complete the work and leave the issue open for owner verification and closure.

**`pipeline-definition.md` is the anchor for all pipeline step files.** Every pipeline step file must be consistent with the step definition in `pipeline-definition.md` Section 2. An agent writing step files should read Section 2 for the step they are writing before starting, not just the issue body.

**Step 07 has two skip conditions.** Both must be explicitly documented in the step file with sign-off condition statements: (1) pure line art = SKIP with sign-off "confirm with brief that pure line art is the intended output"; (2) greyscale = merge with Step 06 with sign-off "greyscale render from Step 06 is the complete tonal work — no separate colour pass required." These are not gaps in the pipeline; they are intentional, documented behaviours.

**The Plain-English mandate is absolute.** The target reader is someone using Photoshop or Photopea for the first time with no formal art training. Zero art jargon in the Plain-English Guide section examples. If a technical term appears anywhere in a pipeline step file, it must be followed immediately by a plain-English explanation and a concrete physical example on first use.

**The `Relationship to Pipeline` section in all 8 fundamentals files currently contains a placeholder.** After pipeline step files are committed, these placeholders should be updated to reference the confirmed step names and link to the step files. This is not a separate issue — it is a maintenance update that happens as each step file is committed.

**The research directory now contains only substantive art content.** If a next agent asks "where is the research?" the answer is: `docs/research/` has 17 files organised by topic. The summary files (`*-summary.md`) are the best starting points. For manga pipeline specifics, `manga/manga-source-17.md` is the most complete single-file walkthrough. For inking techniques, `lineart/lineart-source-6.md` and `manga/manga-source-19.md` are the primary sources.

---

## Part 7 — GitHub API Usage (gh CLI is not available)

```bash
# Get open issues
TOKEN=$(python3 /tmp/gh_token_fixed.py)
curl -s -H "Authorization: Bearer $TOKEN" -H "Accept: application/vnd.github+json" \
  "https://api.github.com/repos/SevWren/digital_art_teacher/issues?state=open&per_page=50"

# Get a specific issue body
curl -s -H "Authorization: Bearer $TOKEN" -H "Accept: application/vnd.github+json" \
  "https://api.github.com/repos/SevWren/digital_art_teacher/issues/36" | python3 -c "import json,sys; d=json.load(sys.stdin); print(d['body'])"

# Add a comment to an issue
curl -s -X POST \
  -H "Authorization: Bearer $TOKEN" -H "Accept: application/vnd.github+json" \
  "https://api.github.com/repos/SevWren/digital_art_teacher/issues/36/comments" \
  -d '{"body": "Comment text here"}'

# The gh CLI is NOT available in this sandbox. Use curl for all GitHub API calls.
```
