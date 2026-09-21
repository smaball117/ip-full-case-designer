# IP Full Case Designer

A reusable AI workflow skill for building a complete character IP system from reference analysis and concept exploration to character assets, visual identity, campaigns, merchandise, offline experiences, and project review.

> 核心原则：**前面做决策，后面做继承。**

```text
Reference / Idea
      ↓
Light Intake
      ↓
5 Concept Directions
      ↓  GATE A
Deep IP Brief
      ↓
5 Sketch Explorations
      ↓  GATE B
3D Character Master
      ↓  GATE C
Character System
(turnaround / expressions / actions / outfits)
      ↓
Visual Identity
(2D assets / logo / typography / graphics)
      ↓  GATE D
Campaign System
      ↓
Merchandise
      ↓
Offline Experience
      ↓
Case Study + Review
```

## Architecture

The main `SKILL.md` is intentionally small. It acts as an **orchestrator** and loads detailed knowledge only when needed.

```text
SKILL.md
├── references/
├── templates/
└── examples/
    └── apple-magic-cat/
```

## Why modular instead of one giant prompt?

A full IP case contains very different jobs. Keeping every rule active at once creates prompt noise, instruction competition, higher context cost, and harder debugging.

This repository separates:
- workflow control from design knowledge;
- Character DNA from Brand Visual DNA;
- locked assets from changeable variables;
- reference intent from reference appearance;
- project state from decision history.

## Four hard approval gates

- **Gate A — Concept:** choose one of five genuinely different IP directions.
- **Gate B — Sketch:** choose one character form exploration.
- **Gate C — Character Master:** approve the final 3D character and lock Character DNA v1.
- **Gate D — Visual Identity:** approve the visual identity system and lock Visual DNA v1.

## Current status

**v0.1 — workflow architecture**

First test project: **Apple Magic Cat / 苹果魔法猫**.

## Design philosophy

1. Reference images must be assigned a role before use.
2. Concept direction and form exploration are different stages.
3. Character identity is locked only after the approved 3D master.
4. Downstream generation should describe the delta, not re-describe the whole character.
5. Use the closest approved reference for each generation.
6. 3D character assets and 2D graphic assets should coexist.
7. Every output has a status: `draft / revise / approved / rejected / locked`.
8. Final review records `Keep / Improve / Extend / Reuse`.

## Version

`0.1.0` — initial architecture.
