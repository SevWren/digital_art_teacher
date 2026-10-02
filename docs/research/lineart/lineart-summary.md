# Line Art Research — Retrieval Summary
# Date: 2026-10-02
# Task: Retrieve complete text of professional pages describing line art, inking, and B&W illustration pipelines

## Results Overview

| # | URL | File | Status | Method | Size |
|---|-----|------|--------|--------|------|
| 1 | https://en.wikipedia.org/wiki/Line_art | lineart-source-1.md | SUCCESS | curl (method 2) | ~3KB |
| 2 | https://en.wikipedia.org/wiki/Inking_(comics) | lineart-source-2.md | FAIL — article doesn't exist | — | note only |
| 3 | https://en.wikipedia.org/wiki/Pen_and_ink | lineart-source-3.md | SUCCESS (redirected to Pen) | curl (method 2) | ~32KB |
| 4 | https://www.ctrlpaint.com/library | lineart-source-4.md | SUCCESS — full library listing | curl (method 2) | ~9KB |
| 5 | https://www.clipstudio.net/how-to-draw/archives/category/line-art | lineart-source-5.md | FAIL — 404 | — | note only |
| 6 | https://www.clipstudio.net/how-to-draw/archives/category/inking | lineart-source-6.md | PARTIAL SUCCESS — inking article retrieved | curl (method 2) | ~15KB |
| 7 | https://www.clipstudio.net/how-to-draw | lineart-source-7.md | SUCCESS — Art Rocket home | curl (method 2) | ~4KB |
| 8 | https://conceptartempire.com/line-art/ | lineart-source-8.md | FAIL — 404 | — | note only |
| 9 | https://conceptartempire.com/inking/ | lineart-source-9.md | FAIL — 404 | — | note only |
| 10 | https://www.cgspectrum.com/blog/line-art | lineart-source-10.md | FAIL — 404 | — | note only |
| 11 | https://www.cgspectrum.com/blog/inking-tips | lineart-source-11.md | FAIL — 404 | — | note only |
| 12 | https://drawingfromscratch.com/line-art-tutorial/ | lineart-source-12.md | FAIL — maintenance | — | note only |
| 13 | https://www.proko.com/how-to-ink/ | lineart-source-13.md | FAIL — JS-only | — | note only |
| 14 | https://gurneyjourney.blogspot.com/search/label/pen+and+ink | lineart-source-14.md | SUCCESS (corrected label case) | curl (method 2) | ~28KB |
| 15 | https://gurneyjourney.blogspot.com/search/label/line | lineart-source-15.md | PARTIAL — empty label | — | note only |

## Successful Retrievals: 6 out of 15 targets

### Source 1 — Wikipedia: Line Art
The Wikipedia article on Line Art covers:
- Definition: images of distinct straight or curved lines against a (usually plain) background
- Usually monochromatic
- Techniques: varying line widths, constant widths (technical illustration), freely varying widths (brush, engraving)
- Relationship to form: lines indicate edges of 2D shapes and 3D forms; contour lines
- History: pre-photography standard for print illustration; black ink on white paper
- Shading techniques: stippling, hatching to simulate grays
- See also: hatching, stippling, halftone, Ben-Day dots, screentone

### Source 3 — Wikipedia: Pen (redirected from Pen and ink)
The Wikipedia article on Pen (which "Pen and ink" redirects to) covers:
- Full history of writing/drawing implements
- Types: modern pens (ballpoint, fountain, rollerball, felt-tip, gel) and historic (quill, reed, dip pen)
- Dip pens and their use in drawing/illustration
- Ink flow mechanisms

### Source 4 — Ctrl+Paint Free Video Library
Complete listing of Matt Kohr's free digital painting video library. Line art and inking relevant sections:
- Section 3 "Drawing 2": "Fluid Linework", "Line Weight" videos
- Section 8 "The Brush Tool": "Clean Lines pt. 1", "Clean Lines pt. 2", "Scanning Your Lineart"
- Section 9: "Line Removal pt. 1/2/3" (removing sketch lines after painting)
- Section 11: "Colored Lineart"
The library progresses from traditional drawing fundamentals through digital tools.

