# Prompt Record

**Asset ID:** JSG-EXP-002  
**Stage:** 07_expressions  
**Version:** v0.2  
**Status:** planned

## Goal

Repair the failed expression-sheet test. The previous generation changed outfits, props and backgrounds. This version must vary **expression only**.

## Locked identity

Use JSG-3D-HERO-001 exactly:
- same transparent jellyfish dome
- same star placement logic
- same lavender hair
- same blue-violet eyes
- same face proportions
- same body proportions
- same blue-violet base outfit
- same materials
- same camera distance
- same lighting
- same plain studio background family

## Canonical prompt

```text
Create a 3x3 facial-expression reference sheet of ONE identical 3D collectible-toy character.

CRITICAL RULE:
This is NOT an outfit sheet, NOT a pose series, NOT a scene series.

Use the exact same jellyfish guardian girl in every cell:
same transparent jellyfish dome;
same 3–5 warm star inserts;
same lavender hair;
same blue-violet eyes;
same face proportions;
same Q-version body;
same blue-violet base dress;
same shoes;
same materials;
same character scale;
same camera angle;
same simple pale blue-violet studio background.

DO NOT ADD ANY PROP.
DO NOT CHANGE OUTFIT.
DO NOT CHANGE BACKGROUND.
DO NOT ADD SCENERY.
DO NOT ADD ACCESSORIES.

Only change:
- eyebrows
- eye openness
- mouth shape
- blush
- tiny head tilt
- tiny hand gesture close to torso

Nine expressions:
1 cheerful hello
2 laughing
3 teary sad
4 tiny angry pout
5 surprised
6 affectionate heart-hands
7 sleepy
8 proud / pleased
9 curious / confused

Composition:
3x3 grid on one 3:4 board;
same crop and same character scale in every cell;
clean equal spacing;
neutral pale blue-violet studio field;
no text.

Rendering:
real collectible-toy product render;
matte painted PVC face/body/hair;
clear resin / transparent PVC jellyfish dome;
soft studio lighting.
```

## Negative / Do not

- no outfit variation
- no hats
- no umbrellas
- no lantern
- no shells
- no coral
- no moon
- no clouds
- no scenery
- no new props
- no alternate costumes
- no different camera angles
- no 2D illustration
- no text

## Repair notes

The failure mode to prevent is "expression sheet becomes themed outfit series".
If the model tries to vary clothing or props, remove them completely and keep only face + micro gesture.

## Learnings

When generating expression grids, positive wording about themes or scenes can overpower expression-only constraints. Use repeated identity locks and explicitly forbid all secondary design variables.
