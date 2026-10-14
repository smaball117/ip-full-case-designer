# Visual Stage Prompt Patterns v0.4

These are **compact execution patterns**, not giant prompts.

Every generated image must also create a matching prompt record using `templates/prompt-record.md`.
The prompt record is part of the deliverable and should be reusable by another AI.

The Skill should build prompts from:
- approved character anchor;
- current task;
- current reference role;
- only the variables that are allowed to change.

Do not repeat the full IP brief unless the image model needs it.

---

# 1. Character Sketch

```text
TASK:
Create [N] character sketch directions for [IP name].

LOCK:
- selected concept
- species / identity
- signature symbol
- personality direction

REFERENCE USE:
- learn [head shape / face / proportion / costume logic] from REF-[ID]
- do not inherit [unrelated species / colors / props / background]

EXPLORE:
- head silhouette
- face / eyes
- body proportion
- costume silhouette
- prop relationship

OUTPUT:
[N] clearly different sketch directions on a clean sheet.
Do not render as final 3D.
```

---

# 2. Character Final / 3D

```text
LOCK CHARACTER:
Use approved sketch [asset ID].

CHANGE ONLY:
- refine [face / proportion / costume / prop]
- apply material from REF-[ID]

PRESERVE:
- identity
- silhouette
- signature symbol
- approved colors
- accessory scale

OUTPUT:
single hero character render, clean background, requested ratio.
```

---

# 3. Turnaround

```text
LOCK CHARACTER:
Use approved Character Final [asset ID].

OUTPUT:
front / side / back [plus optional 3/4].

PRESERVE:
same face, proportions, costume, material, prop scale.

DO NOT:
redesign hidden areas casually;
change facial identity between views;
change accessory count.
```

---

# 4. Expression Sheet

```text
LOCK CHARACTER:
Use [asset ID].

CHANGE ONLY:
expression + small head/body gesture.

EXPRESSIONS:
[list 6 or 9]

PRESERVE:
face construction, eye design, costume, colors, proportions.

OUTPUT:
clean grid, no labels unless requested.
```

---

# 5. Action Sheet

```text
LOCK CHARACTER:
Use [asset ID].

ACTIONS:
[list actions based on personality / story]

PRESERVE:
character identity and costume.

REFERENCE USE:
REF-[ID] controls pose only.

OUTPUT:
clean grid, readable silhouettes, no text unless requested.
```

---

# 6. Outfit Sheet

```text
LOCK CHARACTER:
Use approved Character Final [asset ID].

REFERENCE USE:
REF-[ID] controls:
- outfit silhouette
- layering
- palette
- material cue
- 1–2 key accessories

DO NOT INHERIT:
reference model face, anatomy, pose, photography background.

TRANSLATE:
simplify outfit into the character's proportions and shape language.

OUTPUT:
[N]-look outfit grid.
```

---

# 7. 2D Flat Character

```text
LOCK CHARACTER:
Use [3D asset ID] as identity anchor.

REFERENCE USE:
REF-[ID] controls flat graphic treatment only.

PRESERVE:
face identity, proportions, colors, costume, signature symbol.

CHANGE:
rendering language only.

OUTPUT:
flat illustration, clean outline/fill rules, no extra text.
```

---

# 8. Logo / Typography

```text
BRAND:
[IP name / wordmark text]

REFERENCE USE:
REF-[ID] controls:
- weight
- roundness
- curvature
- rhythm
- symbol integration

DO NOT COPY:
exact glyphs, wording, source-brand symbols.

USE:
approved IP symbols: [apple / star / cat ear / etc.]

OUTPUT:
[Chinese / English / combo] logo route.
No random small text.
```

---

# 9. Poster / KV

```text
THEME:
[theme]

LOCK CHARACTER:
[2D or 3D asset ID]

REFERENCE USE:
REF-[ID] controls:
- composition / typography / density / color rhythm
[choose only what matters]

PRESERVE:
IP identity, current palette, logo.

HIERARCHY:
1. title
2. character
3. one core story symbol
4. minimal support elements

TEXT:
allow only [exact text].
No microcopy unless explicitly requested.

OUTPUT:
[ratio].
```

### Poster repair shortcuts

**Too crowded**
```text
Reduce supporting elements by 40–60%.
Keep one hero character + one core symbol.
Increase negative space.
Do not add replacement decoration.
```

**Too close to reference**
```text
Keep only the reference's hierarchy principle.
Change scene concept, prop system and spatial structure.
Build the scene from the current IP theme.
```

**Character too small**
```text
Increase character scale to become the dominant visual.
Remove competing background objects.
```

**No small text**
```text
Only render the approved title / logo.
No captions, labels, dates, signatures, filler English or decorative microcopy.
```

---

# 10. Merchandise Board

```text
LOCK IP:
use approved Character Final + 2D assets + logo.

PRODUCT SET:
[list 4–8 products]

ASSET ROUTING:
- figure → 3D character
- plush → simplified silhouette
- badge / sticker → face / icon
- tote / pouch → 2D art / pattern
- packaging → character + logo + theme graphics

REFERENCE USE:
REF-[ID] controls product presentation / material / layout only.

RULE:
Do not paste the same full-body character on every item.

OUTPUT:
clean merchandise presentation board.
```

---

# 11. Offline Application

```text
LOCK IP:
use approved character + logo + current theme.

CONTEXT:
[indoor / outdoor / pop-up / market / exhibition]

REFERENCE USE:
REF-[ID] controls:
- spatial zoning
- material mood
- display scale
- circulation

IP TRANSLATION:
turn the theme into:
- entrance
- hero installation
- photo spot
- display
- wayfinding
- interaction

DO NOT:
paste character stickers onto a generic booth.

OUTPUT:
coherent spatial concept visualization.
```

---

# 12. Prompt compression rule

Before generation, remove:
- duplicated constraints;
- repeated adjectives;
- old decisions already visible in the approved reference;
- irrelevant negative prompts.

Prefer:

```text
LOCK
CHANGE
REFERENCE USE
OUTPUT
DO NOT
```

over long prose.


---

# 13. Mandatory prompt-record output

After generating any visual, save or return:

```text
ASSET ID
STAGE
VERSION
GOAL
LOCK
REFERENCE USE
CHANGE
CANONICAL PROMPT
NEGATIVE / DO NOT
OUTPUT
REPAIR NOTES
LEARNINGS
```

For outfit / themed-series generation, also read:
`docs/SERIES_OUTFIT_BACKGROUND_RULES.md`.

For project-wide reproducibility, read:
`docs/REPRODUCIBLE_GENERATION_PROTOCOL.md`.
