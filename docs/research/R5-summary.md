# R5 Research Summary
# Agent: R5
# Date: 2026-10-02
# Mission: Retrieve complete text of academic and professional educational pages about digital painting workflows, traditional-to-digital workflows, and formal digital art instruction.

## Retrieval Results

| # | Original Target URL | Status | Source File | Method Used | Notes |
|---|---|---|---|---|---|
| 1 | https://en.wikipedia.org/wiki/Digital_painting | SUCCESS | R5-source-1.md | 3 (curl) | Full article text retrieved |
| 2 | https://en.wikipedia.org/wiki/Concept_art | SUCCESS | R5-source-2.md | 3 (curl) | Full article text retrieved |
| 3 | https://en.wikipedia.org/wiki/Digital_art | SUCCESS | R5-source-3.md | 3 (curl) | Full article text retrieved (~38KB) |
| 4 | https://gurneyjourney.blogspot.com/2010/06/stages-of-painting.html | FAILURE | R5-source-4.md | ALL FAILED | Post deleted from Blogspot; no Wayback archive |
| 5 | https://gurneyjourney.blogspot.com/2009/02/value-study-first.html | FAILURE | R5-source-5.md | ALL FAILED | Post deleted from Blogspot; no Wayback archive |
| 6 | https://gurneyjourney.blogspot.com/ | SUCCESS | R5-source-6.md | 3 (curl) | Homepage + recent posts retrieved |
| 7 | https://www.ctrlpaint.com/library | SUCCESS | R5-source-7.md | 3 (curl) | Full free video library curriculum retrieved |
| 8 | https://www.ctrlpaint.com/ | SUCCESS | R5-source-8.md | 3 (curl) | Homepage retrieved |
| 9 | https://www.svslearn.com/blog | FAILURE | R5-source-9.md | 3 (curl) | 404 not found; no Wayback archive |
| 10 | https://www.svslearn.com/blog/digital-illustration-workflow | FAILURE | R5-source-10.md | 3 (curl) | 404 not found; no Wayback archive |
| 11 | https://www.gnomon.edu/blog | PARTIAL | R5-source-11.md | 3 (curl) | Redirected to homepage; homepage content captured |
| 12 | https://www.gnomon.edu/digital-painting | PARTIAL | R5-source-12.md | 3 (curl) | Page doesn't exist; redirected to homepage |
| 13 | https://www.pencilkings.com/digital-painting-workflow/ | FAILURE | R5-source-13.md | ALL FAILED | 404; no Wayback archive |
| 14 | https://www.drawingfromscratch.com/ | FAILURE | R5-source-14.md | ALL FAILED | Site in maintenance mode |
| 15 | https://www.illustrationage.com/ | FAILURE | R5-source-15.md | ALL FAILED | JS bot detection; Wayback blocked |

## Counts
- Total targets: 15
- Full success: 6 (URLs 1, 2, 3, 6, 7, 8)
- Partial success: 2 (URLs 11, 12 — homepage captured)
- Complete failures: 7 (URLs 4, 5, 9, 10, 13, 14, 15)

## Key Content Successfully Retrieved

### Wikipedia: Digital Painting (R5-source-1.md)
Comprehensive article covering: technological origins (Sketchpad 1963, RAND Tablet 1968, MacPaint 1984, Photoshop 1987, Corel Painter 1991, Krita), applications in film/games/advertising/publishing, complete list of digital art software (28 programs with platform/license data).

### Wikipedia: Concept Art (R5-source-2.md)
Covers: industry overview, concept artist roles and salaries, digital vs. traditional materials, themes and styles (blue sky stage, speed paints, matte paintings), iteration process.

### Wikipedia: Digital Art (R5-source-3.md)
Comprehensive ~38KB article covering: history of digital art, digital painting section, AI art, digital art education, scholarship and archives (computer demos, installation art, internet art, blockchain), 3D animation generation process, full software list, subtypes, organizations.

### Gurney Journey Homepage (R5-source-6.md)
Blog by Dinotopia creator James Gurney. Covers illustrators, plein-air painters, sketchers, comic artists, animators. Blog index shows 5,000+ posts across categories including: Paint Technique (249 posts), Color (248), Composition (105), Watercolor Painting (355), Computer Graphics (107), Preliminary Sketches (75), Visual Perception (153), Figure Drawing (65). Recent posts visible (2025-2026). Note: Blog has transitioned heavily to Substack; specific older posts (2009, 2010) are no longer accessible.

### Ctrl+Paint Library (R5-source-7.md)
THE MOST SUBSTANTIVE CURRICULUM DOCUMENT RETRIEVED. Complete free video library curriculum for digital painting education, organized as an 18-section progressive course:
1. Digital Painting 101 (overview, navigation, layers, brush, color, blending)
2. Traditional Drawing (pencils, visual measuring, contour lines, block-in, crosshatching, negative space, constructive form)
3. Drawing 2 (drawing habit, fluid linework, line weight, form vs. shape, perspective)
4. Composition Basics (principles of design: scale, repetition, emphasis, balance, movement, unity; visual hierarchy)
5. Using Reference Materials (reference process, design, photo studies, film studies, gesture drawing)
6-7. Making the Switch to Digital Tools (Photoshop navigation)
8. The Brush Tool (stroke types, control, opacity/flow, blending, custom brushes, smudge tool)
9. Basic Painting Techniques (temp layers, value/light/form, grayscale, hard/soft edges, rendering, line removal, flat painting)
10. Adding Surface Details (photos, textures, overlays, glossiness, warp tool)
11. Painting With Color (color schemes, contrast, vibrant colors, palette unity, skin tones, grayscale-to-color)
12. Masking & Selections (lasso, masking, pen tool, layer groups)
13. Vector Tools (vector bootcamp series)
14. The User Interface (workspace, resolution, histogram, scanning lineart)
15. Uniquely Digital Techniques (adjustment layers, color correction, puppet warp, eyedropper, chop and warp, clone stamp, gradient map)
16. Efficiency Through Repetition (swarms, thumbnail iteration, smart objects)
17. Theory & Mindset (staying objective, beginner mindset, expectation vs. reality, the learning curve)
18. Study Habits (assignments, learning to learn, importance of editing, idea generation)

### Ctrl+Paint Homepage (R5-source-8.md)
Mission statement: free learning resource for digital painting basics. Bite-sized videos (~5 min). Organized like a school curriculum from basic to advanced. Student-supported (no ads/subscriptions).

### Gnomon Homepage (R5-sources 11 & 12)
Gnomon School of Visual Effects — North Hollywood, CA. Programs: 4-year BFA, 2-year Certificate in Digital Production for Entertainment, 10-week individual courses, Foundation in Art & Design. Specializations: Game Art, Modeling & Texturing, VFX Animation, Character & Creature Animation, Virtual Production. Stats: 1,000+ industry-employed graduates, 98% BFA placement rate. Ranked highly by Hollywood Reporter, Animation Career Review, The Rookies (2025).

## Environmental Notes
- WebFetch tool (Method 1) failed for ALL URLs due to AWS Bedrock permission error in this sandbox environment.
- All successful retrievals used Method 3 (curl with browser User-Agent).
- Wayback Machine intermittently blocked requests as suspected bot traffic.
- Several high-value target URLs (Gurney Journey specific posts, SVSLearn articles, Pencil Kings workflow article) no longer exist and have no archived copies.
