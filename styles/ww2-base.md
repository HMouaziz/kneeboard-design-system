# Style Family: WW2

Version: 2.0

## Purpose

Shared structural rules for origin-specific WWII kneeboard styles.

WWII is a style family, not one universal visual theme. Every rendered page must
select an aircraft-origin variant such as:

```txt
ww2-german-day
ww2-german-night
ww2-british-day
ww2-american-day
```

German and British day/night variants are currently implemented.

## Core Character

```txt
working form + field annotation + aircraft technical document
```

The page should feel completed, stamped, corrected, or marked for cockpit use.
It should not resemble a modern dashboard made vintage through color alone.

## Form Logic

- Prefer ruled blocks, underlined headings, registration fields, stamps, and
  margin marks over repeated filled cards.
- Let some information share a continuous sheet instead of placing every group
  inside an isolated panel.
- Use slight variation in rule weight, inset, and heading treatment to imply a
  working document while preserving alignment.
- Values may resemble typed or stamped entries in a pre-printed form.
- Critical actions may resemble pencil, grease-pencil, or inspection marks.
- Texture must remain subtle enough that text is always the strongest signal.

This is a handwritten-form *logic*. Do not rely on handwriting fonts.

## Origin Layer

Each origin style may define:

- national or service color references
- aircraft insignia or a simplified service mark
- document conventions and label vocabulary
- stamp shape
- rule and ink colors
- night-light response

Origin marks are decorative identification, not content. Do not use prohibited
political symbols. Prefer aircraft/service insignia and restrained color bars.

## Scan Purpose

Each page answers one cockpit question:

```txt
normal: What do I do next?
reference: What number or limit do I need?
combat: How do I arm, attack, safe, and recover?
```

## Emphasis Semantics

```txt
normal text: standard procedure or reference data
muted text: optional, contextual, or explanatory information
marked row: action gate or critical scan item
inset note: warning, reminder, or special note
```

Emphasis should look applied to the form, not like a modern UI component.
