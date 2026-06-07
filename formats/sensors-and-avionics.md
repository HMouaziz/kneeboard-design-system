# Format: Sensors and Avionics

## Purpose

A page format for systems that find, track, designate, identify, or manage targets and aircraft state.

Use for radar, RWR, datalink, TGP, TADS/PNVS, IHADSS, MFD/HOTAS flows, and sensor mode references.

## Typical sections

```txt
Radar Setup
Radar Modes
RWR / Threat Display
Datalink
Targeting Pod / TADS
Helmet Sight / IHADSS
MFD Pages
HOTAS Flow
Sensor Handoff
Crew Coordination
```

## Content types

Allowed:

- mode tables
- flow blocks
- HOTAS command rows
- sensor setup rows
- symbol legends
- crew/station-specific steps
- small diagrams

Avoid:

- normal startup flow
- actual weapon release procedure unless sensor operation and release are inseparable
- huge manual excerpts

## Page planning

Use separate pages when:

- radar and targeting pod each need their own flow
- pilot and gunner/WSO/CPG roles differ
- symbol legends are large
- MFD pages or HOTAS maps dominate

## Modern helicopter note

AH-64D-style content often requires station-aware sensor pages:

```txt
Pilot
CPG
TADS
PNVS
IHADSS
George AI / crew interface if DCS-specific
```

Mark DCS-specific AI or interface steps clearly.

## Cold War note

Cold War radar pages should be simple and practical:

```txt
Power / Warmup
Mode
Range
Elevation
Lock / Break Lock
Boresight / ACM if available
```
