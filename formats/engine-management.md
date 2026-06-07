# Format: Engine Management

## Purpose

A page format for power settings, operating limits, temperatures, pressure, boost/ATA, RPM, cooling, fuel, and engine handling.

Especially important for WWII piston aircraft and some Cold War jets.

## Typical sections

```txt
Power Settings
Takeoff Power
Climb Power
Cruise / Economy
Combat / Emergency Power
Temperature Limits
Pressure Limits
Cooling Management
Fuel Management
Relight / Restart Quick Reference
```

## Content types

Allowed:

- power tables
- limit tables
- short action rows
- cautions/warnings
- temperature/pressure notes

Avoid:

- full normal checklist unless only a few rows are needed inline
- detailed emergency procedures; use `emergency`

## WW2 examples

```txt
Max Takeoff / Combat | +18 BOOST / 3000 RPM | 5 min
Max Climbing | +12 BOOST / 2850 RPM | 1 hour
Max Continuous | +7 BOOST / 2650 RPM
Economy | -4 BOOST / 1800 RPM
Oil Temp | 15-105 C
Radiator Temp | 60-135 C
```

## Cold War examples

```txt
Military Power | LIMIT
Afterburner | AS REQ.
EGT | MONITOR
Relight Envelope | CHECK
Fuel Transfer | AUTO / MAN
```

## Emphasis rules

- hard engine limits: `warning`
- normal power settings: `normal`
- emergency power: `critical` or `warning` depending context
- monitoring notes: `caution`
