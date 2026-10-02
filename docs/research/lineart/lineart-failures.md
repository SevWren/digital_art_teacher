# Line Art Research — Retrieval Failures
# Date: 2026-10-02

## Summary of Failed URLs

| # | URL | Status | Reason |
|---|-----|--------|--------|
| 2 | https://en.wikipedia.org/wiki/Inking_(comics) | MISSING | Wikipedia article does not exist at this URL |
| 5 | https://www.clipstudio.net/how-to-draw/archives/category/line-art | 404 | Category page no longer exists (site rebranded to Art Rocket) |
| 8 | https://conceptartempire.com/line-art/ | 404 | Page removed or URL structure changed |
| 9 | https://conceptartempire.com/inking/ | 404 | Page removed or URL structure changed |
| 10 | https://www.cgspectrum.com/blog/line-art | 404 | Blog post not found |
| 11 | https://www.cgspectrum.com/blog/inking-tips | 404 | Blog post not found |
| 12 | https://drawingfromscratch.com/line-art-tutorial/ | MAINTENANCE | Site under maintenance mode |
| 13 | https://www.proko.com/how-to-ink/ | JS-ONLY | Requires JavaScript; static content not accessible |
| 15 | https://gurneyjourney.blogspot.com/search/label/line | EMPTY | Label "line" has no posts |

## Method Attempts for Failed URLs

### conceptartempire.com URLs (sources 8, 9)
- Method 2 (curl): 404 returned
- Method 3 (wget): Same result
- Method 4 (Python urllib): Same result
- Method 5 (Wayback CDX API): Returned HTTP 503 (Service Temporarily Unavailable)
- Method 6 (URL variants): No variants succeeded

### cgspectrum.com URLs (sources 10, 11)
- Method 2 (curl): 404 returned
- Method 5 (Wayback CDX API): TLS/SSL handshake timeout

### drawingfromscratch.com (source 12)
- Method 2 (curl): Maintenance mode page returned
- Method 5 (Wayback CDX API): HTTP 503

### proko.com (source 13)
- Method 2 (curl): JavaScript SPA — "Please enable JavaScript" message only
- JavaScript execution not available in this environment

## Notes on WebFetch Tool
The WebFetch tool failed for ALL URLs attempted with it due to an AWS Bedrock authorization error:
"User is not authorized to perform: bedrock:InvokeModelWithResponseStream on resource: us.anthropic.claude-haiku-4-5-20251001-v1:0"
This is an environment configuration issue. All retrieval was done via bash curl/wget/python fallbacks.

## Partial Successes
- Source 2 (Inking comics): Wikipedia page exists but article not written yet
- Source 3 (Pen and ink): Redirects to "Pen" article — full Pen article retrieved and saved
- Source 14 (Gurney Journey pen+and+ink): Label URL with lowercase returns nothing, but properly capitalized "Pen and Ink" label worked
