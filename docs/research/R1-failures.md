# R1 Failures Log

---

URL: https://www.cgspectrum.com/blog/concept-art-process
Methods tried:
- Method 1 (WebFetch direct): FAILED — WebFetch tool returned API error (bedrock:InvokeModelWithResponseStream not authorized)
- Method 2 (Wayback CDX API): No snapshot available — {"url": "...", "archived_snapshots": {}}
- Method 3 (curl): HTTP 404 — page does not exist
- Method 4 (wget): Not attempted after confirmed 404
- Method 5 (Python urllib): Not attempted after confirmed 404
- Method 6 (Wayback direct snapshot): No snapshot in archive
- Method 7 (URL variants): Tried http:// variant — same 404 result
- Method 8 (Domain homepage scan): Not needed — domain is accessible
- Method 9 (Sitemap scan): Sitemap retrieved from cgspectrum.com; no URL for "concept-art-process" found. Best alternative article retrieved: https://www.cgspectrum.com/blog/what-it-is-like-to-be-a-professional-concept-artist (saved as R1-source-3.md with note)

---

URL: https://conceptartworld.com/articles/concept-art-workflow/
Methods tried:
- Method 1 (WebFetch direct): FAILED — WebFetch tool returned API error (bedrock:InvokeModelWithResponseStream not authorized)
- Method 2 (Wayback CDX API): No snapshot available — {"archived_snapshots": {}}
- Method 3 (curl): Site is under maintenance — returns maintenance page with no article content
- Method 4 (wget): Not attempted after confirmed maintenance mode
- Method 5 (Python urllib): Not attempted after confirmed maintenance mode
- Method 6 (Wayback direct snapshot): Tried https://web.archive.org/web/20231001/URL and https://web.archive.org/web/20220601/URL — Wayback Machine returned "The Wayback Machine has not archived that URL."
- Method 7 (URL variants): Not applicable — confirmed no archive exists
- Method 8 (Domain homepage scan): Also in maintenance mode
- Method 9 (Sitemap scan): Site under maintenance — sitemap inaccessible

---

URL: https://conceptartworld.com/
Methods tried:
- Method 1 (WebFetch direct): FAILED — WebFetch tool returned API error
- Method 2 (Wayback CDX API): Snapshot found at http://web.archive.org/web/20260926213038/https://conceptartworld.com/
- Method 3 (curl on original URL): Returns maintenance page
- Method 3 on Wayback snapshot: Wayback Machine returned bot-detection block — "Your request is being blocked because our system has flagged it as suspected abusive bot traffic"
- Methods 4-9: Not attempted — Wayback Machine actively blocked all requests

---

URL: https://www.creativebloq.com/digital-art/concept-art-tips-6150013
Methods tried:
- Method 1 (WebFetch direct): FAILED — WebFetch tool returned API error
- Method 2 (Wayback CDX API): No snapshot available — {"archived_snapshots": {}}
- Method 3 (curl): HTTP 404 — page does not exist; site returns "Sorry! Page not found."
- Method 4 (wget): Not attempted after confirmed 404
- Method 5 (Python urllib): Not attempted after confirmed 404
- Method 6 (Wayback direct snapshot): CDX search returned empty array [] — no archived snapshots
- Method 7 (URL variants): Not applicable — no archive of any variant exists
- Method 8 (Domain homepage scan): creativebloq.com domain is accessible but the specific article has been removed
- Method 9 (Sitemap scan): Not attempted — article confirmed permanently removed from site and Wayback

---

URL: https://www.pencilkings.com/concept-art-process/
Methods tried:
- Method 1 (WebFetch direct): FAILED — WebFetch tool returned API error
- Method 2 (Wayback CDX API): No snapshot available — {"archived_snapshots": {}}
- Method 3 (curl): HTTP 404 — returns "This page doesn't seem to exist."
- Method 4 (wget): Not attempted after confirmed 404
- Method 5 (Python urllib): Not attempted after confirmed 404
- Method 6 (Wayback direct snapshot): CDX gateway timeout; no snapshots available
- Method 7 (URL variants): Not attempted — confirmed no archive
- Method 8 (Domain homepage scan): pencilkings.com homepage is accessible (saved as R1-source-11.md) but the specific concept-art-process article is missing
- Method 9 (Sitemap scan): Not attempted

---

URL: https://gurneyjourney.blogspot.com/2010/06/stages-of-painting.html
Methods tried:
- Method 1 (WebFetch direct): FAILED — WebFetch tool returned API error
- Method 2 (Wayback CDX API): No snapshot available — {"archived_snapshots": {}}
- Method 3 (curl): Blocked by Google CAPTCHA/reCAPTCHA — returns CAPTCHA challenge page, not article content
- Method 4 (wget): Not attempted — same IP is CAPTCHA-blocked
- Method 5 (Python urllib): HTTP Error 404 returned (CAPTCHA redirected to non-existent page)
- Method 6 (Wayback direct snapshot): CDX search returned empty array [] — no archived snapshots
- Method 7 (URL variants): Not applicable — no archive exists, CAPTCHA blocks all direct access
- Method 8 (Domain homepage scan): gurneyjourney.blogspot.com homepage also blocked by CAPTCHA (different block — Google automated traffic detection)
- Method 9 (Sitemap scan): Not attempted — domain access fully CAPTCHA-blocked

---

URL: https://gurneyjourney.blogspot.com/
Methods tried:
- Method 1 (WebFetch direct): FAILED — WebFetch tool returned API error
- Method 3 (curl): Blocked by Google CAPTCHA — "In order to continue, please enable javascript on your web browser." and reCAPTCHA challenge served (IP: 44.223.37.29 flagged as bot traffic)
- All other methods: Not attempted — Google's automated traffic detection blocks all server-side requests to this Blogger domain

---

URL: https://www.illustrationage.com/concept-art-workflow
Methods tried:
- Method 1 (WebFetch direct): FAILED — WebFetch tool returned API error
- Method 2 (Wayback CDX API): No snapshot available — {"archived_snapshots": {}}
- Method 3 (curl): Returns JavaScript hashcash bot-protection challenge page — no content accessible
- Method 4 (wget): Not attempted — same bot protection blocks wget
- Method 5 (Python urllib): Not attempted — bot protection requires JS execution
- Method 6 (Wayback direct snapshot): No snapshot in archive
- Method 7 (URL variants): Not attempted — bot protection on entire domain
- Method 8 (Domain homepage scan): illustrationage.com domain root also returns same hashcash/JS challenge (HTTP 403)
- Method 9 (Sitemap scan): Returns hashcash challenge — inaccessible

---

URL: https://thegnomonworkshop.com/blog/concept-art-workflow
Methods tried:
- Method 1 (WebFetch direct): FAILED — WebFetch tool returned API error
- Method 2 (Wayback CDX API): No snapshot available — {"archived_snapshots": {}}
- Method 3 (curl): HTTP 404 — returns "Page not found" with "0 results found in this keyword"
- Method 4 (wget): Not attempted after confirmed 404
- Method 5 (Python urllib): Not attempted after confirmed 404
- Method 6 (Wayback direct snapshot): No snapshot in archive
- Method 7 (URL variants): Not attempted — confirmed 404 and no Wayback archive
- Method 8 (Domain homepage scan): thegnomonworkshop.com blog section shows concept art workshop listings but not this specific article
- Method 9 (Sitemap scan): Not attempted
