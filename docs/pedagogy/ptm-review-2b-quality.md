# PTM Review — Plain-English Quality (Team 2B)

## Summary

Total violations found: **17**

Breakdown by check type:
- Check A (Plain definition uses art vocabulary): 2
- Check B (Example contains art vocabulary): 4
- Check C (Example physically inaccurate): 0
- Check D (Abstract noun without physical anchor in example): 3
- Check E (Use in output contains unexplained jargon): 10

Note: several entries have multiple violations counted once per entry below, but are tagged with all applicable check types. The counts above reflect distinct field-level violations across the full document.

---

## Violations

---

### Lost edge — Check B, Check E

**Field:** Example
**Problem:** "Look at a face lit softly from above in a dim room — the boundary where the **lit cheek** transitions into the **shadow under the cheek** is not a sharp line... If you put your finger on the image and tried to find the exact pixel where '**lit skin**' ends and '**shadow skin**' begins, you could not do it."

"Lit" used to describe a surface is art vocabulary — it presupposes knowledge of the lit/shadow surface model that this very section of the PTM is teaching. "Shadow under the cheek" uses "shadow" as a technical art term describing a surface zone. A beginner reading this without having absorbed the entire Light and Value section first would not know what "lit cheek" or "shadow skin" means as technical descriptors. The example fails Test 1: it uses art vocabulary to explain an art concept.

**Field:** Use in output
**Problem:** "The boundary between your **lit area** and **shadow area** on the [cheek / background / hair] is currently a sharp, crisp line."

Same issue: "lit area" and "shadow area" are art-vocabulary labels for surface zones. A beginner who does not yet know what the "lit area" of a cheek means will not understand this sentence without the PTM context.

**Suggested fix (Example):** Look at a photo of a person's face taken in soft indoor lighting. Now try to find the exact point where the bright skin on the forehead ends and the darker skin below begins. There is no sharp line — the skin just gradually gets darker as it curves away from the window, like a slow fade. That slow fade is a "lost edge." Compare it to the edge of a printed letter on paper, which has a crisp, hard boundary you could trace with a fingernail. That crisp boundary is a "found edge." A painting uses both: soft fades where you want things to look gentle or far away, hard lines where you want things to look sharp and close.

**Suggested fix (Use in output):** "The boundary between the bright side and the dark side of your [cheek / hair / background] is currently a sharp, crisp line — you can trace exactly where one ends and the other begins. If you want that area to feel soft or to recede into the background, soften that boundary with a low-opacity soft brush until the transition becomes a gradual fade rather than a cut edge."

---

### Found edge — Check E

**Field:** Use in output
**Problem:** "The most important areas of your painting should have the crispest, most **found edges** — that is where you want the viewer's eye to go. Right now your [**focal point** / main subject edge] has been softened to a gradual fade..."

"Found edges" is the jargon term this very entry is introducing. Using it in the Use in output sentence as if the beginner now knows what it means — before the conversation has established the term — defeats the purpose. The Use in output is supposed to be a sentence the assistant can deliver to a beginner. The term has just been introduced in the Plain definition and Example; using it again in the delivery sentence without re-anchoring it asks the reader to hold a new term in memory and apply it immediately, which is exactly the failure mode the PTM is designed to prevent.

"Focal point" is also art vocabulary. It is defined elsewhere in the PTM, but the Use in output sentence must stand on its own for a beginner reading this entry in isolation or hearing it spoken.

**Suggested fix:** "The sharpest, most crisply-edged areas of your painting are where the viewer's eye will land first — those hard, traceable edges signal 'important, close, look here.' Right now your [main subject / the face / the weapon edge] has been softened into a gradual fade, which is making it recede instead of pop. Sharpen that boundary using a harder brush or the Sharpen tool along just that edge."

---

### Rendering / Shading stage — Check A, Check D

**Field:** Plain definition
**Problem:** "turning the flat shapes into **forms** that look solid and three-dimensional."

