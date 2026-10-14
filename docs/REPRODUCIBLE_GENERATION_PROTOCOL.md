# Reproducible Generation Protocol v0.4

> Every visual output must be accompanied by a reusable prompt package.
> The Skill is not finished when it only produces an image.

The goal is that:
- the user can understand how the image was made;
- the same design logic can be reused later;
- another AI can continue from the same stage;
- prompt knowledge becomes part of the project asset, not hidden inside one conversation.

---

# 1. Mandatory dual output

For every image-generation stage, return and/or save **both**:

1. **Visual Asset**
2. **Prompt Record**

A visual asset without a prompt record is considered incomplete.

This applies to:
- sketch
- 3D character final
- turnaround
- expressions
- actions
- outfits
- 2D flat assets
- logo / typography
- poster / KV
- merchandise
- offline applications

---

# 2. Prompt Record structure

Every prompt record should contain:

```text
ASSET ID:
STAGE:
VERSION:
STATUS:

GOAL:
What this image is supposed to achieve.

LOCK:
What must stay unchanged.

REFERENCE USE:
Which reference controls which variable.

CHANGE / EXPLORE:
What is allowed to change.

CANONICAL PROMPT:
The reusable generation prompt.

NEGATIVE / DO NOT:
The critical exclusions.

OUTPUT:
Ratio, grid, number of variants, background type, text policy.

REPAIR NOTES:
What to change if the first result fails.

LEARNINGS:
What this round taught the Skill.
```

Do not save chain-of-thought or hidden reasoning.
Save only operational design instructions and visible decision logic.

---

# 3. Canonical prompt rule

Before generating an image, the Agent should first compose a **canonical prompt**.

The canonical prompt is the source of truth for that asset.

It should be:
- compact;
- explicit;
- reusable;
- model-agnostic where possible;
- free of duplicate instructions.

Preferred structure:

```text
[SUBJECT / TASK]
[LOCKED CHARACTER]
[REFERENCE TRANSLATION]
[DESIGN CHANGES]
[MATERIAL / RENDERING]
[COMPOSITION / BACKGROUND]
[OUTPUT FORMAT]
[DO NOT]
```

---

# 4. Prompt should describe design logic, not only adjectives

Weak:

```text
cute, dreamy, premium, pretty, ocean, magical
```

Better:

```text
Q-version collectible-toy girl with a large transparent jellyfish dome;
three warm stars suspended inside the dome;
short compact body;
blue-violet palette;
realistic cast-resin / transparent PVC material;
clean commercial product-photography lighting;
one large soft background shape + one low-contrast prop only.
```

The reusable prompt should explain **what creates the look**.

---

# 5. Reference translation must be visible

If the user provides references, the prompt record should explicitly say what is learned.

Example:

```text
REF-OUTFIT-03
learn:
- short cape silhouette
- large collar
- yellow rain boots

do not inherit:
- original character face
- human anatomy
- original background
```

This prevents the next AI from treating the whole reference as a style-copy command.

---

# 6. Image + prompt delivery format

When returning an image to the user, also provide a concise prompt block.

Recommended user-facing format:

```text
【这张图的核心提示词】
...

【本轮锁定】
...

【本轮变化】
...

【如果继续修改】
...
```

If the user only wants the image, the prompt may be stored in the project files without forcing a long message.
But the Skill should still preserve it.

---

# 7. Project storage

Recommended structure:

```text
13_posters/
├── CC-POST-001_v1.0.png
└── prompts/
    └── CC-POST-001_v1.0.md
```

or:

```text
10_outfits/
├── IP-OUT-001_v1.0.png
└── IP-OUT-001_v1.0.prompt.md
```

Each image should have a matching prompt record.

---

# 8. Prompt versioning

Prompt versions follow the visual asset version.

Example:

```text
IP-OUT-001_v0.1.png
IP-OUT-001_v0.1.prompt.md

IP-OUT-001_v0.2.png
IP-OUT-001_v0.2.prompt.md
```

Do not overwrite the old prompt when the visual changes meaningfully.

---

# 9. Repair prompts

When the user gives visual feedback, save the repair delta separately.

Example:

```text
REPAIR DELTA:
- reduce background objects from 7 to max 3 categories
- lower background contrast
- keep the character scale unchanged
- preserve outfit and face
```

The next prompt should combine:
- last approved prompt
- repair delta

Do not rewrite the entire project from zero.

---

# 10. Prompt knowledge becomes Skill knowledge

When a repair repeatedly improves results, promote it from project-specific notes into the Skill.

Examples:
- "no small text"
- "background element categories <= 3"
- "props remain smaller than the head"
- "outfit grid must vary silhouette, not only color"
- "real-world manufacturable materials only"

This is how the Skill improves from real projects.

---

# 11. Cross-AI portability

Prompt records should avoid unnecessary tool-specific syntax.

Preferred:
- descriptive language;
- clear locks;
- explicit ratios;
- reference roles;
- negative constraints.

Optional tool-specific notes can be stored under:

```text
TOOL NOTES:
- Midjourney:
- GPT Image:
- Gemini:
- Seedream:
- other:
```

But the canonical prompt should remain readable by any capable image model.

---

# 12. Completion rule

A visual stage is complete only when:

- image exists;
- asset ID exists;
- status exists;
- canonical prompt exists;
- references are recorded;
- major repair learnings are recorded.

**Image-only output is not a complete Skill output.**
