# Format: Normal Checklist

## Purpose

The standard aircraft lifecycle checklist from cockpit entry to shutdown.

Use for ordinary procedural flow, not combat employment or reference-heavy material.

## Typical sections

```txt
Prestart / Cockpit Entry
Before Start
Engine Start
After Start
Warmup
Taxi
Before Takeoff
Takeoff
After Takeoff
Climb / Cruise
Approach
Landing
After Landing
Shutdown
```

Not every aircraft needs every section.

## Content types

Allowed:

- action rows
- condition rows
- short notes
- very small tables
- safety warnings

Avoid:

- large weapons tables
- radar mode explanations
- full emergency procedures
- large cockpit control maps
- carrier marshal diagrams

## Page planning

### One-page normal checklist

Use when:

- aircraft is simple
- rows are short
- no extensive startup complexity
- no dense landing/shutdown sequence

### Two-page normal checklist

Use when:

- startup is long
- landing and shutdown need space
- aircraft has warmup/engine management notes
- two-column layout becomes cramped

Suggested split:

```txt
Page 1: Prestart through After Takeoff
Page 2: Approach through Shutdown
```

## Section ordering rules

Preserve the operational sequence.

Do not alphabetize sections.

Do not group by system unless the source is already a systems checklist and the cockpit flow is unclear.

## Style behavior

- WW2 styles may include more engine warmup and manual power management.
- Cold War styles may include more avionics and navigation setup, but large avionics flows should move to dedicated formats.
- Modern Unified should keep normal checklist lean and move mission/sensor setup elsewhere.

## Example section skeleton

```txt
Section: Engine Start
- Brakes | SET
- Throttle | IDLE / CRACKED
- Fuel Pump | ON
- Starter | PRESS | critical
- When engine catches | condition
- RPM | CHECK
- Generator | ON
```
