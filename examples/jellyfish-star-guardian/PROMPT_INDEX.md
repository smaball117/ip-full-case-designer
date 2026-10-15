# Prompt Index — Jellyfish Star Guardian

This file tells Codex / another Agent where the reusable prompts for this project are stored.

## Character development

- `prompts/JSG-SKETCH-001_v1.prompt.md`
  - selected character concept merge
  - jellyfish dome + outfit + crescent moon lantern

- `prompts/JSG-3D-HERO-001_v1.prompt.md`
  - main 3D collectible-toy prompt
  - real-world material mapping
  - primary visual anchor

- `prompts/JSG-TURN-001_v0.8.prompt.md`
  - turnaround / multi-view prompt

## Expression development

- `prompts/JSG-EXP-001_v0.1.prompt.md`
  - first expression attempt
  - rejected because it drifted into outfit / scene variation

- `prompts/JSG-EXP-002_v0.2.prompt.md`
  - strict expression-only repair

- `prompts/JSG-EXP-003_v0.3.prompt.md`
  - preserves the preferred visual style of the earlier grid while trying to keep the task structurally correct

## Outfit development

- `prompts/JSG-OUT-001_v0.1.prompt.md`
  - first outfit-grid attempt
  - rejected because looks were too similar and backgrounds were too complex

- `prompts/JSG-OUT-002_v0.2.prompt.md`
  - improved outfit-grid method
  - outfit variation in 2–3 dimensions
  - background element categories <= 3

## Current prompt priority

For future generation, use:

1. `JSG-3D-HERO-001_v1.prompt.md` as character identity anchor
2. `character_dna.yaml` as locked character rules
3. `world_setting.md` as story/world context
4. stage-specific prompt record for the requested task
5. latest user-approved visual as the strongest visual reference

Do not use rejected prompts as final instructions.
Use them only for failure-analysis / repair learning.


## 2D flat asset development

- `prompts/JSG-2D-001_v0.1.prompt.md`
  - translates the approved 3D character into a simplified flat illustration system
  - intended for stickers, badges, packaging, posters and graphic support assets
