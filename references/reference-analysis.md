# Reference Analysis

References are a major input to this Skill.

The purpose of analysis is not to weaken the reference.
The purpose is to understand **what the user wants from it** so the Agent can combine references without visual conflict or accidental copying.

## Reference Map

For every important reference, record:

```text
Reference ID:
Role:
Use / Learn:
Do not inherit:
Priority:
Used in stage:
```

## Common roles

- character silhouette
- face / expression
- eye language
- body proportion
- material / rendering
- pose / camera
- outfit
- palette
- logo
- typography
- poster composition
- graphic language
- merchandise
- packaging
- offline space
- atmosphere

A reference may have several roles when the user's intent clearly requires it.

## Strong reference use is allowed

If the user says:
- "use this face";
- "follow this outfit";
- "use this composition";
- "use this material";
- "use this font feeling";

treat that instruction as high priority.

Still isolate the intended variable instead of importing unrelated content.

Example:

```text
REF-03
Role: outfit
Use / Learn:
- short cape silhouette
- red / cream layering
- oversized bow
Do not inherit:
- model face
- human body proportion
- photography background
Priority: high
Used in stage: outfit
```

## Multiple references

Do not automatically feed every available reference into each generation.

Prefer:
1. latest approved character anchor;
2. current task reference;
3. optional style / material reference.

Add more only when they solve a specific problem.

## Conflict rule

If references conflict:
- obey explicit user priority;
- otherwise use the most stage-relevant reference;
- preserve approved character identity;
- do not silently blend incompatible instructions.

## Translation by task

### Character
Extract silhouette, face, proportion and costume logic.

### Outfit
Extract silhouette, layering, palette, material and key accessory.

### Logo / typography
Extract weight, roundness, curvature, rhythm, spacing and symbol integration.

### Poster
Extract hierarchy, grid, negative space, character scale, density and title relationship.

### Merchandise
Extract product type, graphic scale, placement and finish.

### Offline
Extract zoning, focal installation, circulation, scale and material mood.

## Reference lock-in rule

A new reference should influence the requested stage, not rewrite every earlier approval.

Once the user approves a character, that character becomes the primary anchor for later outputs.