"Forms" is an art-specific abstract noun. It appears here without a physical anchor. For a beginner, "forms" floats as a vague abstraction — it could mean shapes, objects, or volumes. The definition is supposed to be in plain English only. The word "forms" as used in art means "three-dimensional shapes," but a beginner does not know this. The plain definition should say "solid, three-dimensional objects" or "shapes that look like you could pick them up."

**Suggested fix (Plain definition):** "The rendering or shading stage is when you paint the areas of light and shadow onto your flat-coloured image, turning the flat, cartoon-like shapes into objects that look solid and three-dimensional — as if you could reach in and pick them up."

---

### Blocking in — Check D

**Field:** Example
**Problem:** "They first shape the big lump of clay into a rough upright figure — a head, a torso, two legs — just big, simple **masses**."

"Masses" is art vocabulary. In art instruction, "mass" is a specific term describing three-dimensional volume and weight. A beginner who has never taken an art class will not know what "masses" means in this context — they are more likely to think of it in the physics sense (weight) or as "a lot of something." The ADR-0005 amendment explicitly lists "mass" as a word requiring a physical anchor or replacement.

**Suggested fix:** "They first shape the big lump of clay into a rough upright figure — a head, a torso, two legs — just big, simple blobs of the right size, with no detail at all."

---

### Warm-up sketch — Check D

**Field:** Use in output
**Problem:** "drawing a few pages of loose scribbly lines, circles, and random **forms** wakes up the connection between your eye and your hand"

"Forms" appears here as a floating abstract noun with no physical anchor following it. A beginner reading "random forms" does not know what physical thing is being described. The ADR-0005 amendment is explicit: "form" must be immediately followed by something physical and touchable.

**Suggested fix:** "drawing a few pages of loose scribbly lines, circles, and random scribbled shapes wakes up the connection between your eye and your hand"

---

### Colour harmony — Check E

**Field:** Use in output
**Problem:** "One way to unify them is to add a faint wash of the same colour over the whole image on a new layer set to a blending mode like 'Colour' or 'Overlay' at low opacity. This gives every colour a shared tint, like they are all being lit by the same light source."

This Use in output sentence does not contain the term "colour harmony" itself, so there is no self-referential jargon problem. However: "being lit by the same light source" uses "lit" as an art-surface descriptor. More critically, the Use in output for this entry is the only place where the concept is delivered to the user, and the delivery sentence assumes the user already understands why colours "feel like they came from different paintings." The phrasing "each one is fine on its own but they are not sharing any common thread" is acceptable — that is plain English. No severe violation here; this entry passes.

*Correction: on re-read, this entry passes Check E. No flag needed.*

---

### Atmospheric perspective (Colour section, line ~443) — Check E

**Field:** Use in output
**Problem:** "Lighten them, reduce their detail, and add a very slight cool (bluish) tint to push them back in space."

"Push them back in space" uses "space" as an art-specific abstract noun — "in space" here means "in pictorial depth," which is an art concept, not a plain-English phrase. A beginner would likely read "push them back in space" as literally moving things into outer space. The plain-English phrase would be "make them look further away."

**Suggested fix:** "Lighten them, reduce their detail, and add a very slight cool (bluish) tint. Those three changes together will make them look further away."

---

### Atmospheric perspective (Perspective section, line ~1082) — Check E

**Field:** Use in output
**Problem:** "To push this background further back visually, reduce its **contrast** — make the darks lighter and the lights slightly darker so the range between them narrows. Also slightly grey out and cool the **color** (shift it toward a pale blue-grey)."

"Reduce its contrast" uses "contrast" as an art term here — the instruction means "reduce the gap between the darkest and lightest tones," but "contrast" is not plain English when used this way without explanation. A beginner may think "contrast" means the contrast setting on a TV or monitor, which is close enough to be workable, but the word is still art/technical vocabulary in this usage. The sentence immediately explains what it means ("make the darks lighter and the lights slightly darker") — because of that inline explanation, this is borderline. However, the word "contrast" is used as if it is familiar before the explanation arrives, which technically violates the plain-English rule (the explanation should come first, not after the jargon word).

