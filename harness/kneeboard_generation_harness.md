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
- Target format or set of formats: one or more format design docs.

Optional:

- DCS module name.
- Day/night target.
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

### 5. Render to HTML

Use `skills/05-html-rendering.md` and the selected style doc.

HTML should use semantic classes from `templates/html-class-contract.css`.

### 6. QA review

Use `skills/06-qa-review.md`.

Review for:

- Procedure order.
- Missing critical actions.
- Visual hierarchy.
- Readability at kneeboard size.
- Day/night suitability.
- Section type correctness.
- Whether source quirks have been accidentally copied.

## Source observations from the sample batch

The expanded sample set suggests these format families are necessary:

- WW2 piston aircraft benefit from `normal-checklist`, `engine-management`, and compact `weapons-employment` pages.
- Cold War jets need `normal-checklist`, `combat-fence`, `weapons-employment`, `navigation`, and sometimes `sensors-and-avionics`.
- Carrier aircraft such as the F-14 need a dedicated `carrier-operations` format.
- Modern aircraft such as the F-16 need tighter separation between normal procedures, combat setup, avionics/sensors, weapons, and mission data.
- Helicopters such as the AH-64D need a strong `reference-tables` and `cockpit-controls` family because station roles, symbols, radios, and weapon codes can dominate the kneeboard.

## Naming convention

Suggested page names:

```txt
<aircraft>_<style>_<format>_<page-number>.html
<aircraft>_<style>_<format>_<page-number>.png
```

Example:

```txt
fw190-a8_ww2-day_normal_01.html
fw190-a8_ww2-day_weapons_01.png
f14b_cold-war-night_carrier_01.png
ah64d_modern-unified_reference_03.png
```
