# Kneeboard Generation Harness

## Purpose

Use this harness whenever creating or revising an aircraft kneeboard from existing source material.

The output should usually be:

```txt
1. normalized aircraft content
2. page plan
3. HTML kneeboard page(s)
4. PNG render(s)
5. QA notes
```

This harness does not assume a specific aircraft era or style.

## Inputs

Required:

- Aircraft name and variant.
- Source material: image, PDF, existing kneeboard, manual excerpt, or notes.
- Target style: one of the style design docs.
- Artifact statement: what physical or operational document should this feel
  like?
- Design profile: document archetype, aircraft treatment, and lighting profile.
- Target format or set of formats: one or more format design docs.

Optional:

- DCS module name.
- Day/night target.
- Whether paired day/night outputs are required.
- Desired page count.
- Desired density: sparse, normal, dense, emergency-card.
- Known user preferences.
- Accuracy priority: real manual, DCS practical, or hybrid.

## Output contract

The final HTML/PNG should obey these rules:

- Each page has a clear aircraft header.
- Each page has a clear page family or page title.
- Section headers are visually obvious.
- Action rows have consistent leader lines or alignment.
- Values are right-aligned where possible.
- Notes are visibly different from action rows.
- Critical items are semantically marked and visually emphasized by the selected style.
- Optional items are visibly muted.
- Page numbering is present unless the style guide says otherwise.
- No style-specific decisions are embedded in content data.
- Paired day/night outputs use the same content, section order, and page breaks
  unless readability requires a documented exception.

## Workflow

### 1. Intake the source

Use `skills/01-source-intake.md`.

Capture:

- Aircraft and variant.
- Page names.
- Section names.
- Repeated section families.
- Special visual elements: tables, diagrams, cockpit maps, station diagrams, radar pages, weapons charts.
- Any source-specific quirks.

### 2. Normalize the content

Use `skills/02-content-normalization.md`.

Convert the source into semantic rows:

```txt
label | value | note | condition | emphasis | tags
```

Do not preserve bad visual layout unless it contains operational meaning.

### 3. Select formats

Use `skills/03-format-selection.md`.

Pick page formats based on the content type, not based on source page count.

Common mappings:

- Start, taxi, takeoff, landing, shutdown -> `normal-checklist`
- Master arm, lights, countermeasures, stores, post-attack -> `combat-fence`
- Guns, missiles, rockets, bombs, delivery profiles -> `weapons-employment`
- Radar, datalink, TGP, RWR, IHADSS, TADS/PNVS -> `sensors-and-avionics`
- TACAN, INS, radios, waypoints, datacard -> `navigation`
- Case I/II/III, traps, catapult, marshal -> `carrier-operations`
- Power tables, RPM, boost, temperatures, limits -> `engine-management`
- Fire, flameout, hydraulic, gear failure -> `emergency`
- Tables, abbreviations, threats, symbols -> `reference-tables`
- Switch maps, HOTAS, cockpit locations -> `cockpit-controls`
- Frequencies, loadout, bullseye, TOT, package data -> `mission-data-card`

### 4. Plan pages and density

Use `skills/04-pagination-and-density.md`.

Page count should be driven by cockpit use:

- A normal checklist may be 1-2 pages.
- Weapons pages may be 1 page for WW2, 2-5 pages for Cold War/modern.
- Reference material may be split into several focused cards.
- Do not make a page dense just to avoid an extra PNG.

### 5. Select the document identity

Use `skills/05-design-composition.md` and `styles/README.md`.

Write one sentence:

```txt
This kneeboard should feel like:
________________________________
```

Then select:

- a document archetype from `styles/archetypes/`
- an aircraft treatment from `styles/treatments/`
- day/night behavior from `styles/lighting/`

Record the composition in an aircraft profile. Do not invent a new archetype
when the distinction is limited to colors, insignia, or typography.

### 6. Render to HTML

Use `skills/06-html-rendering.md` and the selected design profile.

HTML should use semantic classes from `templates/html-class-contract.css`.

### 7. QA review

Use `skills/07-qa-review.md`.

Review for:

- Procedure order.
- Missing critical actions.
- Visual hierarchy.
- Readability at kneeboard size.
- Day/night suitability.
- Section type correctness.
- Whether source quirks have been accidentally copied.
- Whether the page still resembles the selected physical artifact.

### 8. Package and publish

Use `publishing/README.md` and create a pack manifest from
`templates/pack-manifest-template.yaml`.

Full generated packs belong in ignored `output/`, GitHub Releases, or DCS User
Files. Commit only representative examples and source-safe documentation to the
design-system repository.

## Source observations from the sample batch

The expanded sample set suggests these format families are necessary:

- WW2 piston aircraft benefit from `normal-checklist`, `engine-management`, and compact `weapons-employment` pages.
- Cold War jets need `normal-checklist`, `combat-fence`, `weapons-employment`, `navigation`, and sometimes `sensors-and-avionics`.
- Carrier aircraft such as the F-14 need a dedicated `carrier-operations` format.
- Modern aircraft such as the F-16 need tighter separation between normal procedures, combat setup, avionics/sensors, weapons, and mission data.
- Helicopters such as the AH-64D need a strong `reference-tables` and `cockpit-controls` family because station roles, symbols, radios, and weapon codes can dominate the kneeboard.

## Naming conventions

Authoring files retain the style for traceability:

```txt
<aircraft>_<style>_<page-number>_<format>.html
```

DCS export PNGs omit the style because the selected day/night pack is installed
as a unit:

```txt
<aircraft>_<page-number>_<format>.png
```

Place the zero-padded page number before the format in both conventions so
ordinary lexical sorting preserves kneeboard page order. Day and night exports
may use the same PNG names when stored or distributed in separate pack folders.

Example:

```txt
fw190-a8_ww2-german-day_01_normal.html
fw190-a8_01_normal.png
fw190-a8_03_weapons.png
f14b_01_carrier.png
ah64d_03_reference.png
```
