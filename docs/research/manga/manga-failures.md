# Manga Research - Failed Retrievals
# Retrieved: 2026-10-02

## Summary of Failures

| # | URL | Error | Methods Tried | Notes |
|---|-----|-------|---------------|-------|
| 3 | https://www.clipstudio.net/how-to-draw/archives/158906 | Returns binary JPEG, no text | curl, wget | Old article ID returns image asset, not HTML page |
| 4 | https://www.clipstudio.net/how-to-draw/archives/category/manga | 404 Not Found | curl | Old URL structure; site rebranded to Art Rocket; new URL is /category/comic-manga |
| 6 | https://www.webtoons.com/en/creator-hub/ | 404 Not Found | curl | Webtoons creator hub URL structure changed |
| 7 | https://www.webtoons.com/en/creator-hub/en/create/how-to-create | 500 Internal Server Error | curl | Invalid URL structure |
| 8 | https://medibangpaint.com/en/use-guide/2020/10/what-is-manga/ | 404 Not Found | curl | Article removed from MediBang site |
| 9 | https://medibangpaint.com/en/use-guide/ | 404 Not Found | curl | Use-guide section no longer active |
| 13 | https://www.tofugu.com/japan/how-to-make-manga/ | 404 Not Found | curl, Wayback | Article removed; Wayback Machine temporarily offline |
| 14 | https://www.cgspectrum.com/blog/how-to-make-manga | 404 Not Found | curl, Wayback | Article removed; Wayback Machine temporarily offline |
| 15 | https://www.cgspectrum.com/blog/manga-art-style | 404 Not Found | curl, Wayback | Article removed; Wayback Machine temporarily offline |

## Infrastructure Issues

- **Wayback Machine (archive.org)**: Temporarily offline during retrieval session (2026-10-02). All Wayback CDX API queries returned "Temporarily Offline" page.
- **WebFetch tool**: Authentication failure - AWS Bedrock Claude Haiku model not authorized (403 error). Fell back to curl/wget/python methods for all URLs.

## Successful Fallback Retrievals

For URLs 3 and 4 (Clip Studio), the following equivalent/superior articles were retrieved as bonus sources:
- https://www.clipstudio.net/how-to-draw/archives/160963 - "Pro Artist's Guide to Comic & Manga Layouts, Paneling, Flow" (saved as manga-source-16.md)
- https://www.clipstudio.net/how-to-draw/archives/155309 - "The Difference Between Digital Manga and Hand-Drawn Manga" (saved as manga-source-17.md)
- https://www.clipstudio.net/how-to-draw/archives/172579 - "How to Make a Webtoon Page: Complete Guide & Video Tutorial" (saved as manga-source-18.md)
- https://www.clipstudio.net/how-to-draw/archives/159080 - "Inking Superhero Comics in Clip Studio Paint" (saved as manga-source-19.md)
