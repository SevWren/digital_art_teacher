# Agent 4 — Creature Design Research Summary

**Task:** Retrieve complete text of 7 professional web pages about creature design and creature concept art pipelines/workflows.

**Date:** 2026-10-02

---

## Results Overview

| # | Original URL | Status | Reason |
|---|---|---|---|
| 1 | https://www.cgspectrum.com/blog/creature-design-process | FAILED | 404 — page never existed or was removed; no archive |
| 2 | https://conceptartempire.com/creature-design/ | FAILED | 404 — page never existed or was removed; no archive |
| 3 | https://80.lv/articles/creature-design-workflow | FAILED | SPA returns 200 but article not in database; no archive |
| 4 | https://www.gnomon.edu/blog/creature-design-workflow | FAILED | 404 — gnomon.edu blog section offline; no archive |
| 5 | https://www.cgmasteracademy.com/blog/creature-design-process/ | FAILED | 404 — CGMA blog section offline; no archive |
| 6 | https://www.creativebloq.com/digital-art/creature-design-tips | FAILED | 404 — article does not exist; no archive |
| 7 | https://www.conceptartworld.com/articles/creature-design-workflow | FAILED | 404 — site under maintenance; no archive |

**Total successes: 0 / 7**
**Total failures: 7 / 7**

---

## Retrieval Steps Attempted Per URL

For every URL, the following steps were attempted exhaustively:

1. **Direct fetch** — WebFetch tool + curl with browser User-Agent
2. **Wayback Machine 2024** — `https://web.archive.org/web/2024/{URL}` (blocked for WebFetch; curl attempted)
3. **Wayback Machine multiple timestamps** — 20240101, 20231015, 20230601, 20220601 via curl
4. **Wayback Machine availability API** — `https://archive.org/wayback/available?url={URL}` — all returned `{"archived_snapshots": {}}`
5. **Wayback CDX API** — `http://web.archive.org/cdx/search/cdx?url={URL}` — all returned empty (never captured)
6. **Google cache** — `https://webcache.googleusercontent.com/search?q=cache:{URL}` — returned 429 rate limited
7. **HTTP variant** — http:// instead of https://
8. **www variant** — with/without www prefix
9. **Trailing slash variant** — with and without trailing slash
10. **Additional methods:**
    - archive.ph / archive.today — returned 429 for all
    - cachedview.nl — frontend-only service, no direct cached content
    - Bing cache (cc.bingj.com) — connection refused (000)
    - Domain sitemaps — checked CGSpectrum, CGMA; neither contained creature design blog entries
    - RSS feeds — CGSpectrum RSS had no creature articles
    - Alternate URL slugs on the same domains — none resolved to creature design workflow articles
    - 80.lv API endpoints (v1, v2) — all returned 404 Not Found for article slug
    - Site searches — creativebloq.com search returned no creature design articles

---

## Key Findings

- **None of the 7 target URLs have ever been captured by the Wayback Machine** (CDX API confirmed zero captures for all 7). This strongly suggests these URLs were never publicly live.
- **CGSpectrum** blog is live and has other articles, but not this specific slug. The sitemap shows only 2 creature-related pages (an event page and a career pathway page, neither being this article).
- **ConceptArtEmpire** has a creature concept art gallery page (`/creature-concept-art-gallery/`) but not the targeted `/creature-design/` article.
- **80.lv** is a live site with active articles, but the `creature-design-workflow` slug does not exist in their database (confirmed via their API).
- **Gnomon.edu blog** and **CGMA blog** sections appear to be entirely offline (both return 404).
- **ConceptArtWorld** is under maintenance (entire site).
- **Creative Bloq** is live but the specific article URL does not exist.

---

## Files Produced

- `/home/vercel-sandbox/digital_art_teacher/docs/research/source-creature-design-failures.md` — detailed failure log for all 7 URLs
- `/home/vercel-sandbox/digital_art_teacher/docs/research/agent4-summary.md` — this file
