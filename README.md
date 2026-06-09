# Kneeboard Design System

A documentation-first design system for turning aircraft reference material into
consistent, readable simulator kneeboards.

The repository separates source content, page structure, document identity,
aircraft treatment, and lighting so the same normalized procedure can be
rendered as different believable aviation artifacts.

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
- Reusable document archetypes, aircraft treatments, and day/night profiles
- Page-planning, density, HTML-rendering, and QA guidance
- Packaging and DCS User Files publishing guidance

This repository defines the authoring system and its contracts. Complete
installable packs and source manuals are not committed here; generated packs
belong in ignored `output/`, GitHub Releases, or DCS User Files.

## Core Model

```text
source material
+ normalized aircraft content
+ format
+ document archetype
+ aircraft treatment
+ lighting
= kneeboard pages
```

- **Source material** supplies the facts to be represented.
- **Aircraft content** stores those facts in a presentation-neutral structure.
- **Format** defines the page's semantic structure.
- **Document archetype** defines the physical artifact: binder sheet, pilot
  ledger, technical field form, sortie card, or professional folio.
- **Aircraft treatment** adds restrained service, role, origin, and aircraft
  character.
- **Lighting** adapts the artifact for daylight or low-glare use.

Keeping these concerns separate makes content easier to review, reuse, restyle,
and maintain.

## Repository Map

| Path | Purpose |
| --- | --- |
| [`harness/`](harness/) | End-to-end generation workflow and output contract |
| [`skills/`](skills/) | Focused guidance for intake, normalization, planning, rendering, and QA |
| [`formats/`](formats/) | Semantic page families and layout rules |
| [`styles/`](styles/) | Archetypes, treatments, lighting, and composed compatibility styles |
| [`aircraft-profiles/`](aircraft-profiles/) | Example aircraft design compositions |
| [`templates/`](templates/) | Content schema, page specification, and HTML class contract |
| [`examples/`](examples/) | Sample observations and page-planning decisions |
| [`publishing/`](publishing/) | Packaging, GitHub Release, and DCS User Files workflow |

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

## Document Archetypes

- Technical field form
- Pilot briefing ledger
- Punched technical order
- Display-team flight folio
- Squadron sortie card

Treatments currently cover Luftwaffe WWII, RAF WWII, early Cold War USAF,
Italian display-team, and French interceptor applications. New treatments
should reuse an archetype unless they represent a genuinely different physical
document.

## Suggested Workflow

1. Start with [`harness/kneeboard_generation_harness.md`](harness/kneeboard_generation_harness.md).
2. Record source observations with [`skills/01-source-intake.md`](skills/01-source-intake.md).
3. Normalize the content using
   [`templates/aircraft-content-template.md`](templates/aircraft-content-template.md).
4. Select formats and plan pages using the guides in [`formats/`](formats/).
5. Write the artifact sentence and compose the design using
   [`skills/05-design-composition.md`](skills/05-design-composition.md).
6. Render HTML using
   [`skills/06-html-rendering.md`](skills/06-html-rendering.md) and
   [`templates/html_class_contract.css`](templates/html_class_contract.css).
7. Review the output with [`skills/07-qa-review.md`](skills/07-qa-review.md).
8. Package and publish using [`publishing/README.md`](publishing/README.md).

The examples are illustrative rather than authoritative. Replace their aircraft
details with information verified against your chosen source material.

## Design Principles

1. **Separate content from presentation.** Store meaning such as `critical`,
   `optional`, `condition`, or `dcs-specific`, not visual instructions.
2. **Separate design from format.** A checklist structure should remain reusable
   across document archetypes.
3. **Design for cockpit readability.** Prefer focused, quickly scannable pages
   over reproducing an entire manual.
4. **Label simulator-specific simplifications.** Do not present game behavior as
   real-world aircraft doctrine.
5. **Design artifacts, not national color themes.** Start from a believable
   document and add aircraft character as a treatment.
6. **Preserve aircraft character within a predictable page grammar.**
7. **Keep provenance visible.** Generated packs should identify their sources,
   assumptions, and verification status.

## Using the Repository

Three workflows are supported:

- **Local authoring:** generate into ignored `output/`.
- **Fork authoring:** keep aircraft profiles and source-safe examples in a fork.
- **Separate pack repository:** use this project as the design reference while
  publishing packs independently.

Forking is optional. Do not commit copyrighted manuals, extracted guide text,
or complete generated release archives to this repository.

## Project Status

The design system is actively evolving. Current priorities include a reference
renderer, schema validation, automated link and dimension checks, and reusable
packaging tools.

## Contributing

Issues and focused pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md)
before proposing a new format, style, or procedural example.

## License

Released under the [MIT License](LICENSE).

Names and trademarks referenced in examples remain the property of their
respective owners.
