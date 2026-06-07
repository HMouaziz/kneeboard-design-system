# Format: Weapons Employment

## Purpose

A page format for using weapons, not merely arming them.

Use for guns, bombs, rockets, missiles, sight settings, delivery profiles, employment constraints, and attack diagrams.

## Typical sections

```txt
Gunsight / Sight Setup
Guns
Rockets
Bombs
Missiles
Delivery Profiles
Weapon Tables
Attack Diagram
Post-Release / Escape
```

## Content types

Allowed:

- action rows
- setup rows
- weapon selector rows
- tables
- diagrams
- short warnings
- release parameters

Avoid:

- general fence-in state unless needed as a small prerequisite
- deep sensor/radar setup; move to `sensors-and-avionics`
- full mission data; move to `mission-data-card`

## Page planning

### Simple weapons page

Good for WWII aircraft:

```txt
Gunsight
Guns
Bombing
Rockets if present
```

### Multi-page weapons pack

Good for Cold War/modern aircraft:

```txt
Page 1: Weapon selectors and master modes
Page 2: Air-to-air weapons
Page 3: Air-to-ground weapons
Page 4: Bombing/rocket profiles
```

## Diagrams

Use diagrams when they materially improve cockpit use:

- dive bombing profile
- rocket attack profile
- gunsight range picture
- missile employment envelope
- attack/egress flow

WW2 diagrams should be simple line art.

Modern diagrams can use clean flow blocks or profile cards.

## Row examples

```txt
Gun Sight | ON
Range | 300 yd
Base Span | SET
Bomb Release Altitude | 3000 ft
Dive Angle | 45-60 deg
Master Arm | ARM | critical
```

## Emphasis rules

- Weapon safety / master arm: `critical`
- Release constraints: `warning` or `caution`
- Loadout-dependent items: `optional`
- Training-only notes: `muted` or `dcs-specific`
