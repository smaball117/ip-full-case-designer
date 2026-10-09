# Reference Router

References are optional inputs, not the design engine.

## Modes

### MODE A — Original Design
Default.
No external reference required.
Generate from the active IP system.

### MODE B — Reference Assisted
Use a reference for one or two named variables only.

Examples:
- outfit silhouette
- font rhythm
- material
- camera
- layout density

### MODE C — Adaptation
Use only when the user explicitly wants a close structural adaptation.

## Routing format

```text
REF-01
role: typography rhythm
learn: heavy rounded letters, curved baseline
do not learn: wording, logo icon, exact glyph shapes
```

## Rule

Never pass an undefined "style reference" downstream.

Translate the reference into abstract rules first.
