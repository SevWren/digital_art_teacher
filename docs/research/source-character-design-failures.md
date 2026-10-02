# Failed URLs — Character Design Research

All steps attempted per the retrieval protocol. web.archive.org is blocked in this environment ("Claude Code is unable to fetch from web.archive.org"), so Steps 2–4 failed universally for all URLs.

---

## URL 2: https://characterdesignreferences.com/art-of-character-design/workflow

- Step 1 (Direct fetch): 404 Not Found
- Step 2–4 (Wayback Machine): web.archive.org is blocked in this environment
- Step 5 (Google cache): API authentication error (503/403 from underlying model)
- Step 6 (HTTP variant): 404 Not Found
- Step 7 (www/no-www variants): 404 Not Found (site uses no www)
- Step 8 (alternate paths): All numbered variants (/art-of-character-design-2 through -10) return 404. The /art-of-character-design section does not exist on this domain. The site (a Squarespace site) has sections: art-of-animation, artist-of-the-week, interviews, blog-interviews, news, winners. No character-design-workflow content found.
- Result: FAILED — page does not exist on the live site

---

## URL 3: https://www.proko.com/how-to-design-a-character/

- Step 1 (Direct fetch): 403 Forbidden (API auth error from WebFetch)
- Step 2–4 (Wayback Machine): web.archive.org is blocked in this environment
- Step 5 (Google cache): API authentication error
- Step 6 (HTTP variant): 403 / API auth error
- Step 7 (www/no-www): 403 / API auth error
- Step 8 (alternate paths attempted): /blog/how-to-design-a-character, /lessons/how-to-design-a-character, /character-design, /courses/character-design, /blog/character-design-tips, /blog/character-design-fundamentals, /blog/how-to-create-a-character — all return HTTP 200 but the site is a JavaScript SPA (React/Vue); curl only retrieves the empty shell (~500 words nav/footer, no article body). No static HTML content is accessible without a JavaScript runtime.
- Result: FAILED — site requires JavaScript rendering; content not accessible via static HTTP fetch

---

## URL 4: https://www.pluralsight.com/blog/film-games/ultimate-guide-character-concept-art

- Step 1 (Direct fetch): 404 Not Found
- Step 2–4 (Wayback Machine): web.archive.org is blocked in this environment
- Step 5 (Google cache): API authentication error
- Step 6 (HTTP variant): 404 Not Found
- Step 7 (www/no-www): 404 Not Found (www is canonical)
- Step 8 (alternate paths): /blog/film-games/character-concept-art also 404. Blog listing at /blog/film-games returned 402KB of content but zero character-design article links found. The article has been removed from Pluralsight's blog.
- Result: FAILED — page does not exist on the live site

---

## URL 5: https://www.animationcareerreview.com/articles/character-design-process

- Step 1 (Direct fetch): 403 Forbidden (Cloudflare bot challenge)
- Step 2–4 (Wayback Machine): web.archive.org is blocked in this environment
- Step 5 (Google cache): API authentication error
- Step 6 (HTTP variant): 403 Forbidden
- Step 7 (www/no-www): 403 Forbidden
- Step 8 (alternate paths): All /articles/* paths return 403. The site uses Cloudflare with a JavaScript challenge that cannot be passed by a curl/HTTP client. Home page (/) returns 40KB of HTML but all article paths are blocked. Sitemap.xml exists but contains no character-design article URL. The path /articles/character-design-process does not appear in any discovered sitemap or link structure.
- Result: FAILED — site blocked by Cloudflare bot protection on all article paths; original article path unconfirmed to exist

---

## URL 6 (alternate): https://conceptartempire.com/character-design-process/

- Note: The specific path /character-design-process/ returned 404, but content was successfully retrieved from the alternate URL /character-design/ on the same domain. Saved as source-character-design-2.md.

---

## URL 7 (alternate): https://www.cgmasteracademy.com/blog/character-design-workflow/

- Note: The specific path /blog/character-design-workflow/ returned 404. The CGMA blog uses .html extensions. The path /blog/character-design-workflow.html also returns 404. However, content was successfully retrieved from the alternate URL /blog/4-projects-to-build-character-design-skills-from-carhops-to-bebops.html on the same domain. Saved as source-character-design-3.md. Note: CGMA posted a legal dissolution notice dated Nov 14, 2024; the academy has ceased operations.
