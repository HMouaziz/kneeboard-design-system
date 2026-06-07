# Format: Emergency

## Purpose

A high-clarity page format for emergency procedures.

Emergency pages should prioritize fast comprehension over visual style.

## Typical sections

```txt
Engine Failure
Engine Fire
Electrical Failure
Hydraulic Failure
Fuel Emergency
Gear / Flap Failure
Compressor Stall / Flameout
Ejection / Bailout
Forced Landing
```

## Content types

Allowed:

- short numbered steps
- bold condition headers
- warning/caution blocks
- decision gates
- memory items

Avoid:

- decorative diagrams unless they are essential
- dense multi-procedure pages
- long explanatory text

## Layout rules

- Emergency pages should be sparse or normal density, never dense.
- Memory items should be visually distinct.
- Use numbering when order matters.
- Use condition blocks for branching.

## Example skeleton

```txt
ENGINE FIRE
1. Throttle | IDLE
2. Fuel | OFF
3. Fire Handle | PULL
4. Extinguisher | DISCHARGE
If fire persists | EJECT / BAILOUT
```

## Emphasis rules

- emergency title: `warning`
- memory items: `critical`
- irreversible actions: `warning`
- explanatory notes: small but readable
