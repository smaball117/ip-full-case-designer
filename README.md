# IP Full Case Designer

A **reference-driven IP creative full-case Skill**.

The user brings an idea, visual references and ongoing feedback.
The Agent turns those inputs into a complete IP project, from creative directions and character development to logo, posters, merchandise and offline applications.

> 核心原则：**用户提供灵感与审美判断，Skill 负责创意整理、连续执行、风格统一和完整交付。**

## What it does

```text
Idea + References
      ↓
Reference Analysis
      ↓
5 Creative Directions
      ↓  GATE A
IP Setting Sheet
      ↓
5 Character Sketches
      ↓  GATE B
Character Final / 3D
      ↓  GATE C
Turnaround
Expressions
Actions
Outfits
      ↓
2D Character Assets
      ↓
Logo / Typography
      ↓
Poster / Campaign KV
      ↓
Merchandise
      ↓
Offline Applications
      ↓
Final Review / Case Package
```

## This Skill is not

- a single-image generator;
- a prompt-only tool;
- a fully automatic no-reference design system;
- a "swap my character into this reference" tool;
- a rigid pipeline that ignores user choices.

## Fixed template

The reference workflow already tested with Coco is now the **default fixed template** for every new IP project.

The template fixes the workflow structure, not the visual style.

Reference slots:

```text
REF-01 Character / overall style
REF-02 Face / eyes / expression
REF-03 Proportion / silhouette
REF-04 3D material / rendering
REF-05 Color palette
REF-06 Outfit / clothing
REF-07 Flat illustration
REF-08 Logo / typography
REF-09 Poster / KV
REF-10 Merchandise
REF-11 Offline / indoor
REF-12 Offline / outdoor
```

Default outputs:

```text
5 creative directions
→ IP setting
→ 5 sketches
→ 3D final
→ turnaround
→ expressions
→ outfits
→ flat assets
→ logo
→ posters
→ merchandise
→ offline
→ review
```

See:
- `templates/FIXED_REFERENCE_TEMPLATE.md`
- `templates/fixed-reference-template.yaml`

## Working style

The user can feed references gradually.

Examples:
- character face reference;
- proportion reference;
- clothing reference;
- material reference;
- typography reference;
- poster reference;
- merchandise reference;
- offline-space reference.

The Agent identifies what each reference should control, then uses it at the appropriate stage.

## Three important approvals

- **Gate A — Creative Direction**
- **Gate B — Character Sketch**
- **Gate C — Character Final**

After Gate C, the approved character becomes the primary identity anchor for later work.

## Final deliverable

```text
PROJECT_NAME/
├── 01_brief/
├── 02_references/
├── 03_concept-directions/
├── 04_sketch/
├── 05_character-final/
├── 06_3d/
├── 07_turnaround/
├── 08_expressions/
├── 09_actions/
├── 10_outfits/
├── 11_2d-assets/
├── 12_logo-typography/
├── 13_posters/
├── 14_merchandise/
├── 15_offline/
└── 16_review/
```

The result is a **complete IP asset package**, not one final image.

## Architecture

```text
SKILL.md
├── docs/
│   └── SKILL_POSITIONING_v0.3.md
├── references/
│   ├── workflow.md
│   ├── reference-analysis.md
│   ├── character-design.md
│   ├── character-consistency.md
│   ├── visual-identity.md
│   ├── application-system.md
│   └── qa-review.md
├── templates/
├── systems/          # optional support modules
└── examples/
    └── apple-magic-cat/
```

## Test project

**可可 / Coco — Apple Magic Cat**

Coco is the first real project used to validate the workflow through:
character exploration → 3D → expressions → outfits → flat illustration → logo → posters → merchandise / offline.

## Version

`0.3.0-dev` — reference-driven full-case workflow.


## Second validation project

**水母星守 / Jellyfish Star Guardian**

This project validates:
- starting from a loose idea;
- combining selected parts from multiple references;
- converting 2D concept thinking into real collectible-toy 3D language;
- using manufacturable materials;
- producing varied outfit series;
- controlling background complexity;
- saving a reusable prompt record for every major visual.

See:
`examples/jellyfish-star-guardian/`
