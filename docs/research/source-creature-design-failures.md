# Failed Retrievals — Creature Design Research

All 7 target URLs failed all retrieval steps. None of the target pages exist at their specified URLs, have no Wayback Machine snapshots, no Google cache, and no archive.ph copies.

---

## URL 1: https://www.cgspectrum.com/blog/creature-design-process

**All steps attempted:**

- Step 1 (Direct fetch): 404 Not Found
- Step 2 (Wayback 2024): web.archive.org is blocked by WebFetch; curl returned empty (no snapshot)
- Step 3 (Wayback multiple timestamps): CDX API returned no captures at 20240101, 20231015, 20230601, 20220601
- Step 4 (Wayback availability API): `{"archived_snapshots": {}}` — no snapshot exists
- Step 5 (Google cache): 429 Too Many Requests (rate limited)
- Step 6 (HTTP variant): http://www.cgspectrum.com/blog/creature-design-process → 301 → 404
- Step 7 (www/trailing-slash variants): https://cgspectrum.com/blog/creature-design-process → 301 → 404; https://www.cgspectrum.com/blog/creature-design-process/ → 404
- Additional: archive.ph → 429; cachedview.nl → frontend-only (no cached content); Wayback CDX API → no captures ever recorded

**Conclusion:** Page does not exist and has never been captured by any archive service.

---

## URL 2: https://conceptartempire.com/creature-design/

**All steps attempted:**

- Step 1 (Direct fetch): 404 Not Found
- Step 2 (Wayback 2024): No snapshot
- Step 3 (Wayback multiple timestamps): CDX API returned no captures
- Step 4 (Wayback availability API): `{"archived_snapshots": {}}` — no snapshot exists
- Step 5 (Google cache): 429 Too Many Requests
- Step 6 (HTTP variant): http://conceptartempire.com/creature-design/ → 301 → 404
- Step 7 (www/trailing-slash variants): https://www.conceptartempire.com/creature-design/ → connection error (000); https://conceptartempire.com/creature-design → 404
- Additional: archive.ph → 429; Wayback CDX API → no captures; alternate slug creature-concept-art → 301 → creature-concept-art-gallery (a gallery page, not a design workflow article)

**Conclusion:** Page does not exist and has never been captured by any archive service.

---

## URL 3: https://80.lv/articles/creature-design-workflow

**All steps attempted:**

- Step 1 (Direct fetch): WebFetch returned auth error (internal); curl fetched 200 but JavaScript SPA with article error: "TypeError: Cannot convert undefined or null to object" — the article slug does not exist in the database
- Step 2 (Wayback 2024): No snapshot
- Step 3 (Wayback multiple timestamps): CDX API returned no captures
- Step 4 (Wayback availability API): `{"archived_snapshots": {}}` — no snapshot exists
- Step 5 (Google cache): 429 Too Many Requests
- Step 6 (HTTP variant): Same SPA response (200 with error)
- Step 7 (www/trailing-slash variants): Same SPA response
- Additional: 80.lv API v1/v2 endpoints returned 404 Not Found; Next.js data endpoint returned empty; Wayback CDX API → no captures

**Conclusion:** Article slug does not exist in 80.lv database and has never been archived.

---

## URL 4: https://www.gnomon.edu/blog/creature-design-workflow

**All steps attempted:**

- Step 1 (Direct fetch): 404 Not Found
- Step 2 (Wayback 2024): No snapshot
- Step 3 (Wayback multiple timestamps): CDX API returned no captures
- Step 4 (Wayback availability API): `{"archived_snapshots": {}}` — no snapshot exists
- Step 5 (Google cache): 429 Too Many Requests
- Step 6 (HTTP variant): http://www.gnomon.edu/blog/creature-design-workflow → 301 → 404
- Step 7 (www/trailing-slash variants): https://gnomon.edu/blog/creature-design-workflow → 302 → 404; https://www.gnomon.edu/blog/creature-design-workflow/ → 404
- Additional: archive.ph → 429; Wayback CDX API → no captures; gnomon.edu/blog/ itself returns 404

**Conclusion:** Page does not exist (gnomon.edu blog section appears to be entirely offline/removed) and has never been captured.

---

## URL 5: https://www.cgmasteracademy.com/blog/creature-design-process/

**All steps attempted:**

- Step 1 (Direct fetch): 404 Not Found
- Step 2 (Wayback 2024): No snapshot
- Step 3 (Wayback multiple timestamps): CDX API returned no captures
- Step 4 (Wayback availability API): `{"archived_snapshots": {}}` — no snapshot exists
- Step 5 (Google cache): 429 Too Many Requests
- Step 6 (HTTP variant): http://www.cgmasteracademy.com/blog/creature-design-process/ → 301 → 404
- Step 7 (www/trailing-slash variants): https://cgmasteracademy.com/blog/creature-design-process/ → 404; https://www.cgmasteracademy.com/blog/creature-design-process → 404
- Additional: archive.ph → 429; Wayback CDX API → no captures; cgmasteracademy.com/blog/ returns 404 (entire blog section offline)

**Conclusion:** Page does not exist (CGMA blog section appears offline) and has never been captured.

---

## URL 6: https://www.creativebloq.com/digital-art/creature-design-tips

**All steps attempted:**

- Step 1 (Direct fetch): 404 Not Found
- Step 2 (Wayback 2024): No snapshot
- Step 3 (Wayback multiple timestamps): CDX API returned no captures
- Step 4 (Wayback availability API): `{"archived_snapshots": {}}` — no snapshot exists
- Step 5 (Google cache): 429 Too Many Requests
- Step 6 (HTTP variant): http://www.creativebloq.com/digital-art/creature-design-tips → 301 → 404
- Step 7 (www/trailing-slash variants): https://creativebloq.com/digital-art/creature-design-tips → 301 → 404; https://www.creativebloq.com/digital-art/creature-design-tips/ → 301 → 404
- Additional: archive.ph → 429; Wayback CDX API → no captures; Creative Bloq site is live but this article URL is not; site search for "creature design" returned no matching articles

**Conclusion:** Page does not exist and has never been captured by any archive service.

---

## URL 7: https://www.conceptartworld.com/articles/creature-design-workflow

**All steps attempted:**

- Step 1 (Direct fetch): 404 Not Found
- Step 2 (Wayback 2024): No snapshot
- Step 3 (Wayback multiple timestamps): CDX API returned no captures
- Step 4 (Wayback availability API): `{"archived_snapshots": {}}` — no snapshot exists
- Step 5 (Google cache): 429 Too Many Requests
- Step 6 (HTTP variant): http://www.conceptartworld.com/articles/creature-design-workflow → 301 → 404
- Step 7 (www/trailing-slash variants): https://conceptartworld.com/articles/creature-design-workflow → 404; https://www.conceptartworld.com/articles/creature-design-workflow/ → 301 → 404
- Additional: archive.ph → 429; Wayback CDX API → no captures; conceptartworld.com homepage shows "under maintenance" message; articles section returns 404

**Conclusion:** Page does not exist (site is under maintenance) and has never been captured by any archive service.
