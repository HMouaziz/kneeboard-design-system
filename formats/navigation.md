# Format: Navigation

## Purpose

A page format for navigation setup, route following, radio navigation, INS/TACAN, waypoint entry, and approach navigation references.

## Typical sections

```txt
Radios
TACAN / ILS / VOR
INS / Alignment
Waypoints
HSI / Course Setup
Approach Navigation
Route Notes
Conversion / Altimeter Tables
```

## Content types

Allowed:

- action rows
- frequency/channel tables
- waypoint tables
- mode setup rows
- compact reference tables

Avoid:

- general mission card data if it changes every mission; use `mission-data-card`
- full startup checklist
- combat radar/sensor modes

## Page planning

Cold War aircraft often need a compact navigation card.

Modern aircraft may need separate pages for:

```txt
INS alignment
Waypoint entry
TACAN/ILS
Mission data
```

## Row examples

```txt
Altimeter | SET
TACAN | T/R
Channel | SET
Course | SET
INS Mode | NAV
Waypoint | SELECT
```

## Notes

If a page contains generic conversion tables such as mbar/inHg/mmHg, it may be either:

- `navigation`, if used during cockpit setup, or
- `reference-tables`, if presented as a general lookup card.
