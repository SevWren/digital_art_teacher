# Tools, Layers, and Resolution

**Status:** Work in progress.

Understanding how digital painting software stores and organises your image is not optional background knowledge — it directly controls the quality of the result you can achieve and your ability to change your mind as you work. The three concepts that underpin all digital painting practice are: how large and detailed to make your canvas before you start (resolution), how to separate work into independent sheets so no stage destroys a previous one (layers), and how to ensure colour is stored in a way that survives screen display and, if needed, print (colour space and bit depth). These concepts are consistent across all good painting software — whether you use Photoshop, Procreate, Krita, Photopea, Clip Studio Paint, or any comparable tool.

---

## Core Concepts

**Resolution and canvas size.** A digital painting is made of pixels — a grid of individually coloured squares. The total number of pixels in your canvas determines how much detail you can include, how large you can print it, and how sharp it looks on screen. Resolution (expressed as pixels per inch, or PPI) only becomes relevant when the image is printed: it tells the printer how densely to pack those pixels onto paper. For screen delivery, total pixel dimensions are what matter; PPI is irrelevant. The critical practical rule is: set up your canvas at or above the size you will finally need before you draw the first stroke. Upscaling a small canvas later does not recover detail — it only makes each pixel larger and blurrier. Platform pixel requirements for social media, portfolio sites, and other destinations change over time and vary by platform; always verify the current specification on the platform's own documentation before exporting.

**Layers.** A layer is a separate, transparent sheet in your document stack. You can paint, draw, or make adjustments on any one layer without disturbing the others above or below it. The core habit layers make possible is working non-destructively: keeping each stage of your painting on its own sheet so that fixing one stage does not undo another. Your master file should always stay layered. Only a flattened copy — all layers merged into one — is exported for delivery.

**Colour space.** A colour space is the agreed set of colour values a file stores and a device can display. For screen delivery (web, social media, portfolio), sRGB is the standard and safest choice: browsers, phones, and most screens understand it reliably. Print workflows may benefit from a wider colour space while working; at export, convert to whatever profile the printer specifies. Do not make up a print profile — ask the print house or check their documentation.

**Bit depth.** An 8-bit file stores 256 brightness steps per colour channel — enough for most screen display. A 16-bit file stores 65,536 steps, which provides headroom during heavy colour corrections or large-scale printing, preventing visible banding in smooth gradients. The practical habit is to paint in 16-bit and convert to 8-bit only if the final delivery format requires it.

**Non-destructive workflow.** Never make permanent changes to base-painted pixels until a decision is final. Use adjustment layers (Curves, Levels, Hue/Saturation, Colour Balance) instead of painting corrections directly onto existing layers. Keep construction, value, colour, and detail work on separate layer groups. Use layer masks rather than the eraser when you want to hide part of a layer — a mask can always be repainted; an erased pixel is gone until you undo.

**Brush tools — opacity vs. flow.** Opacity controls how transparent the entire brush stroke is — at 50% opacity, the stroke is a half-transparent smear of colour. Flow controls how quickly colour builds up as you hold the stylus or mouse in one spot — a low flow means the stroke barely deposits colour in a single pass and builds up gradually with repeated passes. Hard brushes (high hardness setting) leave crisp, clean-edged marks like a rubber stamp. Soft brushes (low hardness) leave marks with edges that fade to transparent, suitable for blending and smooth gradients. Both have their place; choose based on whether you want a defined or a feathered edge.

---

## Practical Decision Criteria

1. **Set canvas size before starting.** Decide your output goal (screen only, print, or both) and set the canvas to the maximum size you will need. If print is uncertain, a canvas roughly equivalent to A4 at 300 PPI (approximately 2480 × 3508 pixels) gives headroom for both good screen display and potential printing without upscaling. Check any platform-specific export targets against that platform's current official documentation at the time of export — do not rely on remembered or hardcoded dimensions.

