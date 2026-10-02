# Failed URL Retrievals
# Date: 2026-10-02

This file documents URLs that could not be retrieved after exhausting all retrieval steps.

---

## URL 3: https://www.gnomon.edu/blog/digital-painting-workflow

**All steps attempted:**

- Step 1 (Direct fetch): HTTP 404 Not Found
- Step 2 (Wayback 2024): Wayback Machine API returned 404 (URL not archived)
- Step 3 (Wayback multiple timestamps): Not archived — Wayback Machine confirms "The Wayback Machine has not archived that URL."
- Step 4 (Wayback availability API): Wayback API itself returned HTTP 404
- Step 5 (Google cache): Google cache returned a redirect page with no real content ("Please click here if you are not redirected...")
- Step 6 (HTTP variant): HTTP variant also returned 404
- Step 7 (www variant / without www): gnomon.edu without www also returned 404 for this path
- Step 8 (trailing slash): HTTP 404
- Additional attempts: Tried https://www.gnomon.edu/blog (returns homepage, not blog listing), https://www.gnomon.edu/news/digital-painting-workflow (404), https://www.gnomon.edu/articles/digital-painting-workflow (404), https://www.gnomon.edu/resources/digital-painting-workflow (404), https://gnomon.edu/blog/digital-painting-workflow (404)

**Conclusion:** The specific blog post does not exist at gnomon.edu. The gnomon.edu/blog path redirects to the homepage. This URL was likely a hypothetical or the post has been taken down.

---

## URL 6: https://www.3dtotal.com/tutorial/the-complete-digital-painting-workflow

**All steps attempted:**

- Step 1 (Direct fetch via WebFetch): Detected redirect to https://store.3dtotal.com/tutorial/the-complete-digital-painting-workflow (301 Moved Permanently)
- Step 1b (Follow redirect to store.3dtotal.com): HTTP 404 Not Found
- Step 2 (Wayback 2024): Wayback Machine confirms "The Wayback Machine has not archived that URL."
- Step 3 (Wayback 2023-10-15): HTTP 404 (Wayback has no snapshot)
- Step 3b (Wayback 2022-06-01): HTTP 404
- Step 4 (Wayback availability API): API returned 404 (URL not indexed)
- Step 5 (Google cache): Google cache returned redirect page with no real content
- Step 6 (HTTP variant): Not tried separately (main domain returns 404 for this path)
- Step 7 (without www): Tried 3dtotal.com/tutorial — HTTP 404
- Additional attempts: Tried https://www.3dtotal.com/tutorials — HTTP 404; https://www.3dtotal.com/tutorial — HTTP 404

**Conclusion:** This URL does not exist anywhere retrievable. The tutorial path at 3dtotal.com/tutorial/* returns 404, and the Wayback Machine has no archived snapshots of this specific URL. The domain has moved tutorial content to store.3dtotal.com but that redirected URL also 404s.

---

## URL 7: https://www.svslearn.com/blog/digital-illustration-workflow

**All steps attempted:**

- Step 1 (Direct fetch): HTTP 404 Not Found
- Step 2 (Wayback 2024): Wayback Machine confirms "The Wayback Machine has not archived that URL."
- Step 3 (Wayback multiple timestamps): Not archived
- Step 4 (Wayback availability API): API returned 404 (URL not indexed)
- Step 5 (Google cache): Google cache returned redirect page with no real content
- Step 6 (HTTP variant): HTTP 404
- Step 7 (without www - svslearn.com): HTTP 404 for this specific path
- Step 8 (trailing slash): HTTP 404
- Additional attempts: https://www.svslearn.com/blog (404), https://www.svslearn.com/blog/illustration-workflow (404), https://www.svslearn.com/resources (404), https://www.svslearn.com/articles/digital-illustration-workflow (404), http://www.svslearn.com/blog/digital-illustration-workflow (404), https://www.svslearn.com/digital-illustration-workflow (404), https://www.svslearn.com/essentials (404). Note: svslearn.com main page (/) returns 200 — the site exists but uses Workshops, Essentials, Children's Books, Graphic Novels, Podcast sections — no /blog path exists.

**Conclusion:** The SVS Learn website (School of Visual Storytelling) exists but does not have a /blog section. The specific URL was likely hypothetical or the blog has been removed/reorganized. The site structure does not include a blog.
