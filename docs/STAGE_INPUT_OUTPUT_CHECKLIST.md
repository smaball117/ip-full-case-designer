# Stage Input / Output Checklist v0.3

This checklist tells the Agent what it needs at each stage and what it should produce.

The user does **not** need to provide every input in advance.
Use what already exists, ask only for blockers, and continue from the current project state.

| Stage | Minimum input | Optional references | Required output | Approval / next |
|---|---|---|---|---|
| 00 Project Setup | project idea or existing project | none | project state + folder target | continue |
| 01 Idea + Reference Intake | idea, likes/dislikes, current refs | any visual refs | reference map + light brief | continue |
| 02 Creative Directions | Stage 01 summary | character/style refs | 5 genuinely different directions | Gate A |
| 03 IP Setting | selected direction | story / audience refs | editable IP setting sheet | continue |
| 04 Character Sketch | IP setting | form / face / proportion refs | 5 sketch explorations | Gate B |
| 05 Character Final / 3D | selected sketch | material / color refs | hero character + corrected final | Gate C |
| 06 Turnaround | approved character | construction refs if needed | front / side / back / optional 3/4 | continue |
| 07 Expressions | approved character + personality | expression refs | 6 or 9-expression sheet | continue |
| 08 Actions | approved character + recurring behaviors | pose refs | action sheet | continue |
| 09 Outfits | approved character | clothing refs | outfit sheet / seasonal set | continue |
| 10 2D Assets | approved character | flat-style refs | full body / half body / avatar / line / sticker | continue |
| 11 Logo / Typography | IP name | logo / font refs | Chinese / English / combo / simplified variants | continue |
| 12 Posters / KV | theme + approved character | poster / type / layout refs | hero KV + requested ratios | iterate |
| 13 Merchandise | approved assets | product refs | focused product family | iterate |
| 14 Offline | theme + approved assets | space / event refs | coherent offline touchpoint family | iterate |
| 15 Review | approved project outputs | none | Keep / Improve / Extend / Reuse + case package | complete |

## Stage execution rule

Before every visual stage, the Agent should silently resolve:

```text
1. What is already approved?
2. What is allowed to change?
3. Which reference is relevant now?
4. What should NOT be inherited from that reference?
5. What is the exact output format?
```

Then generate.

## User feedback rule

Treat short visual feedback as a valid design instruction.

Examples:

- "眼睛大一点" → change eyes only unless another issue is named.
- "道具太大" → reduce prop scale, preserve character.
- "太拥挤" → reduce supporting elements and increase negative space.
- "太像参考" → rebuild theme/composition structure.
- "不要小字" → remove all nonessential copy.
- "这个版本可以" → use it as the new downstream anchor.

Do not force the user to rewrite a full brief after every correction.

## Reference rule

Reference priority for downstream production:

```text
latest approved character anchor
> explicit current-task reference
> older style reference
> general inspiration
```

If the user explicitly sets another priority, follow the user.

## Output rule

When the user requests an image and image generation is available:

**create the image.**

Do not stop at:
- analysis only;
- prompt only;
- "here is what I would do".

Prompt text may be stored internally or returned when the user explicitly asks for it.
