# Style: Modern Night

## Purpose

A low-glare style for modern aircraft and helicopter kneeboards used during
night missions, in dark cockpits, or in VR where bright pages harm adaptation.

Use for night versions of:

- F-16C
- F/A-18C
- A-10C
- AH-64D
- modern helicopters
- late Cold War aircraft using a modern digital presentation

## Visual Character

```txt
dim mission tablet + cockpit quick-reference display
```

Modern Night should retain the same information architecture as Modern Day while
reducing emitted brightness. It is not a simple color inversion.

## Palette

Recommended semantic palette:

```txt
background: deep graphite / dark blue-grey
panel background: slightly raised dark neutral card
text: low-glare off-white / pale cool grey
muted text: desaturated medium grey
section header: very dark card strip or outlined header
section header text: pale off-white
accent: restrained cyan, green, amber, or orange
critical: amber marker, outline, or compact chip
warning: red-orange/amber outline and label
caution: thin amber side marker
borders: dim cool grey
```

Use color only where it improves recognition. Large bright fills should be
avoided, including for critical states.

Avoid:

- pure black with pure white text
- bright blue across large areas
- neon accents
- glowing shadows and bloom
- large yellow or red warning blocks
- thin low-contrast type

## Typography

Use the same family and hierarchy as Modern Day so paired packs feel consistent.

Night-specific adjustments:

- slightly increase body size or weight when required
- preserve tabular numerals
- avoid ultra-thin fonts
- allow more line spacing where contrast is reduced

## Layout

Use the same page grammar and section order as Modern Day:

```txt
Header
  aircraft | page family | night/mode chip
Body
  cards, tables, or flow blocks
Footer
  page number | version/date or source note
```

Night adaptations:

- prefer outlines and separators over filled panels
- reduce the number of simultaneous accent colors
- use spacing and borders to group content
- keep important values brighter than labels where useful

## Section Headers

Preferred patterns:

- dark outlined header with pale text
- small uppercase label with a dim accent rule
- compact header with a restrained left accent border

Avoid bright full-width header fills.

## Emphasis Mapping

```txt
normal: low-glare off-white / pale grey
muted: dim desaturated grey
optional: dim grey with a small tag
critical: amber outline, side marker, or compact chip
warning: red-orange/amber border and warning label
caution: thin amber side marker
```

Emphasis must remain distinguishable without relying on color alone. Pair color
with labels, borders, weight, or position.

## Modern Aircraft Rules

Keep task families separated:

- normal aircraft operation
- combat setup
- sensor setup
- weapons employment
- navigation and mission data
- cockpit controls and HOTAS
- reference tables

Do not imitate an aircraft multifunction display unless the content specifically
requires that display's symbology. Kneeboard readability takes priority.

## Night Adaptation Rules

- Test at reduced display brightness.
- Check readability in both flat-screen and VR use.
- Keep the page background dark enough to avoid a bright rectangular flash.
- Ensure warnings remain visible when accent saturation is reduced.
- Do not encode state using red/green color alone.

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
