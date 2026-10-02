# Pipeline Overview — From Planning to Completion

**Status:** Work in progress.

A professional digital-art pipeline moves an idea from brief to finished, presentable file through a sequence of decisions that progressively reduce uncertainty. Each stage has a governing fundamental; skipping a stage or solving its problems too late is the most common source of rework.


## Plain-English Guide

### What this is

The pipeline is a set of steps done in a specific order so that problems are caught early, when they are cheap to fix, rather than late, when they are buried under hours of finished work. Each step answers one question and leaves a clear result the next step can build on.

### Why it matters for your painting

Skipping steps does not save time — it hides problems that cost far more time later. A layout problem caught at the thumbnail stage is a two-minute fix; the same problem caught after the rendering is finished can mean repainting hours of work.

### The one thing to remember

Solve the biggest problems first. Layout and light-and-dark are the cheapest things to change at the start of a painting; they are the most expensive things to change once detail work sits on top of them.

### Common beginner pitfall

Starting with fine detail — textures, colour, small features — before the layout and light structure are settled, then having to repaint everything when the foundation turns out to be wrong.

## Stage Sequence

| # | Stage | Primary question answered | Governing fundamental(s) |
|---|-------|---------------------------|---------------------------|
| 01 | Brief & Ideation | What must this image achieve and for whom? | Design / Shape language, Composition |
| 02 | Reference Gathering | What visual evidence do I need? | All fundamentals (observation) |
| 03 | Thumbnailing & Composition | What is the strongest arrangement of major shapes? | Composition, Design |
| 04 | Gesture / Silhouette | Does the pose or major form read clearly at a distance? | Anatomy & Gesture, Form |
| 05 | Perspective & Construction | Do the forms sit convincingly in space? | Perspective, Form & Construction |
| 06 | Value / Lighting | Is the light design clear and hierarchical? | Light & Value |
| 07 | Colour & Palette | Do the colours support hierarchy and mood? | Colour |
| 08 | Form & Materials | Do surfaces respond correctly to the light? | Materials & Texture, Form |
| 09 | Rendering & Detail | Where does the eye rest and where does it travel? | Composition, Light & Value |
| 10 | Atmosphere & Polish | Are depth, focus, and final adjustments coherent? | Perspective (atmospheric), Colour, Light |
| 11 | Critique, Revision & Export | Does the image meet the brief and technical requirements? | All + Critique methods |

## Core Principles Across the Pipeline

1. **Solve large problems early.** Composition, value hierarchy, and major proportions are cheapest to change at the thumbnail and block-in stages.
2. **Separate concerns.** Value can be designed before colour; construction can be solved before surface detail.
3. **One decision at a time.** Each stage should leave a clear, checkable result before the next stage begins.
4. **Primary sources of truth.** The approved thumbnail, the value study, and the construction drawing remain primary references; later stages should not silently override them without conscious revision.

## How to Use This Overview

- Identify the stage the user is currently in (or the earliest stage that is still unresolved).
- Load the corresponding stage file under `pipeline/` and the governing fundamental file(s) under `fundamentals/`.
- Answer from those files, citing them explicitly.