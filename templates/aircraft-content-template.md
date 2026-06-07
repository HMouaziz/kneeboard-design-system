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
    target_style: "ww2-day | ww2-night | cold-war-day | cold-war-night | modern-day | modern-night"
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
Style: WW2 Day
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
