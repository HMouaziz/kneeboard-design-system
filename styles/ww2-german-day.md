# Style: WW2 German Day

Version: 2.0

## Purpose

A daylight field-form style for German WWII aircraft such as the Fw 190 and
Bf 109. It implements the shared rules in `ww2-base.md`.

## Visual Character

```txt
Luftwaffe technical form + cockpit working sheet + field annotations
```

The page should feel issued and used: pre-printed rules, typed values, inspection
marks, and restrained aircraft identification.

## Palette

Recommended semantic palette:

```txt
paper: cool field-grey/off-white stock, low saturation
secondary stock: slightly darker grey-beige
primary ink: blue-black or carbon-black
secondary ink: graphite grey
form rules: faded blue-grey
origin colors: black / warm white / muted red
critical mark: red grease-pencil rule or graphite hatch
warning: double-rule box or stamped outline
```

Avoid:

- bright pure white background
- yellow parchment
- large dark filled header bars
- repeated modern cards
- saturated flag colors
- heavy drop shadows
- glossy digital effects

## Origin Marks

- Use a simplified Balkenkreuz-style aircraft recognition mark. The current
  cross is intended to reference this Luftwaffe aircraft marking, not a generic
  decorative cross.
- A narrow black/white/red registration stripe may appear once in the header.
- Use `DEUTSCH` or an aircraft document code as a small registration label.
- Do not use political emblems.

An externally supplied replacement icon should be historically appropriate,
legible at kneeboard scale, and preferably available as SVG. Aircraft/service
insignia are preferred over state or political emblems.

## Typography

Use condensed mechanical sans-serif faces. Headings should resemble pre-printed
form labels; values should resemble typed or stamped entries. Do not use a
handwriting font.

## Layout

```txt
registration header: origin mark | aircraft | document fields
stamped page-purpose title
one or two ruled form columns
document footer: source | Blatt/page | revision
```

Sections should be separated by open rules, not filled cards. Section names sit
on the upper rule like a form legend. Dotted leaders remain acceptable.

## Emphasis

```txt
normal: blue-black typed entry
muted: graphite note
critical: red side rule plus sparse diagonal pencil hatch
warning: double-rule stamped box
caution: short red margin mark
```

## Diagram treatment

Use sparse blue-black technical line art with form-style labels.

## Best format matches

- normal-checklist
- engine-management
- weapons-employment
- reference-tables
- emergency