2. **Set colour space and bit depth before the first mark.** Open the canvas settings in your software and confirm the colour space is sRGB for screen-primary work (or the wider space your print workflow requires) and that bit depth is 16-bit if your software and hardware support it. These settings are much harder to change reliably after painting has begun.

3. **Name every layer and use layer groups.** Before adding paint, rename your default layer and commit to a naming habit. Group related layers (e.g., a folder called "Construction", one called "Value", one called "Local Colour", one called "Lighting", one called "Adjustments"). This costs seconds and saves hours of confusion later.

4. **Never flatten the master file.** After each session, save the layered native file (PSD, KRA, Procreate, CSP, or equivalent). For sharing or delivery, use File > Export or File > Save As to create a separate flattened JPEG or PNG. The layered master is your permanent record; the export is the delivery copy.

5. **Use adjustment layers for global changes.** When you want to shift the overall brightness, colour temperature, or contrast of the image, add an adjustment layer above all other layers rather than painting over existing work. The adjustment can be weakened, modified, or deleted at any point without touching the paint below.

6. **Keep bit depth in mind at export.** If your software produces a 16-bit PNG and your delivery target expects 8-bit (most JPEG exports and some web platforms), convert explicitly at export time so the conversion is intentional and you can verify the result.

---

## Common Failure Modes

- **Starting too small.** A canvas that looks adequate at screen zoom looks blocky and pixelated when printed or displayed at full size. The only fix is to restart at the correct dimensions.

- **Flattening the master early.** Merging all layers into one before work is finished removes the ability to fix any individual stage. If this happens, restore from the last saved layered version and re-establish the layer structure.

- **Working in the wrong colour space.** Painting in sRGB and delivering to a print house that requires a different profile, or vice versa, can shift colours significantly. Always check the target colour space before starting and at export.

- **Ignoring bit depth until too late.** Starting in 8-bit and then applying heavy Curves or exposure corrections introduces visible banding in gradients. If banding appears after adjustments, this is often the cause.

- **Painting over earlier decisions.** Merging a value study into the colour layer, or painting lighting corrections directly onto the base colour, silently destroys the ability to revise those decisions independently. Keep stages on separate layers until they are genuinely final.

- **Confusing opacity and flow.** Setting flow to 100% and opacity to 10% behaves differently from setting opacity to 100% and flow to 10%. The first deposits a thin wash in each pass; the second deposits full-strength colour but in a partially transparent stroke. Mismatched expectations here cause painting to feel unresponsive or to overpower too quickly.

---

## Relationship to Pipeline

_Pipeline step relationships pending #36 validation. This section will be updated once the confirmed pipeline structure exists._
---

## Plain-English Guide

> **Who this is for:** Someone opening a digital painting app for the first time with no formal art training.

### What are tools, layers, and resolution?

When you open a digital painting app, you are working on a grid of tiny coloured squares called pixels. The size of that grid — how many squares wide and tall — is what people mean by the resolution of your canvas. The bigger the grid, the more detail you can paint and the larger you can print the result. Layers are separate sheets of that grid, stacked on top of each other. You can paint on one sheet without disturbing the others, which means you can always go back and fix one part of your work without undoing everything else. The tools — brushes, erasers, adjustment controls — are how you put marks on those sheets and change how they look.

### The key ideas, without the jargon

**Your canvas is like a physical piece of paper — except you choose the size before you start.**
Imagine you are going to paint on paper. Once you have painted on a small postcard, you cannot tape two postcards together and pretend it was always a larger sheet — the join is obvious and the image quality is reduced. The same is true digitally: the canvas must be large enough for your goal before you paint the first stroke. A good starting point if you are unsure is to make your canvas roughly the size of an A4 page at 300 dots per inch — most painting apps have a preset close to this. If you want to post your painting online rather than print it, a canvas around 3000 pixels on the long side is a reasonable general starting point. Check what the platform you are posting to currently recommends; those numbers change.