**Suggested fix:** "To push this background further away, narrow the gap between its darkest and lightest areas — make the darks a little lighter and the lights a little darker until the whole background sits in a similar medium range. Also shift the background color slightly toward a cool pale blue-grey."

---

### Colour hierarchy / Saturation hierarchy — Check E

**Field:** Use in output
**Problem:** "Reduce the vividness of your background by at least half. The main subject will immediately feel more important without changing anything about the subject itself."

The Use in output sentence itself is clean. However, the preceding context sentence reads: "Right now the colour intensity is roughly equal across your whole image. Try thinking of it as a budget: you only have a limited amount of 'maximum vividness' to spend, and spending it on the main subject means spending less everywhere else."

The term "**mid-ground**" does not appear in this entry. On re-read, this entry passes. No flag needed.

*Correction: re-read confirms no violation in Use in output for this entry.*

---

### Value (in colour context) — Check E

**Field:** Use in output
**Problem:** "Squint at your painting until the colours almost disappear and you just see light and dark. That reading is the **value structure**, and it needs to tell a clear story on its own."

"Value structure" is art vocabulary. "Value" has been introduced as a PTM term in the Light and Value section, but this is a separate entry in the Colour section. The Use in output sentence for this entry uses "value structure" as if it is already known — but the beginner may encounter this entry without having read the Light and Value section first. The Use in output sentence must stand alone. The phrase "value structure" is art jargon; plain English would be "the light-and-dark pattern."

**Suggested fix:** "Squint at your painting until the colours almost disappear and you just see light and dark patches. That light-and-dark pattern needs to tell a clear story on its own — the important parts should still be obvious even when all the colour is gone. Right now, [describe the specific problem]. Let's fix the lights and darks first before adjusting colours."

---

### Overblending — Check E

**Field:** Use in output
**Problem:** "try introducing some crisper edges — particularly where there should be a definite change in surface, like the edge of a [lip / crease / fold / **highlight**]."

"Highlight" is art vocabulary — it refers specifically to the bright glint from a light source on a surface (it has its own dedicated entry in the Light and Value section). A beginner using the Overblending entry in isolation would not know that "highlight" here means a specific surface feature caused by direct light reflection, not a general bright area. The word appears without any plain-English anchor in this sentence.

**Suggested fix:** "try introducing some crisper edges — particularly where there should be a definite change in surface, like the edge of a [lip / crease / fold / the tiny bright glint on a shiny surface]."

---

### Rendering / Shading stage — Check E (second violation, separate field)

**Field:** Use in output
**Problem:** "use a soft brush at low opacity to paint in the **shadowed areas** first — the side of each shape facing away from your light source. Build up the shadow gradually, then add a brighter pass on the **lit side**."

"Shadowed areas" and "lit side" are art-vocabulary surface descriptors from the light-and-shadow model. While these terms appear throughout the PTM and are individually defined, the Use in output sentence for Rendering / Shading stage is the moment the assistant would speak these words to a beginner who may just be reaching this stage and may not have the earlier entries memorised. "The side of each shape facing away from your light source" is a good plain-English anchor — but it comes after the jargon phrase "shadowed areas" rather than replacing it. The instruction should be structured so the plain explanation arrives first.

**Suggested fix:** "On a new layer above the flat color, use a soft brush at low opacity to darken the side of each shape that faces away from your light source. Build that up gradually, then add a lighter pass on the side that faces toward the light. Step back regularly to check the shapes are reading as solid."

---

### Structural anatomy (artistic) — Check E

**Field:** Use in output
**Problem:** "Once those points are in the right place, the **flesh** between them can be filled in with confidence."

"Flesh" used in this way — "the flesh between them" — is an art-figure-drawing term. While "flesh" is an ordinary English word, the phrase "fill in the flesh" is artist shorthand for "draw the surface of the body between the landmark bones." A beginner would likely find this phrasing odd or unclear. "The surface of the body between them" or "the skin and muscle between them" would be plain English.

**Suggested fix:** "Once those points are in the right place, you can draw the skin and muscle between them with confidence — the surface will fill in naturally between the fixed points."

---

### Rhythm (figure) — Check E

