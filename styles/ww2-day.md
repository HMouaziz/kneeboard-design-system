# Style: WW2 Day

## Purpose

A daylight kneeboard style for WWII piston aircraft. It should feel period-appropriate and tactile without becoming a replica of any single existing kneeboard.

Use for:

- Spitfire
- Fw 190
- Bf 109
- P-51
- P-47
- Mosquito
- La-7
- Yak series
- other WWII piston aircraft

## Visual character

```txt
manual card + field note + aircraft checklist
```

The style should feel like a clean modern recreation of a wartime pilot aid: paper, ink, simple hierarchy, high readability.

## Palette

Recommended semantic palette:

```txt
background: warm paper / light parchment
text: near-black
muted text: grey-brown / faded ink
section header: black or very dark charcoal
section header text: off-white
accent: muted yellow / ochre
critical: yellow highlight with black text
warning: boxed amber/yellow or black/yellow strip
borders: black or dark brown
```

Avoid:

- bright pure white background
- neon yellow
- modern blue UI accents
- heavy drop shadows
- glossy digital effects

## Typography

Use a narrow, readable sans-serif or mechanical manual-like face.

Recommended feel:

- condensed headings
- strong uppercase section titles
- readable action text
- italic or smaller note text

Rules:

- Aircraft title may be bold/italicized.
- Section titles should be uppercase.
- Row labels should be title case or cockpit-label uppercase when appropriate.
- Values should be uppercase for switch states.

## Layout

Best suited for:

- one or two columns
- boxed sections
- dotted leader action rows
- compact notes
- small reference tables
- simple line diagrams

Default page anatomy:

```txt
Header
  aircraft name | variant/nickname | day/night marker
Body
  stacked section cards, one or two columns
Footer
  page number/version/source note if needed
```

## Section headers

Use dark header bars with light text.

Optional accent:

- yellow top stripe
- yellow page mode chip
- yellow left marker for important section families

## Rows

Action row pattern:

```txt
Label ................. VALUE
```

Notes should sit below the row and should not use the same leader pattern.

Condition rows can be italic or smaller:

```txt
When engine catches
Below 160 mph
On final
```

## Emphasis mapping

```txt
normal: black text
muted: grey/faded text
optional: grey text or optional tag
critical: yellow highlight row
warning: yellow/black boxed row
caution: thin yellow side marker
```

## Diagram treatment

Use black line art. Keep diagrams simple.

Good uses:

- bombing profile
- landing pattern
- gunsight range explanation
- cockpit switch location mini-map

Avoid photorealistic diagrams unless the source absolutely needs it.

## Era-specific behavior

WWII kneeboards usually need more engine-management information than modern jets:

- RPM
- boost/ATA
- radiator/cowl flap
- oil temperature
- fuel pressure
- supercharger
- mixture/prop control

These should either be embedded in normal checklist or moved to an `engine-management` page.

## Best format matches

- normal-checklist
- engine-management
- weapons-employment
- reference-tables
- emergency

