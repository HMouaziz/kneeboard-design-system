# Kneeboard Design System

A documentation-first design system for turning aircraft reference material into
consistent, readable simulator kneeboards.

The repository separates source content, page structure, and visual style so the
same normalized procedure can be rendered for different eras, formats, and
day/night environments.

> [!IMPORTANT]
> This is an unofficial community project for flight simulation. It is not
> affiliated with or endorsed by Eagle Dynamics, aircraft manufacturers, module
> developers, or military organizations. The material is not validated for
> real-world aviation, training, or operational use. Verify procedures and limits
> against the current documentation for the simulator module you use.

## What This Repository Contains

- An end-to-end authoring workflow for building a kneeboard pack
- Semantic templates for normalizing aircraft procedures and reference data
- Format guides for checklists, weapons, navigation, emergencies, and more
- Visual direction for WWII, Cold War, modern, day, and night presentations
- Page-planning, density, HTML-rendering, and QA guidance
- Small examples that demonstrate the intended workflow

This repository defines the system and its contracts. It does not currently
include a renderer, complete aircraft kneeboard packs, or authoritative aircraft
procedures.

## Core Model

```text
source material + normalized aircraft content + format + style = kneeboard pages
```

- **Source material** supplies the facts to be represented.
- **Aircraft content** stores those facts in a presentation-neutral structure.
- **Format** defines the page's semantic structure.
- **Style** defines its visual language.

Keeping these concerns separate makes content easier to review, reuse, restyle,
and maintain.

## Repository Map

| Path | Purpose |
| --- | --- |
| [`harness/`](harness/) | End-to-end generation workflow and output contract |
| [`skills/`](skills/) | Focused guidance for intake, normalization, planning, rendering, and QA |
| [`formats/`](formats/) | Semantic page families and layout rules |
| [`styles/`](styles/) | Era and lighting-specific visual direction |
| [`templates/`](templates/) | Content schema, page specification, and HTML class contract |
| [`examples/`](examples/) | Sample observations and page-planning decisions |

## Supported Page Formats

- Normal checklist
- Combat fence
- Weapons employment
- Sensors and avionics
- Navigation
- Carrier operations
- Engine management
- Emergency procedures
- Reference tables
- Cockpit controls
- Mission data cards

## Available Styles

- WWII Day
- WWII Night
- Cold War Day
- Cold War Night
- Modern Unified

## Suggested Workflow

1. Start with [`harness/kneeboard_generation_harness.md`](harness/kneeboard_generation_harness.md).
2. Record source observations with [`skills/01-source-intake.md`](skills/01-source-intake.md).
3. Normalize the content using
   [`templates/aircraft-content-template.md`](templates/aircraft-content-template.md).
4. Select formats and plan pages using the guides in [`formats/`](formats/).
5. Apply a visual direction from [`styles/`](styles/).
6. Build HTML against
   [`templates/html_class_contract.css`](templates/html_class_contract.css).
7. Review the output with [`skills/06-qa-review.md`](skills/06-qa-review.md).

The examples are illustrative rather than authoritative. Replace their aircraft
details with information verified against your chosen source material.

## Design Principles

1. **Separate content from presentation.** Store meaning such as `critical`,
   `optional`, `condition`, or `dcs-specific`, not visual instructions.
2. **Separate style from format.** A checklist structure should remain reusable
   across visual themes.
3. **Design for cockpit readability.** Prefer focused, quickly scannable pages
   over reproducing an entire manual.
4. **Label simulator-specific simplifications.** Do not present game behavior as
   real-world aircraft doctrine.
5. **Preserve aircraft character within a predictable page grammar.**
6. **Keep provenance visible.** Generated packs should identify their sources,
   assumptions, and verification status.

## Project Status

The design system is usable as an authoring reference, but it is still evolving.
The most useful future additions would be:

- A reference HTML/CSS renderer
- Schema validation for normalized content and page specifications
- Rendered example pages
- Automated checks for structure, links, and page dimensions

## Contributing

Issues and focused pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md)
before proposing a new format, style, or procedural example.

## License

Released under the [MIT License](LICENSE).

Names and trademarks referenced in examples remain the property of their
respective owners.