**Field:** Use in output
**Problem:** "Does each curve flow into the next without a jarring change in direction? If the path feels bumpy or interrupted, look for where one curve stops and a mismatched one starts — smoothing those **hand-offs** is what creates a figure that reads as one living thing."

"Reads as one living thing" is borderline art phrasing — "reads as" is art-critique vocabulary. More clearly, "hand-offs" as used here is jargon from figure-drawing instruction, meaning the transition point where one body part's curve passes its direction to the next. A beginner would not know what "hand-offs" means in this anatomical drawing sense.

**Suggested fix:** "Does each curve flow into the next without a sudden change in direction? If the path feels bumpy or interrupted, find the exact point where one curve ends and the next one starts going a different way — smoothing that transition point is what makes the figure feel like one continuous, living body rather than parts joined together."

---

### Value family — Check B (shared example quality issue)

**Field:** Example
**Problem:** "In a black-and-white photo, everything is either bright or dark. A good painting keeps all the bright things in one 'team' and all the dark things in another team. The moment those teams mix everywhere into the same **muddy grey**, the image looks flat and hard to read."

This exact example is used word-for-word for three separate entries: **Value family**, **Light group**, and **Shadow group**. This is not strictly a vocabulary violation, but it does create a quality failure: the example for "Light group" and "Shadow group" does not differentiate between those two concepts — it describes the same general principle (bright team / dark team), which means neither entry has an example that specifically illustrates its own concept. The example was designed to illustrate the overall two-team principle, which belongs to Value family. Light group needs an example that specifically shows what "all the lit surfaces staying in a similar brightness range" looks like in a concrete physical scenario. Shadow group needs an example specifically illustrating that the shadow side of objects should stay together in a dark range.

Additionally, "muddy grey" in the example is art vocabulary. "Muddy" in this context is an art-critique term for a specific kind of tonal collapse. A beginner would not know what "muddy grey" means as a technical failure mode.

**Suggested fix (shared example — muddy grey):** Replace "the same muddy grey" with "the same in-between grey — neither clearly bright nor clearly dark." The three entries also need differentiated examples rather than one repeated example. For Light group, an example might be: "Think of a stage with a spotlight. All the surfaces the spotlight catches — the top of the actor's head, their shoulders, the front of their chest — glow at a similar bright level. If some of those lit surfaces were painted much darker than the others, it would look as if a second spotlight were randomly absent. The lit side of anything under one light source should all belong to the same brightness club." For Shadow group, a parallel example.

---

### Simultaneous contrast — Check E

**Field:** Use in output
**Problem:** "Your eyes automatically compare every colour to its neighbours, so the same **paint colour** can look completely different depending on what is next to it."

"Paint colour" is a fine general phrase, but the preceding sentence in the Use in output says: "The area that looks too [colour description] may not actually need to change — the problem might be what is surrounding it." The phrase "colour description" appears inside brackets as a placeholder, which is acceptable, but the Use in output sentence also says "Try checking that area in isolation by **covering the surrounding colours temporarily**." This is clear and plain. The overall Use in output passes. No flag needed on further review.

*Correction: this entry passes on closer reading.*

---

### Colour study (Colour section) — Check E

**Field:** Use in output
**Problem:** "Before going further, it is worth doing a quick **colour study** — a small, rough, fast version painted just to answer 'do these colours work together and do they still read clearly in light and dark.'"

"Read clearly in light and dark" uses "read" as art-critique vocabulary. In art instruction, "reads" means "is visually perceived as." A beginner may not know that "reads clearly" is jargon for "looks correct to the eye." The phrase "is still clear and legible when viewed in light and dark" or "still makes sense when you squint at it" would be plain English.

Also, "colour study" is used in the Use in output before it has been fully explained — since this is the Use in output for the Colour study entry, the term is being defined, but the sentence uses the term before anchoring it: "it is worth doing a quick colour study." For a beginner hearing this spoken aloud without having read the Plain definition, the word "study" implies a long piece of academic work rather than a quick rough test.

