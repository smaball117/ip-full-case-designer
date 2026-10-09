# Prompt Compiler

The user should not have to manually rewrite a long prompt for every asset.

## Inputs

- project state
- Character DNA
- Visual DNA
- Narrative Engine
- selected Theme
- Layout preset
- task-specific delta
- optional reference roles
- output constraints

## Compiler order

```text
1. LOCKED IDENTITY
2. TASK / DELTA
3. THEME / STORY MOMENT
4. VISUAL LANGUAGE
5. LAYOUT
6. TEXT POLICY
7. OUTPUT FORMAT
8. NEGATIVE CONSTRAINTS
```

## Rule

Only include information that can materially change the output.

Do not duplicate the same instruction in multiple sections.

## Compact prompt target

Prefer a short operational prompt over a long manifesto.

If the model already has approved reference images in context, reduce repeated descriptive text further.
