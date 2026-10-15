# Prompt Record

**Asset ID:** JSG-EXP-004  
**Stage:** 07_expressions  
**Version:** v1.0  
**Status:** planned

## Goal

Create the final expression-only sheet for the approved Jellyfish Star Guardian.

## Locked identity

Use the approved 3D hero as the identity anchor:
- transparent jellyfish dome
- warm star inserts
- lavender hair
- blue-violet eyes
- compact Q-version body
- same base blue-violet outfit
- same collectible-toy materials
- same camera distance and studio presentation

## Canonical prompt

```text
Create a strict 3x3 facial-expression sheet of ONE identical 3D collectible-toy jellyfish guardian girl.

LOCK EVERYTHING EXCEPT EXPRESSION:
same transparent blue-violet jellyfish dome;
same 3–5 warm star inserts;
same lavender hair;
same blue-violet eyes;
same face proportions;
same body proportions;
same blue-violet base outfit;
same shoes;
same materials;
same camera distance;
same character scale;
same simple studio background;
same lighting.

ONLY CHANGE:
eyebrows;
eye openness;
mouth shape;
blush;
very small head tilt;
very small hand gesture close to torso.

EXPRESSIONS:
1 happy hello
2 laughing
3 teary sad
4 tiny angry pout
5 surprised
6 shy / affectionate
7 sleepy
8 proud / pleased
9 curious / confused

BACKGROUND:
one simple low-detail blue-violet studio field;
no scene props;
no environment storytelling;
no decorative objects.

OUTPUT:
3:4 board;
3x3 grid;
no text;
high-consistency 3D collectible-toy product render.
```

## Negative / Do not

- no outfit changes
- no props
- no hats
- no umbrellas
- no shell throne
- no moon
- no coral
- no scenery
- no new accessories
- no different camera angles
- no text
- no 2D illustration

## Repair rule

If the image model introduces outfit or scene variation, reject the result and regenerate with all non-expression variables explicitly locked.

## Learning

Expression-sheet success depends on preventing secondary variables from changing. The Skill must separate "expression" from "outfit", "pose", and "scene".
