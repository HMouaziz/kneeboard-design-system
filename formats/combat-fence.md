# Format: Combat Fence

## Purpose

A combat transition checklist for entering and leaving the fight.

This format is for aircraft state, safety, weapons readiness, sensors, lights, IFF, countermeasures, and post-combat safing.

## Typical sections

```txt
Fence In
Combat Setup
Weapons Arm / Master Arm
Sensors / Radar Combat State
Countermeasures
Lights / IFF / Transponder
Fence Out
Recovery Setup
```

## Content types

Allowed:

- action rows
- short mode rows
- optional mission-dependent rows
- warning rows
- small combat setup tables

Avoid:

- detailed weapon employment procedures
- detailed radar theory
- long navigation setup
- startup/shutdown flow

## Page planning

A combat fence page is often compact. It may share a page with weapons setup for simple WWII or Cold War aircraft, but modern aircraft usually benefit from a dedicated page.

Common page layouts:

```txt
Left: Fence In / Combat Setup
Right: Fence Out / Recovery
```

or

```txt
Top: Fence In
Middle: Attack / Combat State
Bottom: Fence Out
```

## Key semantic rows

```txt
Master Arm | ARM / SAFE
Gun Safety | OFF / SAFE
Stores | SET
Countermeasures | PROGRAM / AUTO / MAN
Radar | OPER / STBY / SILENT
Lights | OFF / AS REQ.
IFF | AS REQ.
```

## Emphasis rules

- Master arm changes are usually `critical`.
- Weapon safety cover actions are usually `critical`.
- Lights/IFF are often `optional` or `as-required`.
- Countermeasures may be `critical` in modern combat aircraft.

## Era notes

### WW2

Fence checks are usually simple:

```txt
Gun sight ON
Gun safety OFF
Bombs/rockets armed
Canopy closed
Radiator/power set
```

### Cold War

Expect weapon selectors, radar modes, ECM, IFF, and countermeasure setup.

### Modern

Separate combat fence from detailed sensor/weapon employment unless the page is intentionally a quick card.
