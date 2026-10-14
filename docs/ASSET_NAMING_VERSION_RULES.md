# Asset Naming & Version Rules v0.3

The goal is simple:
make it obvious what an asset is, which stage it belongs to, and whether it is safe to reuse.

---

# 1. Asset ID format

Use:

```text
[PROJECT]-[STAGE]-[TYPE]-[NNN]
```

Example:

```text
CC-3D-HERO-001
CC-EXP-GRID-001
CC-OUT-AUTUMN-001
CC-LOGO-COMBO-001
CC-POST-WISHCHECKIN-001
CC-MERCH-SET-001
```

For compact projects, stage abbreviations may be shortened.

Recommended Coco prefixes:

- `CC-SKETCH`
- `CC-3D`
- `CC-TURN`
- `CC-EXP`
- `CC-ACT`
- `CC-OUT`
- `CC-2D`
- `CC-LOGO`
- `CC-POST`
- `CC-MERCH`
- `CC-OFFLINE`

---

# 2. File name format

Use:

```text
[asset-id]_[short-name]_v[major.minor].[ext]
```

Example:

```text
CC-EXP-GRID-001_nine-expressions_v1.0.png
CC-POST-WISHCHECKIN-001_vertical-3x4_v1.2.png
```

Keep names short and descriptive.

Do not use:
- final-final;
- new2;
- latest;
- good-one;
- random timestamps as the only identifier.

---

# 3. Version meaning

## v0.x
Exploration / not approved.

Examples:
- v0.1 first attempt
- v0.2 corrected eyes
- v0.3 smaller props

## v1.0
First approved version safe for downstream use.

## v1.x
Minor visual correction that does not change identity.

Examples:
- lighting cleanup
- spacing
- text placement
- color correction

## v2.0
Meaningful redesign.

Examples:
- new face construction
- new costume system
- new logo architecture
- changed silhouette

A v2.0 change should not silently overwrite v1.0.

---

# 4. Status values

Use only:

- `draft`
- `candidate`
- `revise`
- `approved`
- `rejected`
- `superseded`
- `locked`

### Meaning

**draft**  
first exploration.

**candidate**  
good enough for review, not yet selected.

**revise**  
selected direction but still needs correction.

**approved**  
safe to use downstream.

**rejected**  
do not reuse.

**superseded**  
was approved before, replaced by a newer approved asset.

**locked**  
identity-critical asset that must not drift without explicit redesign.

---

# 5. Source tracking

Every asset should record:

- source asset IDs;
- reference IDs;
- generation / edit round;
- short note describing the change.

Example:

```text
asset_id: CC-OUT-AUTUMN-001
source_assets: CC-3D-HERO-001
reference_ids: REF-OUT-03, REF-OUT-04
note: "Autumn 9-look set; translated knit / detective / rainwear / harvest references into Coco proportions."
```

---

# 6. Reuse rule

Only reuse downstream assets with status:

- approved
- locked

Candidate assets may be used only when:
- the user clearly treats them as the current working direction;
- the downstream output is exploratory.

Rejected assets must never become hidden references later.

---

# 7. Superseding rule

When the user says:
- "用这张作为新的标准"
- "这个版本就定了"
- "以后都按这个"

then:

1. mark the new asset `approved` or `locked`;
2. mark the old anchor `superseded`;
3. update `project_state.yaml`;
4. keep both in the manifest for history.

Do not delete the old record.

---

# 8. Reference IDs

Use:

```text
REF-[CATEGORY]-[NNN]
```

Examples:

- REF-FACE-001
- REF-MAT-001
- REF-OUTFIT-004
- REF-LOGO-002
- REF-POSTER-003
- REF-MERCH-001
- REF-OFFLINE-002

References may be superseded too.

---

# 9. Minimal asset manifest fields

Required columns:

```text
asset_id
stage
type
version
status
location_type
path_or_ref
source_assets
reference_ids
notes
```

This is enough for the Agent to know:
- what exists;
- what is approved;
- what it came from;
- whether it is safe to continue from.