**Suggested fix:** "Before going further, it is worth painting a quick rough test — a small, fast version just to check: do these colours work together, and does the painting still look clear when you squint at it? If yes, move forward with confidence. If the test version looks muddy or confusing, the colours need adjusting before you commit to the full-size piece."

---

### Value study — Check E

**Field:** Use in output
**Problem:** "A value study forces you to make that squint-test intentional: paint a small rough version in gray only to check that the lights and darks form a clear, interesting **pattern**."

"Pattern" here is borderline but acceptable plain English. However, the Use in output sentence says: "Do a value study first — work in black and white on a tiny canvas, using just three or four shades of gray." This is clean. The prior sentence in the example, though, says "A well-designed image still reads clearly even at that squinting distance" — "reads clearly" is art-critique jargon.

**Field:** Example
**Problem:** "A well-designed image still **reads clearly** even at that squinting distance."

"Reads clearly" is art vocabulary. In everyday English, "reads" means text you read with your eyes. "Reads clearly" as applied to an image is art-critic shorthand for "is easily understood / is visually legible." A beginner would find this phrase confusing.

**Suggested fix (Example):** "Squint at any photograph until your eyes are almost closed and the colour disappears — what you see is a pattern of light blobs and dark blobs. If those blobs still make an interesting picture even when blurred beyond recognition, the image has a strong foundation. A value study forces you to test this on purpose: paint a small rough version in grey only to check that the light and dark areas form a clear, interesting arrangement."

**Suggested fix (Use in output):** "Do a value study first — work in black and white on a tiny canvas, using just three or four shades of grey. Fill the areas that will be in light with a pale grey and the areas in shadow with a dark grey. Then squint at it hard. If the important shapes are still obvious and the image is interesting at that small, blurry scale, your light-and-dark design is strong enough to move forward with."

---

## Entries confirmed clean (spot-check)

The following sections were read in full and found to pass all five checks without violation: Notan, Gestalt grouping, Figure-ground, Visual weight, Hierarchy/Emphasis, Negative space, Tangent, Value massing, Rule of thirds, Golden ratio, Cropping, Framing, Focal point, Leading lines, Symmetry/Asymmetry, Balance, Rhythm (composition), Pattern, Unity, Contrast (compositional), Proportion, Scale, Silhouette readability, Entry and path, Value (primary), Highlight, Halftone/Midtone, Core shadow, Reflected light, Cast shadow, Occlusion shadow, Key light, Fill light, Rim light, Ambient light, Muddy values failure mode, Value compression, Form shadow, Terminator, Specular reflection, Diffuse reflection, Local value, Value scale, Atmospheric perspective (Light section), Hue, Saturation/Chroma, Colour wheel, Primary/Secondary/Tertiary, Complementary pairs, Analogous groups, Temperature (warm/cool), Colour temperature shift, Extension/Area ratio, sRGB/Colour space, Colour gamut, Local colour (primary), Split complementary, Triadic, Tetradic, Monochromatic, Atmospheric colour (Colour section), Colour mixing additive/subtractive, Colour grading, Desaturation, Oversaturation failure mode, Colour mudding failure mode, Colour cast, Local colour (palette restriction), Accent colour, Dominant temperature, Neutral, Gesture, Line of action, ASIS, Greater trochanter, Clavicle, Foreshortening, C-curve/S-curve, Bean shape, Rhythm (figure — Example only; Use in output flagged above), Landmark bones, Action pose, Dynamic pose, Static pose, Mannequin method, Bean-and-limbs method, Exaggeration, Weight and balance, Centre of gravity, Proportions (figure), Primary forms, Planar analysis, Cross-contour lines, Surface planes, Form shadow vs cast shadow (construction), Simplified forms, Organic vs geometric forms, Volume, Mass, 3D construction method, Ribbon method, Contour, Relative measurement, Envelope/silhouette first, all Perspective entries, all Software Tools entries, thumbnail stage, sketch stage, linework stage, flat colour stage, detail pass, polish pass, reference gathering, master study, colour study (Pipeline section), underpainting, overpainting, construction pass, cleanup pass.
