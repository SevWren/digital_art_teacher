# R1 Research Summary
# Agent: R1
# Retrieved: 2026-10-02

---

## Files Saved

| File | Source URL | Original Target URL | Method | Size (bytes) |
|------|-----------|---------------------|--------|--------------|
| R1-source-1.md | https://en.wikipedia.org/wiki/Concept_art | https://en.wikipedia.org/wiki/Concept_art | 3 (curl) | 10740 |
| R1-source-2.md | https://www.cgspectrum.com/blog/what-is-concept-art | https://www.cgspectrum.com/blog/what-is-concept-art | 3 (curl) | 14820 |
| R1-source-3.md | https://www.cgspectrum.com/blog/what-it-is-like-to-be-a-professional-concept-artist | https://www.cgspectrum.com/blog/concept-art-process | 9 (sitemap scan) + 3 (curl) | 16205 |
| R1-source-4.md | https://conceptartempire.com/what-is-concept-art/ | https://conceptartempire.com/what-is-concept-art/ | 3 (curl) | 6628 |
| R1-source-5.md | https://conceptartempire.com/ | https://conceptartempire.com/ | 3 (curl) | 1820 |
| R1-source-6.md | https://www.cgspectrum.com/blog | https://www.cgspectrum.com/blog | 3 (curl) | 9848 |
| R1-source-11.md | https://www.pencilkings.com/ | https://www.pencilkings.com/ | 3 (curl) | 3038 |

**Total bytes saved: 63,099**

---

## Notes on Successful Retrievals

- **R1-source-1.md** (Wikipedia): Full article text retrieved including all sections: Overview of the Industry, Materials, Themes and Styles, References, and External Links.

- **R1-source-2.md** (CG Spectrum — What is Concept Art): Full article retrieved including concept artist job description, skills, salary, software, and role details.

- **R1-source-3.md** (CG Spectrum — Tyler James interview): Original URL (concept-art-process) returned HTTP 404. Replaced with the best available alternative found via sitemap scan (Method 9): a detailed interview with award-winning concept artist Tyler James (Blizzard Entertainment) covering concept art process, career path, and industry advice.

- **R1-source-4.md** (Concept Art Empire — What is Concept Art): Full article text including workflow description, thumbnailing, character design process, and career advice.

- **R1-source-5.md** (Concept Art Empire homepage): Navigation and category listing only — limited content. Site navigation shows categories: Tips, Inspiration, Reviews, Resources, Interviews.

- **R1-source-6.md** (CG Spectrum blog index): Blog listing page with article titles and summaries. Predominantly navigation and article teasers rather than full article body text.

- **R1-source-11.md** (Pencil Kings homepage): Homepage content including testimonials, popular article titles, and site description. No full article body text.

---

## Failed URLs

| Target URL | Reason for Failure |
|-----------|-------------------|
| https://www.cgspectrum.com/blog/concept-art-process | HTTP 404 — page does not exist; no Wayback archive |
| https://conceptartworld.com/articles/concept-art-workflow/ | Site under maintenance; no Wayback archive of this URL |
| https://conceptartworld.com/ | Site under maintenance; Wayback Machine blocked request as bot traffic |
| https://www.creativebloq.com/digital-art/concept-art-tips-6150013 | HTTP 404 — page removed; no Wayback archive (CDX returned empty) |
| https://www.pencilkings.com/concept-art-process/ | HTTP 404 — page does not exist; no Wayback archive |
| https://gurneyjourney.blogspot.com/2010/06/stages-of-painting.html | Blocked by Google CAPTCHA/reCAPTCHA on all methods; no Wayback archive |
| https://gurneyjourney.blogspot.com/ | Blocked by Google automated traffic detection (CAPTCHA) on all methods |
| https://www.illustrationage.com/concept-art-workflow | Hashcash JS bot-protection blocks all non-browser access; no Wayback archive |
| https://thegnomonworkshop.com/blog/concept-art-workflow | HTTP 404 — page does not exist; no Wayback archive |

---

## WebFetch Tool Status

The WebFetch tool was unavailable during this entire research session due to an AWS Bedrock IAM authorization error:
`User: arn:aws:iam::841162713753:user/bedrock-sonnet-invoke is not authorized to perform: bedrock:InvokeModelWithResponseStream on resource: us.anthropic.claude-haiku-4-5-20251001-v1:0`

All successful retrievals therefore relied on Method 3 (curl with browser User-Agent) as the primary method, with Method 9 (sitemap scan) used for URL3.

---

## Method Coverage Summary

- Method 1 (WebFetch): Attempted for all 15 URLs in first batch — all failed due to tool API error
- Method 2 (Wayback CDX API): Attempted for all failed URLs — most returned no snapshots
- Method 3 (curl): Primary successful method — retrieved 7 URLs successfully
- Method 4 (wget): Not needed — Method 3 was sufficient for accessible pages
- Method 5 (Python urllib): Attempted for Gurney Journey — returned HTTP 404 (CAPTCHA redirect)
- Method 6 (Wayback direct snapshots): Attempted for conceptartworld.com (blocked as bot), conceptartworld.com/articles/workflow (not archived), creativebloq, gurneyjourney (not archived)
- Method 7 (URL variants): Confirmed no alternate variants worked for 404 pages
- Method 8 (Domain homepage scan): Used to verify maintenance status of conceptartworld.com
- Method 9 (Sitemap scan): Successfully used for cgspectrum.com — found alternative article for URL3
