# Style: Modern Day

## Purpose

A bright, high-readability style for modern aircraft and helicopter kneeboards
used in daylight, bright cockpits, desktop reference, or printed output.

Use for:

- F-16C
- F/A-18C
- A-10C
- AH-64D
- modern helicopters
- late Cold War aircraft when a clean digital style is preferred

## Visual character

```txt
mission tablet + technical quick-reference card + clean cockpit display
```

The style should be systematic and information-dense without looking like a
generic dashboard.

## Palette

Recommended semantic palette:

```txt
background: cool off-white / very pale blue-grey
panel background: white or lightly tinted card
text: near-black / dark navy-charcoal
muted text: medium cool grey
section header: dark navy, graphite, or aircraft-specific dark accent
section header text: white
accent: controlled cyan, blue, green, amber, or orange
critical: high-contrast amber/yellow chip or left bar
warning: red-orange label with strong text contrast
caution: amber side marker or light amber fill
borders: cool medium grey
```

Use one primary accent per aircraft pack. Secondary colors should communicate
meaning, not decoration.

Avoid:

- pure white pages without panel separation
- saturated color across large areas
- translucent glass effects that reduce export clarity
- low-contrast grey text
- decorative cockpit-screen imitation

## Typography

- clean sans-serif
- tabular numerals for frequencies, coordinates, codes, and timing
- clear hierarchy
- compact but not cramped
- uppercase for acronyms, modes, and system states
- minimum weight sufficient for PNG export and VR scaling

## Layout

Modern aircraft often need several focused page families. The style should
support:

- cards
- tables and mode matrices
- sensor flow blocks
- HOTAS and cockpit control maps
- mission data cards
- icon and symbol legends

Default page anatomy:

```txt
Header
  aircraft | page family | day/mode chip
Body
  cards, tables, or flow blocks
Footer
  page number | version/date or source note
```

Day pages may use light panel fills to establish grouping. Keep enough empty
space around high-value data for rapid scanning.

## Section Headers

Preferred patterns:

- dark filled header with white text
- small uppercase label with an accent rule
- light card with a dark left accent border

Do not mix several header patterns on one page.

## Emphasis Mapping

```txt
normal: dark text
muted: medium cool grey
optional: grey text with a small tag
critical: amber/yellow chip, fill, or left bar
warning: red-orange label or outlined warning block
caution: amber side marker or pale amber fill
```

## Modern Aircraft Rules

Split pages by task instead of reproducing a wall of cockpit procedure:

- normal aircraft operation
- combat setup
- sensor setup
- weapons employment
- navigation and mission data
- cockpit controls and HOTAS
- reference tables

Modern helicopters often need more reference pages than checklist pages. This is
expected and should not be forced into the normal checklist format.

## Mission Data Cards

Modern Day is the preferred style for printable or writable mission cards.

- Keep empty fields obvious.
- Use light fills and dark rules.
- Reserve accent color for labels, grouping, and time-critical data.
- Do not tint fields so heavily that handwritten annotations become unclear.

## Best Format Matches

All formats are supported, especially:

- combat-fence
- sensors-and-avionics
- weapons-employment
- navigation
- cockpit-controls
- reference-tables
- mission-data-card
- emergency
