# R2 Failures Log
# Retrieved: 2026-10-02

## Target 2: https://www.cgspectrum.com/blog/character-design-process
- Method 1 (WebFetch): API error (503/internal)
- Method 2 (Wayback CDX): No archived snapshots found (`{}`)
- Method 3 (curl): 404 — "PAGE NOT FOUND" on cgspectrum.com
- Method 4 (wget): Same 404
- Method 5 (Python urllib): Same 404
- Method 6 (Wayback direct): Wayback Machine temporarily offline
- Method 7 (URL variants): All variants return 404
- Method 8 (Domain sitemap scan): Found closest article `https://www.cgspectrum.com/blog/what-is-character-design` — saved as R2-source-2.md
- VERDICT: Original URL is permanently deleted. Closest available article saved instead.

## Target 3: https://www.cgspectrum.com/blog/how-to-become-a-character-designer
- Method 1 (WebFetch): API error
- Method 2 (Wayback CDX): No archived snapshots found
- Method 3 (curl): 404 — "PAGE NOT FOUND"
- Method 4–7: All return 404 or no results
- Method 8 (Domain sitemap scan): Found closest article `https://www.cgspectrum.com/blog/how-to-create-a-concept-art-portfolio` — saved as R2-source-3.md
- VERDICT: Original URL is permanently deleted. Closest available article saved instead.

## Target 6: https://conceptartempire.com/character-design-process/
- Method 1 (WebFetch): 404
- Method 2 (Wayback CDX): No archived snapshots (`[]`)
- Method 3 (curl): 404 — "Looks like this page has gone missing!"
- Method 4–7: All return 404
- Method 8 (sitemap scan): Sitemap returned no results for this URL
- Method 9 (sitemap.xml): No character-design-process URL found in sitemap
- VERDICT: Page permanently deleted; no archived copy available. Not recoverable.

## Target 8: https://www.animationcareerreview.com/articles/character-design-process
- Method 1 (WebFetch): 404
- Method 2 (Wayback CDX): No archived snapshots (`[]`)
- Method 3 (curl): 404 — "Home | Animation Career Review 404"
- Method 4–7: All return 404 or no results
- Method 8 (sitemap scan): Sitemap URL is on backdrop.acr.com subdomain; closest article on character animator career profile found and saved as R2-source-8.md
- VERDICT: Original URL not found. Best alternative from domain sitemap saved instead.

## Target 10: https://gurneyjourney.blogspot.com/search/label/character
- Method 1 (WebFetch): API error
- Method 3 (curl): Google bot-detection CAPTCHA triggered (HTTP 200 but CAPTCHA page returned)
- Method 5 (Python urllib): Same CAPTCHA response
- Method 6 (Wayback CDX): No archived snapshots (`{}`)
- Method 7 (URL variant): Homepage at https://gurneyjourney.blogspot.com/ accessible — saved as R2-source-10.md
- VERDICT: /search/label/character blocked by Google's anti-bot CAPTCHA. Homepage retrieved instead.

## Target 12: https://www.proko.com/how-to-design-a-character/
- Method 1 (WebFetch): API error
- Method 2 (Wayback CDX): No archived snapshots (`{}`)
- Method 3 (curl): Proko requires JavaScript — "Please enable JavaScript to continue using this application."
- Method 4–7: Same JavaScript requirement
- VERDICT: URL requires JavaScript/SPA rendering; content inaccessible to curl/wget. Not recoverable without a headless browser.

## Target 13: https://www.drawingfromscratch.com/character-design
- All methods (1–9): Site is in maintenance mode — "Site will be available soon. Thank you for your patience!"
- Wayback CDX: No archived snapshots
- VERDICT: Site entirely offline/in maintenance mode. Not recoverable.

## Target 14: https://www.posemyfigure.com/character-design-workflow
- Method 3 (curl): Returns empty response (connection refused or immediate empty body)
- Method 2 (Wayback CDX): No archived snapshots
- Method 5 (Python urllib): Empty response
- VERDICT: URL/domain appears to be inactive or non-existent. Not recoverable.

## Target 15 (partial): https://www.illustrationage.com/character-design
- Method 5 (Python urllib): Returns content, but the page is a very short 2013 blog post (not a comprehensive article on character design workflows).
- Saved as R2-source-15.md as it is the actual page at that URL.
