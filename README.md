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
