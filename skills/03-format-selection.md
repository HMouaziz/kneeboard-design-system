# Skill: Format Selection

## Goal

Choose the correct page format(s) for the normalized content.

## Rule

Formats describe **what kind of page this is**, not how it looks.

A format can be rendered in any visual style.

## Selection guide

### Use `normal-checklist` when content includes:

- prestart
- startup
- taxi
- before takeoff
- takeoff
- after takeoff
- approach
- landing
- after landing
- shutdown

### Use `combat-fence` when content includes:

- fence in/fence out
- master arm
- countermeasures
- lights
- IFF
- weapon safety
- radar/ECM combat configuration
- post-attack safing

### Use `weapons-employment` when content includes:

- gunsight setup
- missile, rocket, bomb, or gun employment
- delivery profiles
- sight depression/range tables
- weapon release conditions
- attack diagrams

### Use `sensors-and-avionics` when content includes:

- radar modes
- RWR
- TGP/TADS/PNVS
- datalink
- MFD/HOTAS flow
- target acquisition systems
- two-crew station sensor logic

### Use `navigation` when content includes:

- TACAN
- radio navigation
- INS alignment/use
- waypoint entry
- HSI/ADI/nav mode setup
- kneeboard route data

### Use `carrier-operations` when content includes:

- catapult setup
- launch bar
- hook
- DLC
- Case I/II/III
- marshal
- approach speeds
- trap checklist

### Use `engine-management` when content includes:

- power/RPM/boost/ATA tables
- supercharger settings
- radiator/cowl flap management
- oil/fuel temperature and pressure limits
- war emergency power/combat power limits

### Use `emergency` when content includes:

- engine failure
- fire
- hydraulic/electrical failure
- gear/flap failure
- ejection/bailout
- forced landing

### Use `reference-tables` when content includes:

- conversion tables
- symbol legends
- threat tables
- brevity/code tables
- cockpit abbreviations
- quick lookup data

### Use `cockpit-controls` when content includes:

- switch location map
- HOTAS mapping
- cockpit panel map
- pilot/gunner station control references

### Use `mission-data-card` when content includes:

- frequencies
- callsigns
- bullseye
- package data
- laser codes
- datalink IDs
- loadout
- target coordinates
- TOT

## Anti-patterns

- Do not put radar pages into `weapons-employment` just because radar is used for missiles.
- Do not put all tables into `reference-tables`; power tables belong in `engine-management` if they are used during flight.
- Do not make a separate format for every aircraft-specific section name.
- Do not let visual style names become format names.
