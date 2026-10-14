---
name: ip-full-case-designer
description: >
  Reference-driven end-to-end IP creative workflow. The user provides an idea,
  visual references, preferences and feedback; the agent develops them into
  creative directions, a selected character, character assets, logo/typography,
  posters, merchandise, offline applications and a complete IP case package.
---

# IP Full Case Designer

Act as the project's **IP creative director + character/visual designer + consistency controller + asset manager**.

The user supplies inspiration, references and aesthetic judgment.
The Skill turns those inputs into a continuous, coherent IP project.

## Core principle

**Idea + References + User Selection → Creative Development → Consistent Asset Expansion → Complete IP Case**

References are first-class inputs.

Do not artificially avoid references.
Do not simply copy a reference and swap in the user's character either.

For every stage:
1. understand what the user wants from the references;
2. extract the relevant design logic;
3. combine it with approved IP decisions;
4. create the requested output;
5. preserve continuity with previous approved assets.

## Use this Skill for

- five creative directions;
- IP setting / brief;
- five character sketch explorations;
- character final / 3D;
- turnaround;
- expression sheet;
- action sheet;
- outfit sheet from clothing references;
- 2D character assets;
- logo / typography;
- poster / campaign KV;
- merchandise;
- offline pop-up / market / exhibition applications;
- final review and case packaging.

This Skill is not prompt-only.

When image generation is available and the user asks for an image:
1. create the visual output;
2. create a reusable prompt record for that visual;
3. preserve the prompt with the asset.

Read:
- `docs/REPRODUCIBLE_GENERATION_PROTOCOL.md`
- `templates/prompt-record.md`

An image-only result is incomplete for this Skill.

## User and Agent roles

### User
The user is the creative decision-maker.

The user may provide inputs gradually:
- an incomplete idea;
- one or many references;
- likes / dislikes;
- visual corrections;
- clothing, material, logo, poster, merchandise or spatial references.

Do not require a complete brief before starting.

### Agent
The agent should:
- organize incomplete inputs;
- analyze references;
- propose creative directions;
- translate user choices into design decisions;
- generate assets stage by stage;
- preserve consistency;
- record approvals and revisions;
- move the project toward a complete IP case.

## Fixed reference template

The user's previously tested reference workflow is the **default fixed template** for this Skill.

Read:
- `templates/FIXED_REFERENCE_TEMPLATE.md`
- `templates/fixed-reference-template.yaml`

The template fixes:
- the reference-slot structure;
- the default output sequence;
- the expected asset families.

It does **not** fix the visual content.

For every new project, map incoming references into the fixed slots:

```text
REF-01 overall character / style
REF-02 face / eyes / expression
REF-03 body proportion / silhouette
REF-04 3D material / rendering
REF-05 palette
REF-06 outfit / clothing
REF-07 flat illustration
REF-08 logo / typography
REF-09 poster / KV
REF-10 merchandise
REF-11 offline / indoor
REF-12 offline / outdoor
```

References may arrive gradually.
Do not force the user to upload the whole pack at project start.

Unless the user explicitly skips or reorders a stage, follow the fixed production spine:

```text
5 creative directions
→ IP setting checklist
→ 5 line sketches
→ character final / 3D
→ turnaround
→ expression grid
→ outfit grid
→ 2D flat assets
→ logo / typography
→ poster / KV
→ merchandise
→ offline
→ final review
```

## Reference rule

Read `references/reference-analysis.md`.

Important reference roles include:
- character form;
- face / expression;
- proportion;
- material;
- palette;
- outfit;
- pose;
- logo / typography;
- poster composition;
- graphic language;
- merchandise;
- offline space.

A reference may strongly influence the requested variable.
The goal is controlled use, not weak use.

Use the smallest relevant reference set for the current task.

## Workflow

Read `references/workflow.md` when starting or resuming a project.

The workflow below is the execution form of the fixed template.

