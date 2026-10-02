# R4 Retrieval Failures
# Agent: R4
# Date: 2026-10-02

---

## Summary of Failed Retrievals

The following target URLs could not be retrieved with substantive content despite exhausting all retrieval methods (direct curl, Wayback CDX API, Wayback timestamps, alternate URL variants):

---

### 1. https://en.wikipedia.org/wiki/Creature_design
- **Reason:** Wikipedia does not have an article titled "Creature design". The page returns a "page does not exist" message.
- **Methods tried:** Method 3 (curl browser UA)
- **Fallback:** Retrieved Wikipedia "Concept art" article (https://en.wikipedia.org/wiki/Concept_art) instead. Saved as R4-source-1b.md.

---

### 2. https://en.wikipedia.org/wiki/Character_design (creature sections)
- **Reason:** Wikipedia's "Character design" page is a disambiguation page only. There are no creature-specific sections. It only lists links to "Character creation", "Characterization", and "Model sheet".
- **Methods tried:** Method 3 (curl browser UA)
- **Result saved:** R4-source-2.md (contains the full disambiguation page text)

---

### 3. https://www.cgspectrum.com/blog/creature-design
- **Reason:** Returns HTTP 404. Page has been removed or moved. No Wayback Machine archive available (Wayback CDX API returns empty archived_snapshots).
- **Methods tried:** Method 3 (curl), Method 2 (Wayback CDX), Method 6 (Wayback timestamps)
- **Result saved:** R4-source-3.md (404 page text)

---

### 4. https://www.cgspectrum.com/blog/how-to-become-a-creature-designer
- **Reason:** Returns HTTP 404. Page has been removed or moved. No Wayback Machine archive available.
- **Methods tried:** Method 3 (curl), Method 2 (Wayback CDX), Method 6 (Wayback timestamps)
- **Result saved:** R4-source-4.md (404 page text)

---

### 5. https://conceptartempire.com/creature-design/
- **Reason:** Returns HTTP 404. Page has been removed or moved. No Wayback Machine archive available.
- **Methods tried:** Method 3 (curl), Method 2 (Wayback CDX), Method 6 (Wayback timestamps)
- **Result saved:** R4-source-6.md (404 page text)

---

### 6. https://80.lv/articles/creature-design/
- **Reason:** Returns "Page Not Found" on 80.lv. The URL pattern does not match 80.lv's article URL structure. No Wayback Machine archive available. The tag pages /articles/tags/creature-design/ and /articles/tags/creature/ also return "Page Not Found".
- **Methods tried:** Method 3 (curl), Method 2 (Wayback CDX), Method 7 (URL variants), Method 8 (domain homepage scan for creature links)
- **Fallback:** Found and retrieved a creature/character design article from 80.lv homepage: "Creating an Alien Character for a Sci-Fi Short Film with Blender & Substance 3D" (https://80.lv/articles/creating-an-alien-character-for-a-sci-fi-short-film-with-blender-substance-3d). Saved as R4-source-9b.md.

---

### 7. https://www.gnomon.edu/blog/creature-design
- **Reason:** URL redirects to/returns Gnomon homepage (no separate blog section at this path). No Wayback Machine archive available.
- **Methods tried:** Method 3 (curl), Method 2 (Wayback CDX)
- **Result saved:** R4-source-10.md (Gnomon homepage content)

---

### 8. https://www.gnomon.edu/blog
- **Reason:** URL returns the same Gnomon homepage content. No dedicated blog page at this URL.
- **Methods tried:** Method 3 (curl)
- **Result saved:** R4-source-11.md (Gnomon homepage content)

---

### 9. https://www.thegnomonworkshop.com/blog/creature-design
- **Reason:** Returns HTTP 404. Page does not exist. No Wayback Machine archive available.
- **Methods tried:** Method 3 (curl), Method 2 (Wayback CDX)
- **Result saved:** R4-source-12.md (404 page text)
- **Fallback:** Retrieved The Gnomon Workshop blog index (https://www.thegnomonworkshop.com/blog), which contains extensive list of creature/character art workshop titles. Saved as R4-source-12b.md.

---

### 10. https://gurneyjourney.blogspot.com/search/label/creature
- **Reason:** Google/Blogger serving CAPTCHA challenge page blocking automated access. Multiple methods (curl with various user agents, python urllib) all result in the same CAPTCHA block. No Wayback Machine archive available.
- **Methods tried:** Method 3 (curl), Method 5 (python urllib — returned HTTP 429), Method 2 (Wayback CDX)
- **Result saved:** R4-source-13.md (CAPTCHA block page text)

---

### 11. https://www.creativebloq.com/digital-art/creature-design
- **Reason:** Returns HTTP 404. Page has been removed or moved. No Wayback Machine archive available.
- **Methods tried:** Method 3 (curl), Method 2 (Wayback CDX), Method 6 (Wayback 2024/2023 timestamps)
- **Fallback:** Retrieved the creativebloq.com/digital-art index page as alternative content. Saved in R4-source-14.md.

---

### 12. https://www.zbrushcentral.com/c/articles
- **Reason:** Returns "That page doesn't exist or is private." — the forum section requires login or is restricted.
- **Methods tried:** Method 3 (curl)
- **Result saved:** R4-source-15.md (error page text with recent ZBrushCentral artwork listings)

---

## Statistics

- Total target URLs: 15
- Successfully retrieved with substantive content: 6 (Wikipedia Concept Art, conceptartempire creature gallery, 80.lv homepage, 80.lv alien character article, cgspectrum blog index, thegnomonworkshop blog index)
- 404/Not Found: 6 (cgspectrum creature-design, cgspectrum how-to-become, conceptartempire creature-design, creativebloq creature-design, 80.lv creature-design, thegnomonworkshop blog/creature-design)
- CAPTCHA/Access Blocked: 1 (gurneyjourney.blogspot.com)
- No article exists: 1 (Wikipedia Creature_design)
- Disambiguation page only: 1 (Wikipedia Character_design)
- Redirects to homepage (no content): 2 (gnomon.edu/blog, gnomon.edu/blog/creature-design)
- Private/login required: 1 (ZBrushCentral /c/articles)
- No Wayback Machine archives found for any failed URL.
