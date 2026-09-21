# Workflow Control

This file defines the end-to-end state machine. Keep execution practical: ask only questions that change the design.

## Stage 0 — Project Init

Create project state and folders when a writable workspace exists.

Recommended project folders:

```text
projects/<project-name>/
├── 00_project/
├── 01_references/
├── 02_concept/
├── 03_sketch/
├── 04_character_master/
├── 05_character_system/
│   ├── turnaround/
│   ├── expressions/
│   ├── actions/
│   └── outfits/
├── 06_visual_identity/
│   ├── 2d_assets/
│   ├── logo/
│   ├── typography/
│   └── graphics/
├── 07_campaign/
├── 08_merchandise/
├── 09_offline/
├── 10_case_study/
└── 11_review/
```

## Stage 1 — Light Intake + Reference Analysis

If the user already gives a clear seed such as "white cat + red apple + bow + magician", do not ask redundant questions.

Only resolve blockers:
- core subject or species;
- must-keep element;
- desired emotional territory;
- intended use if it changes design;
- hard avoid list if any.

Analyze references before ideation. Use `reference-analysis.md`.

## Stage 2 — Five Concept Directions

Generate five directions that differ structurally, not cosmetically.

At least three of these should differ between directions:
- world premise;
- character motivation;
- personality tension;
- meaning of the super-symbol;
- recurring behavior;
- audience/commercial extension;
- visual territory.

Stop at Gate A.

## Stage 3 — Deep IP Brief

After a concept is selected, complete the deeper brief:
- one-line story;
- worldview;
- personality;
- small flaw;
- likes/dislikes;
- ability;
- recurring behavior;
- super-symbol;
- secondary symbols;
- audience;
- likely applications;
- must-keep / must-avoid.

The brief should clarify identity, not become a novel.

## Stage 4 — Five Sketch Explorations

All five sketches share the selected concept and differ mainly in form:
- head silhouette;
- ear placement;
- body proportion;
- hat silhouette;
- bow placement;
- symbol integration;
- prop relationship.

Do not secretly change the concept between sketches.

Stop at Gate B.

## Stage 5 — Character Master

Selected sketch = Character Master v0.

Then:
1. create/refine the final 3D hero;
2. test face, proportion, material and signature props;
3. correct design drift;
4. approve;
5. write Character DNA v1.

Only after approval does the character become locked.

Stop at Gate C.

## Stage 6 — Character System

Generate in controlled batches:
- turnaround;
- expression sheet;
- basic action sheet;
- outfit sheet using user-provided clothing references when available.

Use delta-only changes and closest-reference selection.

## Stage 7 — Visual Identity

Create:
- 2D flat character assets;
- avatar / half-body / full-body / line / monochrome / sticker assets;
- logo system;
- typography direction;
- color roles;
- graphic elements and icon language.

Do not treat 3D render style and brand graphic style as the same system.

Lock Visual DNA v1 at Gate D.

## Stage 8 — Campaign System

Analyze user poster references for:
- information hierarchy;
- title scale;
- composition;
- character-to-type relationship;
- color rhythm;
- graphic density.

Create one hero KV first, then series extensions.

## Stage 9 — Merchandise

Use approved 2D assets and Visual DNA.
Prioritize a small meaningful set before producing a catalog.

## Stage 10 — Offline Experience

First choose context: indoor, outdoor, market/event, pop-up, or exhibition.

Then define one theme and user journey before rendering touchpoints.

## Stage 11 — Case Study + Review

Package the design process and audit it using `qa-review.md`.
Final review: Keep / Improve / Extend / Reuse.
