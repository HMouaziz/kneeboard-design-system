# Skill: Source Intake

## Goal

Read the provided source material and identify what kind of kneeboard content it contains before redesigning anything.

## Inputs

- One or more source files: PNG, JPG, PDF, HTML, text, or screenshots.
- Aircraft name/variant if known.
- Target style/format if known.

## Output

Produce a short source inventory:

```txt
Aircraft:
Era:
Source files:
Detected page types:
Detected sections:
Special elements:
Likely target formats:
Open questions:
```

## What to look for

### Page family

Identify whether each page is primarily:

- normal checklist
- combat/fence checklist
- weapons employment
- sensors/avionics
- navigation
- carrier operations
- engine management
- emergency
- reference tables
- cockpit controls
- mission data card

### Section names

Capture section titles exactly first, then normalize later.

Examples:

```txt
PRESTART
ENGINE START
TAKEOFF
LANDING
FENCE IN
GUNSIGHT
BOMBING
RADAR
TACAN
CASE I RECOVERY
```

### Content shapes

Mark content shape because it affects layout:

- action row: `Label ........ Value`
- note row: instructional text
- condition row: `When below 160 mph`
- table
- diagram
- cockpit map
- weapon profile
- symbol legend
- frequency/card data
- warning/critical item

## Rules

- Do not redesign during intake.
- Do not decide that source page count equals final page count.
- Do not force aircraft quirks into global format rules.
- Record uncertainty rather than guessing.

## Sample observation patterns

From the sample set:

- Spitfire/FW 190 sources strongly inform WW2 normal checklist and WW2 weapons pages.
- F-5E/MiG-21/Mirage F1 sources are useful for Cold War normal, combat, and weapon sections.
- F-14 sources add carrier and two-crew/complex avionics considerations.
- F-16 sources add modern HOTAS/MFD/system setup expectations.
- AH-64D sources add day/night design, station-specific references, symbols, and reference-heavy page families.