**Layers are separate sheets of clear film.**
Think of an overhead projector from school, where you can place a fresh clear sheet of film on top of the projected image and draw on the new sheet with a marker. Whatever you draw sits on top without touching the original. You can pull that sheet out, scribble on it, and throw it away — the original is untouched. That is what a layer does: every stage of your painting gets its own clear sheet. When you are done, you can export a flat photocopy of all the sheets together without ever merging the originals.

**The colour space is the recipe that keeps your colours consistent.**
Imagine describing a paint colour to a friend over the phone as "medium red." They might mix something darker or more orange than what you pictured, because "medium red" means different things to different people. A colour space is the agreed recipe that prevents this: it ensures the red you painted on your screen looks like the same red on someone else's screen. For screen delivery — sharing online, posting to social media — choose sRGB. It is the recipe that browsers, phones, and most screens understand.

**Bit depth is how many shades of grey the file can remember.**
Imagine a paint store that sells grey paint in only eight shades from white to black. If you painted a smooth sky gradient using only those eight shades, you would see visible stripes — eight jumps from one shade to the next, with no smooth in-between. A 16-bit file gives your painting tens of thousands of grey steps instead of 256, so gradients stay smooth even after heavy adjustments. Paint in 16-bit if your software supports it; convert to 8-bit only if your final export requires it.

**Opacity and flow are like controlling how watered-down your paint is versus how fast you press the brush.**
Opacity is like the difference between using paint straight from the tube (100% — fully solid and covering) versus thinning it heavily with water (10% — almost transparent, barely visible in one pass). Flow is how fast the paint saturates the paper as you hold the brush still: low flow means the colour builds slowly with repeated strokes; high flow means it reaches full strength quickly. A hard brush leaves a stamp-like edge; a soft brush leaves an edge that fades to nothing.

### What to actually do in your software

1. **Before anything else, set up your canvas correctly.** When you create a new document, look for the canvas size settings. Set the width and height to cover the largest output you might need. Set the colour space to sRGB (or whatever your print house requires). Set bit depth to 16-bit if the option is available. These settings are much harder to change reliably after you have started painting.

2. **Create a new layer before each major stage.** Before you lay down your rough construction sketch, click the new layer button (usually a small page icon with a plus sign in the Layers panel). Before adding colour, create another new layer. Before adding shading, another. Give each layer a short name — "sketch," "flat colour," "shading" — so you know what is on it. Keeping stages separate means you can fix one without redoing all of them.

3. **Use adjustment layers to change the overall look, not direct painting.** When you want to make the whole image brighter, more colourful, or cooler in tone, look for the adjustment layer option (often a half-filled circle at the bottom of the Layers panel, or under Layer > New Adjustment Layer). A Curves or Hue/Saturation adjustment layer sits above your painting like a tinted sheet of glass: it changes how the image looks without touching the paint below. You can delete it, weaken it, or modify it at any time.

4. **Save your layered file, then export a flattened copy for delivery.** When you are done painting, use Save (or Save As) to keep the full layered file in your software's native format — this is your master. Then use Export or Save a Copy to create a JPEG or PNG for sharing. The exported copy is the flat photocopy; your master is the full stack of sheets, safely stored. Never flatten the master.

### Common traps to avoid

- **Starting on a canvas that is too small.** It is very tempting to use a small canvas because it feels faster. The problem appears when you zoom in to add detail, or try to print — the pixels are too large and everything looks blocky. Set the canvas large before you start.

- **Flattening all your layers into one before you are finished.** Once you merge everything into a single layer, you cannot fix any individual stage without affecting everything else. Keep the layers separate until the very end. Export a flat copy for sharing; never flatten the master file itself.

- **Skipping the colour space setting.** If you never check the colour space setting, your software will use whatever default it was set to last. On some setups this is correct; on others it is not. Confirm sRGB is set before you export for screens.

- **Painting your corrections directly onto the base layer.** If you decide the whole image is too dark and you paint a lighter wash directly onto your base colour layer, you have permanently changed it. Add a Brightness/Contrast or Curves adjustment layer instead — you can remove it entirely if you change your mind, and the original paint is untouched.
