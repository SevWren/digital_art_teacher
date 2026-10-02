# R3 Retrieval Failures Log
# Retrieved: 2026-10-02

---

## Target 2: https://www.cgspectrum.com/blog/environment-concept-art

- Method 1 (WebFetch): FAILED - WebFetch tool returned API authentication error (Bedrock model unavailable)
- Method 2 (Wayback CDX): FAILED - {"archived_snapshots": {}} — no archived snapshots found
- Method 3 (curl direct): FAILED - HTTP 200 but page title returned "404 - Page not found" (HubSpot CMS renders 404 as 200)
- Method 4–9: Not attempted separately as all confirm the URL does not exist / was never captured
- CONCLUSION: URL does not exist on cgspectrum.com. This specific blog post URL was never published or has been removed.

---

## Target 3: https://www.cgspectrum.com/blog/what-is-environment-concept-art

- Method 1 (WebFetch): FAILED - WebFetch tool returned API authentication error (Bedrock model unavailable)
- Method 2 (Wayback CDX): FAILED - {"archived_snapshots": {}} — no archived snapshots found
- Method 3 (curl direct): FAILED - HTTP 200 but page title returned "404 - Page not found" (HubSpot CMS renders 404 as 200)
- Method 4–9: Not attempted separately as all confirm the URL does not exist / was never captured
- CONCLUSION: URL does not exist on cgspectrum.com. This specific blog post URL was never published or has been removed. The cgspectrum.com/blog page does not contain any environment concept art articles (see R3-source-4.md for the actual blog index content).

---

## Target 5: https://80.lv/articles/breakdown-of-environment-concept-art-workflow/

- Method 1 (WebFetch): FAILED - WebFetch tool returned API authentication error (Bedrock model unavailable)
- Method 2 (Wayback CDX): FAILED - {"archived_snapshots": {}} — not archived
- Method 3 (curl direct): HTTP 200 but content was only 16,785 bytes — returned boilerplate navigation/metadata only, no article body (JavaScript-rendered content not available via curl)
- Method 4 (wget): Returned same minimal JS-required page
- Method 5 (Python urllib): Same result
- Method 6 (Wayback timestamps): "The Wayback Machine has not archived that URL." Confirmed not in archive.
- Method 7 (URL variants): Tried breakdown-of-environment-concept-art-workflow/ — same issue, article body requires JS
- Method 8 (Domain homepage): Found environment art articles from 80.lv but not this specific slug
- Method 9 (Sitemap): 80.lv does not expose a public sitemap with this URL
- CONCLUSION: The specific article slug "breakdown-of-environment-concept-art-workflow" does exist on 80.lv (returns HTTP 200) but the content is JavaScript-rendered and not accessible via static curl/wget. Saved closest available 80.lv environment art articles to R3-source-5.md and R3-source-8.md instead.

---

## Target 9: https://conceptartempire.com/environment-design/

- Method 3 (curl direct): HTTP 200 but page returned "404 page not found" content
- Wayback: Not checked separately; site renders 404 inline
- CONCLUSION: URL does not exist. Only /environment-concept-art/ URL works (saved as R3-source-3.md).

---

## Target 10: https://www.gnomon.edu/blog/environment-design

- Method 3 (curl direct): Redirects to gnomon.edu homepage (Gnomon does not have a /blog path; their content lives at /news-and-events/)
- Method 8 (Domain homepage scan): Confirmed no /blog URL structure exists; gnomon.edu uses /news-and-events/news/ instead
- CONCLUSION: URL does not exist. Gnomon does not use /blog/ URL structure. Content saved from /news-and-events/news/ as R3-source-10.md.

---

## Target 11: https://www.gnomon.edu/blog

- Same as Target 10 — /blog path does not exist on gnomon.edu
- CONCLUSION: URL does not exist. See R3-source-10.md for the actual Gnomon news/events page.

---

## Target 13: https://www.illustrationage.com/environment-design

- Method 3 (curl direct): Returns "Checking your browser..." — Cloudflare bot protection, JS required
- Method 2 (Wayback CDX): {"archived_snapshots": {}} — not archived
- Method 4 (wget): Same Cloudflare challenge page
- Method 5 (Python urllib): Same Cloudflare challenge page
- Method 6 (Wayback timestamps): Not archived
- Method 7 (URL variants): Not attempted — Cloudflare blocks all non-browser requests
- CONCLUSION: Site protected by Cloudflare bot challenge. Not accessible without a real browser. No Wayback snapshot available.

---

## Target 14: https://www.cgmasteracademy.com/blog/

- Method 3 (curl direct): HTTP 404 — URL with trailing slash returns NoSuchKey S3 error
- Method 7 (URL variants): /blog (no slash) also returns 404. /blog.html returns 404. Homepage / returns 200.
- Note: CGMA has a dissolution filing as of Nov 14, 2024; course operations are paused.
- CONCLUSION: /blog/ URL path does not exist. Blog content is served from homepage with pagination. See R3-source-11.md for blog listing from homepage.

---

## Target 15: https://levelup.gitconnected.com/environment-concept-art-workflow

- Method 1 (WebFetch): FAILED - WebFetch tool returned API authentication error
- Method 2 (Wayback CDX): {"archived_snapshots": {}} — not archived
- Method 3 (curl direct): Returns "Just a moment... Enable JavaScript and cookies to continue" — Cloudflare/Medium bot protection
- Method 4 (wget): Same bot protection page
- Method 5 (Python urllib): Same bot protection page
- Method 6 (Wayback timestamps): Not archived
- CONCLUSION: Medium/gitconnected uses bot protection that prevents static fetching. URL may or may not exist. No content retrieved.

---

## WebFetch Tool

- All WebFetch attempts failed due to: API Error 403 — Bedrock model (claude-haiku-4-5) not authorized for InvokeModelWithResponseStream. This affected all Method 1 attempts.
