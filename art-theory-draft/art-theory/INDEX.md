# Art Theory Knowledge Base — INDEX

**Status:** Work in progress. This repository is the living knowledge store for the project goal: enabling Grok to assist with any question about a digital image the user is planning or currently producing, grounded in professional art theory and digital-art theory.

**Location rule (non-negotiable):** All knowledge files live exclusively under `/home/workdir/artifacts/art-theory/`. Never write theory content to `/tmp` or any other ephemeral path. This directory is the only persistent store across sessions.

## Purpose

Provide a structured, citable body of professional knowledge covering:

- The complete pipeline from brief/ideation to final polish and export.
- The classical and digital fundamentals that govern every stage of that pipeline.

Every response that draws on this base must name the specific file(s) consulted.

## Directory Map

```
art-theory/
├── INDEX.md                          ← this file
├── pipeline/                         ← ordered process knowledge
│   ├── 00-overview.md
│   ├── 01-brief-and-ideation.md
│   ├── 02-reference-gathering.md
│   ├── 03-thumbnailing-composition.md
│   ├── 04-gesture-silhouette.md
│   ├── 05-perspective-construction.md
│   ├── 06-value-lighting.md
│   ├── 07-colour-palette.md
│   ├── 08-form-materials.md
│   ├── 09-rendering-detail.md
│   ├── 10-atmosphere-polish.md
│   └── 11-critique-revision-export.md
├── fundamentals/                     ← theory that governs every stage
│   ├── composition.md
│   ├── perspective.md
│   ├── form-and-construction.md
│   ├── light-and-value.md
│   ├── colour.md
│   ├── anatomy-and-gesture.md
│   ├── materials-and-texture.md
│   └── design-and-shape-language.md
├── digital-practices/
│   ├── workflow-strategies.md
│   ├── tools-layers-resolution.md
│   └── critique-methods.md
├── glossary.md
└── sources.md                        ← provenance of major claims
```

## Usage Rules for Agents

1. Before answering any question about planning, constructing, correcting, or finishing a digital image, load the relevant file(s) from this tree.
2. Prefer the most specific file. If the question spans multiple domains, load the pipeline overview plus the governing fundamental(s).
3. Cite the file path in the response (e.g. “According to `fundamentals/light-and-value.md` …”).
4. Never invent theory. If the required knowledge is absent, state the gap and, if appropriate, follow the controlled extension procedure defined in the `grounded-art-guidance` skill.
5. All new or updated theory must be written back into this same tree under `/home/workdir/artifacts/art-theory/`.

## Current Population Status (work in progress)

- Structure and INDEX established.
- Files present and populated with initial synthesised content:
  - pipeline/00-overview.md
  - fundamentals/composition.md
  - fundamentals/light-and-value.md
  - fundamentals/colour.md
  - fundamentals/perspective.md
  - fundamentals/form-and-construction.md
  - fundamentals/anatomy-and-gesture.md
  - digital-practices/workflow-strategies.md
  - glossary.md
  - sources.md
- Remaining pipeline stage files and additional fundamentals remain to be written.
- Full coverage of every listed file remains an ongoing task. The entire knowledge base is a work in progress.

## Version Notes

- Initial structure created 2026-09-28.
- This INDEX is the single source of truth for the layout. Update it whenever the tree changes.
