# Art Theory Knowledge Base — INDEX

**Status:** Work in progress. This directory is the modular knowledge base for the digital art teaching assistant. It covers art theory, construction fundamentals, pipeline guidance, and digital practice. Universal principles live here from the start. Subject-specific entries (anatomy, construction landmarks, surface systems for a given motif) are added through the promotion workflow defined in `CLAUDE.md` and `CLAUDE/skills/art-guidance/grounded-art-guidance/SKILL.md`.

**Location rule (non-negotiable):** All knowledge files live under this `art-theory/` directory. Write new theory content here only — never to a temporary or session-scoped path. Subject-specific entries retrieved from the web are staged first in `art-theory-pending.md` (at the repo root) and promoted here only after passing the six-check review and receiving explicit user approval.

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
│   ├── 00-overview.md                ← unvalidated internal spec; see #36
│   └── [01–11 step files removed — pending #36 pipeline validation]
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
4. When the required knowledge is absent from this tree, state the gap. If the gap is subject-specific (anatomy, construction landmarks, markings, or surface systems for a particular motif), follow `CLAUDE.md` → load `grounded-art-guidance`. Never invent theory.
5. All new or updated theory promoted from staging must be written into this tree. Update this INDEX whenever a new file is created.

## Current Population Status (updated 2026-10-02)

**Pipeline step files removed 2026-10-02.** Issues #7–#17 (pipeline/01–11) were written before issue #36 (comprehensive pipeline validation gate) was completed. Those files have been rolled back pending #36. See GitHub Issue #36.

### Pipeline — blocked on #36

| File | Status |
|---|---|
| pipeline/00-overview.md | Present — unvalidated internal spec pending #36 |
| pipeline/01-brief-and-ideation.md | **Removed — pending #36** |
| pipeline/02-reference-gathering.md | **Removed — pending #36** |
| pipeline/03-thumbnailing-composition.md | **Removed — pending #36** |
| pipeline/04-gesture-silhouette.md | **Removed — pending #36** |
| pipeline/05-perspective-construction.md | **Removed — pending #36** |
| pipeline/06-value-line-hierarchy.md | **Removed — pending #36** |
| pipeline/07-colour-tone-pass.md | **Removed — pending #36** |
| pipeline/08-form-materials.md | **Removed — pending #36** |
| pipeline/09-rendering-detail.md | **Removed — pending #36** |
| pipeline/10-atmosphere-polish.md | **Removed — pending #36** |
| pipeline/11-critique-revision-export.md | **Removed — pending #36** |

### Fundamentals — fully populated

| File | Status |
|---|---|
| fundamentals/composition.md | Written + Plain-English Guide |
| fundamentals/perspective.md | Written + Plain-English Guide |
| fundamentals/form-and-construction.md | Written + Plain-English Guide |
| fundamentals/light-and-value.md | Written + Plain-English Guide |
| fundamentals/colour.md | Written + Plain-English Guide |
| fundamentals/anatomy-and-gesture.md | Written + Plain-English Guide |
| fundamentals/materials-and-texture.md | Written + Plain-English Guide |
| fundamentals/design-and-shape-language.md | Written + Plain-English Guide |

### Digital practices — fully populated

| File | Status |
|---|---|
| digital-practices/workflow-strategies.md | Written + Plain-English Guide |
| digital-practices/tools-layers-resolution.md | Written + Plain-English Guide |
| digital-practices/critique-methods.md | Written + Plain-English Guide |

### Support files

| File | Status |
|---|---|
| glossary.md | Present |
| sources.md | Present |

## Version Notes

- Initial structure created 2026-09-28.
- Fundamentals and digital-practices files written 2026-10-01 (issues #18–#21).
- Plain-English Guide sections added to pre-existing files 2026-10-01 (issue #29).
- Pipeline step files (01–11) written 2026-10-01 then rolled back 2026-10-02: those files were committed before issue #36 (pipeline validation gate) was completed. They are removed pending #36.
- This INDEX is the single source of truth for the layout. Update it whenever the tree changes.