### Source 6 — Clip Studio Paint: "Inking Superhero Comics in Clip Studio Paint"
By Scott Drummond (American comic artist, creator of NIGHTSMOKE, worked for Marvel/Image Comics).
Key content:
- Three traditional inking tools: Brush (Kolinsky sable, sizes 1-3), Dip Pen (G-Pen style), Multiliner Pens (0.1, 0.3, 0.5mm)
- Digital equivalents in Clip Studio Paint: India Ink Smooth brush, built-in G-Pen, custom Multiliners
- Customizing brush pressure curves in Subtool Detail panel
- G-Pen tips: keep under 12-15px at 600 DPI, Circle Tip for crisp lines
- 4 tips for American comic inking style:
  1. Light source affects line weight: thin lines toward light, thick lines away
  2. Spotted blacks: use black fills to show values; "when in doubt, black it out"
  3. Feathering direction: start at thin point, pull INTO the black area (not outward)
  4. Transparent Swatch: use inking tool with transparent color to erase while preserving texture
- Workflow demo: 600 DPI canvas, blue pencil layer at 30% opacity, inks on separate layer
- Mix-and-match tools: Brush for outlines, G-Pen for details, Multiliners for manufactured surfaces

### Source 7 — Clip Studio Paint Art Rocket Home
Directory listing of the Celsys tutorial hub. Confirms existence of line art articles:
- "Liven Up Your Line Art With Smooth, Attractive Lines" (entry-level)
- "Hints on How to Improve your Line Art and Line Quality"
- "Extracting Scanned Line Art for Digital Coloring"

### Source 14 — Gurney Journey: "Pen and Ink" label
James Gurney's blog (Dinotopia creator) has 81 posts tagged "Pen and Ink". The label index page loaded successfully. The blog covers:
- Practical studio tips for illustrators, painters, comic artists
- Traditional pen and ink techniques
- Plein air painting
- Figure drawing, color theory, composition

Blog index shows: Pen and Ink (81 posts), Pencil Sketching (279 posts), Comics/Cartooning (169 posts), Figure Drawing (65 posts), Paint Technique (249 posts).

Note: As of January 2026, Gurney has moved to Substack for new content.

## Key Themes Across Successful Sources

1. LINE WEIGHT VARIATION: All sources emphasize varying line weight as fundamental. Lines facing light = thin; lines in shadow = thick.

2. TOOLS (Traditional):
   - Brushes: Kolinsky sable, widest range but hardest to control
   - Dip pens (G-Pen): Pressure-sensitive metal nib, moderate range
   - Technical pens / Multiliners: Consistent width, good for manufactured/geometric subjects

3. TOOLS (Digital):
   - Clip Studio Paint built-in G-Pen and India Ink brushes
   - Pressure curve customization (Subtool Detail panel)
   - Vector tools for clean lines

4. TECHNIQUES:
   - Hatching and crosshatching for shading without gray
   - Stippling for tonal values
   - Spotted blacks for strong value contrast
   - Feathering for gradual tonal transitions
   - Contour lines for 3D form

5. WORKFLOW:
   - Traditional: sketch → ink over sketch → erase pencils (or use non-photo blue)
   - Digital: sketch layer at reduced opacity (blue tint) → ink layer → hide sketch layer
   - Scanning lineart for digital coloring
   - Line removal techniques in digital painting

6. HISTORY:
   - Pre-photography: line art was the standard for print publication (black ink on white paper)
   - Halftone development changed the role of line art
   - Comics tradition developed specific inking conventions

## Files Written

- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-1.md (Wikipedia Line Art)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-2.md (Inking comics — missing)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-3.md (Wikipedia Pen / pen and ink)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-4.md (Ctrl+Paint library)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-5.md (Clip Studio line-art category — 404)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-6.md (Clip Studio inking article — SUCCESS)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-7.md (Clip Studio Art Rocket home)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-8.md (conceptartempire line-art — 404)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-9.md (conceptartempire inking — 404)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-10.md (CGSpectrum line-art — 404)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-11.md (CGSpectrum inking-tips — 404)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-12.md (drawingfromscratch — maintenance)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-13.md (proko.com/how-to-ink — JS-only)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-14.md (Gurney Journey Pen and Ink label)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-source-15.md (Gurney Journey line label — empty)
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-failures.md
- /home/vercel-sandbox/digital_art_teacher/docs/research/lineart/lineart-summary.md
