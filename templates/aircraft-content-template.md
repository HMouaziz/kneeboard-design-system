# Aircraft Content Template

Use this template to normalize aircraft content before rendering.

```yaml
aircraft:
  name: ""
  variant: ""
  nickname: ""
  module: "DCS: "
  era: "ww2 | cold-war | modern"
  notes: ""

artifact:
  statement: "This kneeboard should feel like: ..."
  archetype: ""
  treatment: ""
  lighting:
    - "paper-day"
    - "low-glare-night"
  motif_notes:
    - ""

source:
  files:
    - ""
  accuracy_mode: "dcs-practical | real-manual | hybrid"
  source_notes:
    - ""

pages:
  - id: ""
    title: ""
    format: "normal-checklist | combat-fence | weapons-employment | sensors-and-avionics | navigation | carrier-operations | engine-management | emergency | reference-tables | cockpit-controls | mission-data-card"
    design_profile: ""
    lighting: "paper-day | low-glare-night"
    density: "sparse | normal | dense | emergency-card"
    sections:
      - id: ""
        title: ""
        section_type: ""
        rows:
          - type: "action | condition | note | table | diagram"
            label: ""
            value: ""
            note: ""
            condition: ""
            emphasis: "normal | muted | optional | critical | warning | caution"
            tags: []
```

## Markdown shorthand

For quick manual work, this lighter format is acceptable:

```txt
# Fw 190 A-8 / Anton
Era: WW2
Style: WW2 German Day
Artifact: A Luftwaffe technical field form issued with an operational fighter.
Format: Normal Checklist

## Engine Start
- Brakes ............... APPLY
- Starter .............. POWER / PUSH
  note: Power starter for 25 seconds.
- Starter .............. CLUTCH / PULL
  emphasis: critical
  condition: When engine kicks in.
- RPM .................. 1200
```
