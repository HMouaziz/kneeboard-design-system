# Skill: Content Normalization

## Goal

Convert raw source content into reusable aircraft content that can be rendered in any style and page format.

## Canonical row model

Use this semantic model mentally or in markdown/json:

```txt
label: short action/object name
value: desired state, setting, or result
note: supporting text
condition: when this row applies
emphasis: normal | muted | critical | warning | caution | optional
tags: dcs-specific | real-world | combat | landing | weapons | reference | crew-role
```

## Row types

### Action row

Use for direct cockpit actions.

```txt
Throttle | Idle/Cutoff
Fuel pump | ON
Gear | DOWN
```

### Condition row

Use for triggers or sequencing.

```txt
When engine catches
Below 160 mph
After touchdown
```

### Note row

Use for explanatory text that should not be mistaken for an action.

```txt
Keep radiator temperature above 60 C.
Target is at set range when wings fit in the sight reticle.
```

### Table row

Use for repeated comparable values.

```txt
Power setting | RPM | boost/ATA | limit | note
```

### Diagram callout

Use for visual procedures or cockpit/control maps.

```txt
diagram: bombing attack profile
labels: climb, throttle idle, diving turn, target
```

## Normalization rules

- Use consistent casing: Title Case for labels, uppercase only when it is an acronym or cockpit label.
- Prefer concise labels: `Fuel Pump`, not `Turn the fuel pump switch`.
- Prefer concise values: `ON`, `OFF`, `DOWN`, `UP`, `SET`, `AS REQ.`.
- Preserve aircraft-specific terms when they matter: `ATA`, `BOOST`, `RPM`, `CAGE/UNCAGE`, `JESTER`, `CIP`, `TADS`, `RWR`.
- Mark optional items as `optional`, not grey or transparent.
- Mark critical irreversible or safety items as `critical` or `warning`.
- Mark simulation shortcuts or DCS-only steps as `dcs-specific`.

## Muted versus optional

Use `muted` for items that are less important in normal DCS use but may still be procedural.

Use `optional` for items that depend on mission, loadout, weather, multiplayer, or realism setting.

## Critical versus warning

Use `critical` for actions the pilot must not miss.

Examples:

- Pull starter clutch when engine kicks in.
- Gear down.
- Hook down before carrier landing.
- Master arm safe on fence out.

Use `warning` for actions that can damage the aircraft or create a dangerous state.

Examples:

- Do not exceed power limit.
- Do not overcool engine.
- Avoid hot start.
