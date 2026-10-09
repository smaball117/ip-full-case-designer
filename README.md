# IP Full Case Designer

A reusable AI skill for building an **original character IP as a design system**, not a chain of reference-image adaptations.

> 核心原则：**先建立系统，再生产内容。参考图是可选输入，不是设计发动机。**

```text
Idea / Brief
    ↓
IP Core
    ↓
5 Concept Directions
    ↓ Gate A
Deep Brief + Narrative Engine
    ↓
5 Form Explorations
    ↓ Gate B
Character Master
    ↓ Gate C
Character DNA
    ↓
Character System
    ↓
Visual DNA + Typography + Graphics + Layout Grammar
    ↓ Gate D
Theme Engine
    ↓
Campaign / Merchandise / Offline
    ↓
Case Study + Review
```

## v0.2 architecture

```text
SKILL.md
├── systems/
│   ├── 01_ip-core/
│   ├── 02_character/
│   ├── 03_visual-language/
│   ├── 04_layout/
│   ├── 05_campaign/
│   ├── 06_application/
│   └── 07_engine/
├── references/        # legacy + task execution details
├── templates/
└── examples/
    └── apple-magic-cat/
```

## What changed in v0.2

v0.1 was mainly a workflow orchestrator. Real-world testing showed that this still encouraged:
```text
reference → imitate structure → replace character
```

v0.2 adds the missing design-system layer:

- **IP Core** — why the IP exists
- **Narrative Engine** — where themes come from
- **Character DNA** — what keeps the character on-model
- **Visual DNA** — how the brand world looks
- **Shape Grammar** — how new forms are translated
- **Layout Grammar** — reusable compositions without a reference
- **Theme Engine** — campaigns derived from world rules
- **Prompt Compiler** — compact prompts generated from the system
- **Reference Router** — references affect named variables only
- **QA Engine** — system-based validation

## Default reference policy

1. **Original Design** — default.
2. **Reference Assisted** — reference controls a named variable.
3. **Adaptation** — only on explicit request.

## Four hard gates

- **Gate A:** concept
- **Gate B:** sketch
- **Gate C:** Character DNA
- **Gate D:** Design System / Visual DNA

## Test project

**可可 / Coco — Apple Magic Cat**

The Coco project is the first real validation case and is being used to expose missing rules, prompt duplication, reference over-dependence, and system gaps.

## Version

`0.2.0-dev` — design-system architecture.
