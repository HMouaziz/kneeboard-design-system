# Skill: Pagination and Density

## Goal

Turn normalized content and selected formats into readable kneeboard pages.

## Page size assumption

Default DCS kneeboard target:

```txt
portrait page
high readability at cockpit kneeboard scale
HTML exported to PNG
```

The exact pixel size can vary, but every style should assume narrow portrait reading.

## Density levels

### Sparse

Use for:

- training pages
- new aircraft learning
- visual guides
- diagrams

Characteristics:

- fewer sections per page
- larger text
- more spacing
- more notes

### Normal

Use for:

- standard kneeboard checklists
- most aircraft pages

Characteristics:

- balanced density
- action rows remain readable
- notes are short

### Dense

Use for:

- experienced pilot quick references
- many short action rows
- reference tables

Characteristics:

- smaller text
- tighter row height
- limited notes
- strong section hierarchy needed

### Emergency-card

Use for:

- emergency procedures
- irreversible safety procedures

Characteristics:

- very clear hierarchy
- strong warnings
- minimal decoration
- no cramped text

## Page splitting rules

Split a page when:

- Two unrelated formats are competing for space.
- Critical procedures become visually buried.
- Tables dominate more than half the page.
- Diagrams become too small to read.
- Notes become long enough to interrupt checklist scanning.

Do not split a page just because the source did.

## Recommended splits by era

### WW2

Common split:

```txt
Page 1: Normal Checklist
Page 2: Engine Management / Reference
Page 3: Weapons Employment
```

For simple aircraft, engine management can be embedded into normal checklist.

### Cold War

Common split:

```txt
Page 1: Normal Checklist
Page 2: Combat Fence + Weapons Setup
Page 3: Navigation / Sensors
Page 4: Reference Tables
```

Carrier aircraft may add a carrier operations page.

### Modern

Common split:

```txt
Page 1: Normal Checklist
Page 2: Combat Fence
Page 3: Sensors and Avionics
Page 4: Weapons Employment
Page 5: Navigation / Mission Data
Page 6+: Reference Tables / Cockpit Controls
```

## Row ordering

Within a procedural checklist, preserve cockpit sequence unless there is a strong reason to group by system.

Within a reference page, group by lookup task rather than aircraft system.

Example:

- Good: `Landing speeds`, `Power settings`, `Temperature limits`.
- Worse: `Engine`, `Hydraulic`, `Electrical`, if the user only needs final approach data.