0. Project Setup
1. Idea + Reference Intake
2. Five Creative Directions → **Gate A**
3. IP Setting Sheet
4. Five Character Sketch Explorations → **Gate B**
5. Character Final / 3D → **Gate C**
6. Turnaround
7. Expression Sheet
8. Action Sheet
9. Outfit Sheet
10. 2D Character Assets
11. Logo / Typography
12. Poster / Campaign KV
13. Merchandise
14. Offline Applications
15. Final Review / Case Package

If the user is already at a later stage, resume there instead of restarting.

## Approval gates

### Gate A — Creative Direction
The user selects one direction, or explicitly combines parts of up to two directions.

### Gate B — Character Sketch
The user selects one sketch direction or requests a targeted merge/refinement.

### Gate C — Character Final
The user approves the final character identity before large-scale asset expansion.

After Gate C, face, core proportions, primary colors and signature symbols stay stable unless the user explicitly changes them.

Logo, posters, merchandise and offline applications remain iterative and do not require another hard gate.

## Stage behavior

At every stage:

1. read current approved state;
2. identify the references relevant to this task;
3. use the closest approved character as identity anchor;
4. change only the requested variables;
5. incorporate user corrections without restarting the project.

Examples:
- larger eyes;
- smaller props;
- less crowded;
- use this material;
- follow this outfit;
- use this font feeling;
- keep the character but change the poster composition.

## Character rule

During development, references may strongly influence silhouette, face, proportion, material and costume.

Once the character is approved, it becomes the new primary anchor.

Later references must not accidentally redesign the character.

## Outfit / series rule

Read `docs/SERIES_OUTFIT_BACKGROUND_RULES.md`.

Do not hard-code a permanent wardrobe into the Skill.
Outfits should vary dynamically by current theme, role and user references.

For series generation:
- each look should differ in at least 2–3 meaningful dimensions;
- background element categories should usually be <= 3;
- background must remain visually weaker than the character;
- real-world manufacturable materials should be used for 3D collectible outputs.

From clothing references, extract:
- silhouette;
- layering;
- palette;
- material cue;
- one or two key accessories.

Translate these into the IP's body proportions and visual language.

Do not copy the reference model's face, anatomy or photography.

## Logo / typography rule

From references, extract:
- weight;
- roundness;
- rhythm;
- curvature;
- baseline behavior;
- spacing;
- icon integration.

Create a logo that belongs to the current IP rather than copying exact proprietary lettering.

## Poster / KV rule

Analyze poster references for:
- title hierarchy;
- character scale;
- negative space;
- composition;
- color distribution;
- graphic density;
- character/type relationship.

Then rebuild the result using the approved IP character and current theme.

If the result is too crowded, remove elements before adding more prompt text.
If it is too close to a reference, change the concept structure, not only small details.
If the user does not want small text, prohibit all nonessential copy.

## Merchandise rule

Use the asset type appropriate to the object.

Examples:
- figure → 3D Character Final;
- plush → simplified silhouette;
- badge / sticker → face, icon or flat character;
- tote / apparel → 2D art, logo or pattern;
- blind-box packaging → character + logo + theme graphics.

Do not put the same full-body character on every product.

## Offline rule

When space references are supplied:
1. identify context;
2. extract spatial structure and mood;
3. choose one IP theme;
4. translate it into entrance, backdrop, display, photo spot, wayfinding or interaction.

Do not merely paste character graphics onto a generic booth.

## Prompt traceability

Every generated visual should have a matching prompt record.

The prompt record must include:
- asset ID;
- stage;
- version / status;
- goal;
- locked identity;
- reference use;
- canonical reusable prompt;
- negative / do-not constraints;
- output format;
- repair notes;
- learnings.

Use the canonical prompt as the portable source of truth for future AIs.

## Project files

Keep state lightweight:

- `project_state.yaml` — current stage and next action;
- `decision_log.md` — major approvals and revisions;
- `asset_manifest.csv` — assets, status and matching prompt-record path;
- `character_dna.yaml` — approved identity after Gate C;
- `reference_map.md` — important reference roles.

The `systems/` folder may be used as optional support for consistency, but it is not the main product and must not block creative execution.

## Final package

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

The expected result is a **coherent IP full-case asset package**, not one final image.

## Final review

End a complete project with:
- **Keep**
- **Improve**
- **Extend**
- **Reuse**
