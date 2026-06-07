# Style: Modern Unified

## Purpose

A clean, high-readability style for modern DCS modules that works acceptably in both day and night contexts.

Use for:

- F-16C
- F/A-18C
- A-10C
- AH-64D
- modern helicopters
- late Cold War aircraft when a clean UI style is preferred

## Visual character

```txt
mission tablet + cockpit kneeboard + quick-reference card
```

It should be cleaner and more systematic than WWII or Cold War styles.

## Palette

Recommended semantic palette:

```txt
background: dark neutral graphite or very dark blue-grey
panel background: slightly raised dark card
text: off-white
muted text: medium grey
section header: darker card strip or subtle filled header
accent: controlled cyan/green/amber/orange, one primary accent per aircraft pack
critical: high-contrast amber/yellow chip or left bar
warning: red-orange/amber warning label
borders: low-contrast grey
```

This style is “unified” because it avoids blinding white day pages while preserving enough contrast for night use.

## Typography

- clean sans-serif
- tabular numerals
- clear hierarchy
- compact but not cramped
- uppercase for acronyms and system states

## Layout

Modern aircraft often need several focused page families. The style should support:

- cards
- tables
- mode matrices
- sensor flow blocks
- HOTAS/cockpit control maps
- mission data cards
- icon/symbol legends

Default page anatomy:

```txt
Header
  aircraft | page family | mode/context chip
Body
  cards, tables, or flow blocks
Footer
  page number | version/date if needed
```

## Section headers

Prefer compact card headers over heavy black bars.

Possible patterns:

- small uppercase label with accent line
- filled dark card header
- left accent border

## Emphasis mapping

```txt
normal: off-white text
muted: medium grey text
optional: grey text with small tag
critical: amber chip/left bar
warning: red-orange or amber warning chip
caution: amber side marker
```

## Modern aircraft-specific rules

Modern pages should avoid turning into a wall of cockpit procedure. Split by task:

- normal aircraft operation
- combat setup
- sensor setup
- weapons employment
- navigation / mission data
- cockpit controls / HOTAS
- reference tables

AH-64D-style material shows that modern aircraft often need more reference pages than checklist pages. This is expected and should not be forced into normal checklist format.

## Best format matches

All formats are supported, especially:

- combat-fence
- sensors-and-avionics
- weapons-employment
- navigation
- cockpit-controls
- reference-tables
- mission-data-card
- emergency

## Future optional split

A future system may add:

```txt
modern-day
modern-night
```

For now, Modern Unified should be the default modern style unless the user specifically wants separate day/night outputs.
