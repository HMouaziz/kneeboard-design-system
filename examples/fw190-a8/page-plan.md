# Example Page Plan: Fw 190 A-8 Anton

## Artifact statement

An issued Luftwaffe cockpit operating card derived from a technical field form.

This is the canonical example of composing an archetype and treatment:

```txt
technical-field-form
        +
luftwaffe-ww2
        =
Fw 190 A-8 cockpit operating card
```

The physical-document logic does most of the identity work. The compact
registration docket, open ruled sections, typed values, issue fields, and
restrained inspection marks matter more than national colors.

## Source and scope

- Original one-page Anton quick checklist supplied by the user
- `DCS FW190A-8 Guide.pdf` by Charles Ouellet
- Accuracy mode: DCS practical quickstart
- Output: matching 1200 x 1600 day and low-glare night PNGs

The pack stays at three pages. Each page has one primary scan purpose.

## Page 1: Normal Procedures

Format: `normal-checklist`

Scan purpose: What do I do next?

```txt
Before Start
Engine Start
Post-Start / Warm-Up
Taxi / Before Takeoff
Takeoff / After Takeoff
Landing
Shutdown
```

Keep the starter clutch, rotation, touchdown, ready-to-taxi, and shutdown
fuel-lever rows as action gates.

## Page 2: Engine & Flight Reference

Format: `engine-management` + `reference-tables`

Scan purpose: What number or limit do I need?

```txt
BMW 801D-2 Power
Engine Limits
Overheat
Fuel
Key Speeds
Dive Limits
Radiator / Propeller
Taildragger Notes
```

This page is required, not optional. It carries the highest-value guide-derived
data that is difficult to recall in flight.

## Page 3: Combat & Weapons

Format: `combat-fence` + `weapons-employment`

Scan purpose: How do I arm, attack, safe, and recover?

```txt
Fence In
Guns / REVI 16B
SC-250 Setup
BR 21 Rockets
SC-250 Dive Profile
Ordnance Jettison
Fence Out
Combat Reminder
```

The combat reminder stays visually secondary to selectors, fuzing, release,
jettison, and safing actions.

## Style constraints

- Use cool field-grey stock, not yellow parchment.
- Use a compact issue docket, not a poster header.
- Keep sections open and ruled instead of placing every section in a card.
- Use the Balkenkreuz as a restrained aircraft-origin identifier.
- Preserve useful cockpit labels such as `AUF`, `ZU`, `EIN`, `AUS`, `Sturz`,
  `Wagerecht`, `MV`, and `OV`.
- Exclude political emblems.
- Day and night versions must keep identical content and page breaks.
