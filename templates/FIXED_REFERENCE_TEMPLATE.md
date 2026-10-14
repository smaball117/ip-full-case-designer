# Fixed Reference & Output Template v0.4

This file defines the **default fixed template** for ip-full-case-designer.

It is based on the user's proven working method: the user feeds ideas and reference images stage by stage, and the Agent turns them into a complete IP case.

The template is fixed in **structure**, not in visual content.

That means:
- every new IP project follows the same reference slots and output sequence by default;
- the actual images, character, colors, clothing, logo style and poster style can change for each project;
- the user may add references gradually instead of uploading everything at once.

---

# A. Fixed Reference Pack

## REF-01 — Core Character / Overall Style
Purpose: overall character direction, silhouette feeling, cuteness / trend / collectible-toy balance, general design language.
Use for: creative directions, sketch exploration, character final.
Do not automatically inherit: original character identity, original costume, original logo, unrelated props.

## REF-02 — Face / Eyes / Expression
Purpose: face structure, eye size and language, pupil/highlight treatment, eyebrow / mouth expression, species readability.
Use for: sketch correction, character final, expressions.
Priority: high once the user explicitly says this is the face direction.

## REF-03 — Body Proportion / Silhouette
Purpose: head/body ratio, limb length, ear / tail proportion, body compactness, silhouette readability.
Use for: sketch, 3D, turnaround, plush translation.

## REF-04 — 3D Material / Rendering
Purpose: flocked / vinyl / resin / plush / clay / other material, surface finish, lighting, collectible-toy presentation.
Use for: 3D hero, figure, product visualization.

## REF-05 — Color Palette
Purpose: identity color, base color, support colors, accent colors.
Use for: character, 2D assets, logo, poster, merchandise, offline.
Record actual colors when the user provides them.

## REF-06 — Outfit / Clothing
Purpose: silhouette, layering, palette, material cue, key accessories.
Use for: outfit grid, seasonal outfit set, themed outfit set.
Important: this slot can contain many references. The user may add them later.
Do not inherit: reference model face, human anatomy, photography background.

## REF-07 — Flat Illustration / Graphic Style
Purpose: outline, fill, simplification, graphic texture, flat-vs-3D translation.
Use for: 2D character assets, sticker, icon, poster illustration.

## REF-08 — Logo / Typography
Purpose: font weight, roundness, rhythm, baseline, curvature, icon integration.
Use for: Chinese logo, English logo, combo lockup, campaign title style.
Do not copy exact proprietary glyphs or source-brand wording.

## REF-09 — Poster / KV
Purpose: hierarchy, composition, title scale, character scale, negative space, graphic density, commercial mood.
Use for: 3:4 vertical KV, 16:9 horizontal KV, optional 1:1 social version.
Important: do not copy all scene elements. If the reference is crowded, extract only the useful hierarchy / layout logic.

## REF-10 — Merchandise
Purpose: product selection, product styling, material finish, placement, presentation-board layout.
Use for: figure, plush, acrylic, badge, keychain, sticker, tote / pouch, blind-box / gift packaging.

## REF-11 — Offline / Indoor
Purpose: pop-up / exhibition / retail corner, entrance, backdrop, photo spot, display, interaction, indoor materials.

## REF-12 — Offline / Outdoor
Purpose: outdoor activation, market / fair, large installation, wayfinding, outdoor display, photo interaction.

---

# B. Fixed Output Sequence

Unless the user explicitly asks to skip or reorder a stage, use this sequence.

## 01 — Five Creative Directions
Input: user's idea + REF-01 to REF-05 if available.
Output: 5 concept directions.
Each direction includes: name, core concept, character mood, story/worldview hook, visual emphasis, commercial potential, risk.
Then the user chooses one or combines up to two.

## 02 — IP Setting Checklist
Output: name, Chinese/English name, identity, personality, flaw, likes/dislikes, world premise, one-line story, signature symbol, palette, audience, applications, Must Keep, Must Avoid.

## 03 — Five Line-Sketch Directions
Input: selected concept + REF-01 / REF-02 / REF-03.
Output: 5 sketches of the same IP concept.
Explore: head, eyes, ears/hair, body ratio, costume, symbol, prop.
User chooses one.

## 04 — Character Final / 3D Hero
Input: selected sketch + REF-04 material + REF-05 palette.
Output: one approved hero character. This becomes the primary character anchor.

## 05 — Turnaround
Output: front, side, back, optional 3/4 hero. Same character, same costume, same proportions.

## 06 — Expression Grid
Default: 3x3 / 9 expressions.
Suggested: greeting, laugh, cry, angry, surprised, affection, sleepy, approval, confused.
No text unless requested.

## 07 — Outfit Grid
Input: approved character + REF-06 outfit references.
Default: 3x3 / 9 looks.
Translate clothing into the IP's own body proportion and shape language.

## 08 — 2D Flat Character Assets
Input: approved 3D character + REF-07.
Output set: flat full body, half body, avatar, line art, monochrome, sticker/icon, optional signature symbols.

## 09 — Logo / Typography
Input: IP name + REF-08.
Output: Chinese logo, English logo, combination, color, monochrome, simplified mark when useful.
No random microcopy.

## 10 — Poster / KV
Input: current theme + 2D/3D character + logo + REF-09.
Default outputs: 3:4 vertical and 16:9 horizontal. Optional 1:1 social.
Rules: character stays prominent, hierarchy before decoration, no unwanted small text, redesign theme/scene structure if too close to reference.

## 11 — Merchandise Family
Input: approved character + 2D assets + logo + REF-10.
Default first family: collectible figure, plush, acrylic stand, badge/pin, keychain, sticker sheet, tote/pouch, blind-box/gift packaging.
Do not use the same full-body image on every product.

## 12 — Offline Applications
Input: current IP theme + approved visual assets + REF-11 and/or REF-12.
Default outputs: entrance, hero backdrop/installation, photo spot, display, standee, wayfinding, giveaway/packaging, interaction.
Create indoor and outdoor sets when both reference groups are available.

## 13 — Final Review & Archive
Output: Keep, Improve, Extend, Reuse.
Archive approved assets, rejected/superseded assets, reference map, project state, final case order.

---

# C. Fixed Template Rule

The Agent should treat this as the default production spine.

When the user starts a new IP, do not ask them to invent the workflow.
Instead:
1. accept their idea;
2. map incoming references into REF-01 to REF-12;
3. identify which slots are already filled;
4. start from the earliest necessary output stage;
5. let the user keep feeding missing reference slots later;
6. preserve all approved outputs downstream.

The Agent should infer the reference slot from the user's intent when possible.

---

# D. What Is Fixed vs Variable

## Fixed
- reference-slot structure;
- output sequence;
- 5 creative directions;
- 5 sketches;
- character final / 3D;
- turnaround;
- expression grid;
- outfit grid;
- 2D assets;
- logo / typography;
- poster;
- merchandise;
- offline;
- final review.

## Variable
- IP idea;
- species;
- world;
- character shape;
- face;
- material;
- palette;
- clothing;
- logo style;
- poster style;
- product styling;
- spatial styling.

This is why the template is reusable across different IP projects.