# Character Consistency

The goal is to keep a recurring character on-model with the least intervention necessary.

## Consistency ladder

Use the lightest fix that can solve the issue:

1. short corrective rule;
2. approved master reference;
3. small reference atlas;
4. structured dataset / routing;
5. post-process or training.

Do not jump to heavy workflows before simpler fixes fail.

## Delta-only principle

When editing or generating from an approved reference, describe what changes.

Bad:
- re-describe the whole character and style in every prompt.

Better:
- "keep Character Master v1 unchanged; change only expression to embarrassed and raise left paw."

Long duplicate prompts can fight the reference and introduce drift.

## Closest-reference selection

Choose the reference closest to the requested target:
- face close-up for expression;
- side view for side pose;
- outfit-approved frame for outfit continuation;
- hero 3/4 for campaign pose.

## Identity QA

Check:
- head silhouette;
- head/body ratio;
- facial feature placement;
- eye spacing/shape;
- eyebrow language;
- mouth/nose language;
- ear position;
- signature colors;
- primary symbol;
- prop scale;
- material;
- costume construction.

Track historically unstable traits first.

## Drift recovery

Fix in this order:
1. remove irrelevant prompt text;
2. tighten one corrective rule;
3. swap to a better reference;
4. clean or replace a dirty reference;
5. use a stronger edit/reference workflow;
6. only then consider training.

Never solve every problem by adding more adjectives.
