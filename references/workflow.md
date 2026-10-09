# Workflow Control v0.3

This workflow matches the intended working style:

**the user brings ideas and references gradually, and the agent develops them into a complete IP case.**

Do not force the user to complete every stage in one session.
Do not restart approved work when the project resumes later.

## Stage 0 — Project Setup

Recommended folders:

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

Create lightweight project state only.
Do not generate heavy documentation before real decisions exist.

## Stage 1 — Idea + Reference Intake

Accept incomplete input.

The user may provide:
- a sentence;
- rough story;
- mood;
- one or many references;
- an existing character;
- specific likes and dislikes.

Identify:
- what the user wants to create;
- what must be kept;
- what should be avoided;
- which references affect which parts.

Ask only questions that materially change the next creative step.

Use `reference-analysis.md`.

## Stage 2 — Five Creative Directions

Generate five genuinely different directions using the user's idea + references.

Each direction should include:
- direction name;
- core concept;
- character mood;
- story / worldview hook;
- visual emphasis;
- commercial extension;
- risk / caution.

The five directions should not be five cosmetic variants.

Stop at **Gate A**.

The user may:
- select one;
- combine parts of up to two;
- reject all and request another round.

## Stage 3 — IP Setting Sheet

After Gate A, consolidate a practical brief:

- name / working name;
- Chinese / English name when relevant;
- identity / role;
- personality;
- useful flaw;
- likes / dislikes;
- world premise;
- one-line story;
- signature symbol;
- palette tendency;
- audience;
- priority applications;
- Must Keep;
- Must Avoid.

Mark assumptions clearly.
Do not lock details the user has not approved.

## Stage 4 — Five Character Sketch Explorations

Use the approved setting plus current character references.

Explore:
- head silhouette;
- face;
- eyes;
- ears / hair / horns;
- body proportion;
- costume silhouette;
- prop relationship;
- signature-symbol integration.

All five should still feel like the same IP concept.

The goal is comparison, not final rendering.

Stop at **Gate B**.

## Stage 5 — Character Final / 3D

From the selected sketch:

1. refine face and silhouette;
2. refine proportions;
3. refine costume and props;
4. apply material references if supplied;
5. create the hero render;
6. repair identity drift from feedback.

Examples of targeted feedback:
- "the face looks too much like a bear";
- "make the cat pupils larger";
- "use star-shaped eye highlights";
- "use flocked material";
- "make props smaller".

Stop at **Gate C** once the user approves the character.

After Gate C, create/update `character_dna.yaml`.

## Stage 6 — Turnaround

Create:
- front;
- side;
- back;
- optional 3/4 hero.

Preserve:
- same face;
- same proportions;
- same costume;
- same prop scale;
- same material.

The turnaround explains construction, not redesign.

## Stage 7 — Expression Sheet

Default output may be 6 or 9 expressions.

Expressions should reveal personality, not only swap mouths.

Possible expressions:
- greeting;
- laugh;
- cry;
- angry;
- surprised;
- sleepy;
- affection;
- approval;
- confusion.

Do not add text unless requested.

## Stage 8 — Action Sheet

Use the character's story and recurring behavior.

Possible actions:
- holding the core symbol;
- using the signature prop;
- running;
- sitting;
- eating;
- collecting;
- repairing;
- celebrating.

Actions should become reusable sticker / poster / merchandise assets.

## Stage 9 — Outfit Sheet

The user may continue feeding clothing references.

For each outfit reference:
1. extract silhouette;
2. extract layering;
3. extract palette;
4. extract material;
5. choose 1–2 key accessories;
6. translate into the character's body and visual style.

Do not inherit the reference person's anatomy or photography.

Common outputs:
- 3x3 outfit grid;
- seasonal set;
- themed set;
- single outfit refinement.

## Stage 10 — 2D Character Assets

Translate the approved character into practical graphic assets:

- flat full body;
- half body;
- avatar;
- line art;
- monochrome;
- sticker;
- small icons / signature symbols.

The user may provide flat-illustration references.
Use them to control graphic treatment while preserving character identity.

## Stage 11 — Logo / Typography

The user may provide logo / font references.

First extract:
- roundness;
- weight;
- rhythm;
- curvature;
- baseline;
- spacing;
- symbol integration.

Then create:
- Chinese mark;
- English mark;
- combination lockup;
- color version;
- monochrome version;
- simplified mark when useful.

Do not add random microcopy.

## Stage 12 — Poster / Campaign KV

The user may provide poster, typography and layout references.

Before generating, identify:
- theme;
- what is learned from each reference;
- character priority;
- title hierarchy;
- element density;
- target ratio.

Typical outputs:
- 3:4 vertical;
- 16:9 horizontal;
- 1:1 social.

Start with one strong hero KV before expanding a series.

If feedback says:
- **too crowded** → remove elements;
- **too close to reference** → change concept structure;
- **character too small** → enlarge character;
- **unwanted small text** → prohibit all nonessential copy.

## Stage 13 — Merchandise

Use the assets already created.

Possible:
- figure;
- plush;
- badge;
- acrylic stand;
- keychain;
- sticker;
- postcard;
- tote;
- mug;
- phone case;
- blind-box packaging;
- gift box.

Choose a meaningful set rather than a random catalog.

Use different asset types across products.

## Stage 14 — Offline Applications

The user may provide spatial references.

First identify:
- indoor;
- outdoor;
- pop-up;
- market;
- exhibition;
- retail corner.

Then create a coherent set:
- entrance;
- hero backdrop;
- photo spot;
- display unit;
- standee;
- wayfinding;
- packaging / giveaway;
- interactive element.

Keep the character and theme recognizable.

## Stage 15 — Final Review / Case Package

Collect approved stages.

Review with:
- Keep;
- Improve;
- Extend;
- Reuse.

The final case should show the creative journey, not only final renders.

## Resume rule

When the user says "next", "continue", or provides a new reference:

1. read current project state;
2. identify the current stage;
3. apply the new reference only where relevant;
4. continue from the latest approved result.

Do not reset the project.
