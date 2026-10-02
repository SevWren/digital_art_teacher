# Agent 2 Research Summary — Character Design Workflows and Pipelines
# Date: 2026-10-02

## Overview

Attempted retrieval of 7 target URLs about character design workflows and pipelines. 3 files were successfully saved with substantive content. 4 URLs could not be retrieved. web.archive.org is blocked in this environment, which eliminated Steps 2–4 of the retrieval protocol for all URLs.

---

## Successes (3 of 7)

### source-character-design-1.md
- **Original target:** https://www.cgspectrum.com/blog/character-design-process
- **Retrieved from:** https://www.cgspectrum.com/blog/what-is-character-design
- **Method:** Step 8 (alternate URL on same domain) — discovered via HTTP status probing of alternate paths
- **Content:** "What is Character Design for Film & Games? A Complete Guide" by Shoshanah Wall (CG Spectrum). Covers: principles of character design, what makes good character design (style/tone, costume, posture, story, silhouette), 3 examples (Grogu, Pikachu, GlaDOS), 7-step creation process (research, collect references, know your audience, define non-visual characteristics, conceptualization, color palette, begin drawing), and how character design feeds into 3D modeling and animation pipelines.
- **Approximate content length:** ~13,400 characters

### source-character-design-2.md
- **Original target:** https://conceptartempire.com/character-design-process/
- **Retrieved from:** https://conceptartempire.com/character-design/
- **Method:** Step 8 (alternate URL on same domain) — discovered via site search
- **Content:** "What is Character Design? (And What Does A Character Designer Do?)" (Concept Art Empire). Covers: what a character designer does, the typical process (briefing → thumbnailing → detailed painting → model sheet), style adaptation, pre-production role, pipeline handoff to 3D modeling/rigging or storyboard/visual development.
- **Approximate content length:** ~6,160 characters

### source-character-design-3.md
- **Original target:** https://www.cgmasteracademy.com/blog/character-design-workflow/
- **Retrieved from:** https://www.cgmasteracademy.com/blog/4-projects-to-build-character-design-skills-from-carhops-to-bebops.html
- **Method:** Step 8 (alternate URL on same domain) — discovered via CGMA blog.html listing
- **Content:** "4 Projects to Build Character Design Skills: From Carhops to Bebops" (CG Master Academy). Student breakdown by Lead Environment Artist Matthew Quickel documenting 4 character design assignments from CGMA's "Art Direction for Character Designers" course taught by Nate Wragg. Covers: shape/line/color exercises, style adaptation (UPA-influenced, Ronald Searle-influenced), cutesy-fication of existing characters, iteration process.
- **Approximate content length:** ~9,140 characters
- **Note:** CGMA posted a legal dissolution notice; the academy ceased operations as of November 2024.

---

## Failures (4 of 7)

| # | Original URL | Reason |
|---|---|---|
| 2 | https://characterdesignreferences.com/art-of-character-design/workflow | Page does not exist. The /art-of-character-design section is absent from the live site. Site sections are: art-of-animation, artist-of-the-week, interviews, blog-interviews, news, winners. No workflow content found anywhere on domain. |
| 3 | https://www.proko.com/how-to-design-a-character/ | Site is a JavaScript SPA. All URLs return HTTP 200 but deliver only an empty shell (~500 words). Article content is rendered client-side and inaccessible via static curl/HTTP fetch. |
| 4 | https://www.pluralsight.com/blog/film-games/ultimate-guide-character-concept-art | Page 404. Article has been removed from Pluralsight's blog. Alternate paths also 404. |
| 5 | https://www.animationcareerreview.com/articles/character-design-process | All article paths return 403. Cloudflare bot challenge blocks all non-browser access. Original article path not confirmed to exist. |

---

## Environment Constraints Encountered

1. **web.archive.org is blocked** in this environment — "Claude Code is unable to fetch from web.archive.org" — this eliminated the Wayback Machine fallback (Steps 2–4) for all 7 URLs.
2. **WebFetch tool API authentication errors** — the WebFetch tool repeatedly returned AWS Bedrock authorization errors for many URLs including Google cache, Proko, and others. Direct curl was used as the primary retrieval method.
3. **JavaScript SPAs** — Proko's website renders all content client-side; no static content was accessible.
4. **Cloudflare bot protection** — animationcareerreview.com blocks all non-browser article requests.

---

## Files Written

- `/home/vercel-sandbox/digital_art_teacher/docs/research/source-character-design-1.md` — CGSpectrum article
- `/home/vercel-sandbox/digital_art_teacher/docs/research/source-character-design-2.md` — Concept Art Empire article
- `/home/vercel-sandbox/digital_art_teacher/docs/research/source-character-design-3.md` — CGMA article
- `/home/vercel-sandbox/digital_art_teacher/docs/research/source-character-design-failures.md` — detailed failure log
- `/home/vercel-sandbox/digital_art_teacher/docs/research/agent2-summary.md` — this file
