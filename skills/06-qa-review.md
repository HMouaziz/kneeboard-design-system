# Skill: QA Review

## Goal

Review the generated kneeboard for cockpit usability, consistency, and source fidelity.

## QA checklist

### Content

- Aircraft name and variant are correct.
- Procedure order is plausible.
- Critical safety items are present.
- Optional items are marked as optional or muted.
- DCS-specific simplifications are marked when needed.
- Units are preserved and consistent.
- No source text was accidentally misread.

### Format

- Page uses the correct format family.
- Sections belong to that format.
- Tables are not hidden inside normal checklist flow unless they are short.
- Combat/fence items are separate from startup/shutdown unless page count requires a combined card.
- Emergency procedures are not visually buried.

### Style

- Style matches requested era/day/night target.
- Critical items are visible but not visually obnoxious.
- Muted items are readable but secondary.
- Header/footer/page number are consistent.
- The page still looks like part of the design system, not a copy of the source.

### Readability

- Text is readable at kneeboard size.
- Dotted leaders or value alignment do not overpower the text.
- No section is too cramped.
- Notes are clearly distinct from actions.
- Tables and diagrams are large enough to use.

### Export

- PNG crop is correct.
- Page background reaches the edges.
- No browser UI or white margin leaked into the render.
- Dark/night styles are not crushed or too low contrast.
- File names follow the naming convention.

## QA output format

```txt
Status: pass / needs revision
Main issues:
- ...
Suggested fixes:
- ...
Ready to export PNG: yes/no
```
