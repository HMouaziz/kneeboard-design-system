# Contributing

Contributions should keep the design system reusable, source-aware, and clearly
separated from authoritative flight documentation.

## Before Opening a Pull Request

- Keep content, format, document archetype, aircraft treatment, and lighting
  concerns separate.
- Explain the physical artifact represented by a new archetype.
- Prefer adding an aircraft treatment when the distinction is primarily
  insignia, color, typography, service, or role.
- Prefer extending an existing archetype when the distinction is only cosmetic.
- Use fictional or minimal data where a real procedure is not necessary.
- Cite the source category for procedural examples and avoid copying substantial
  text, diagrams, or artwork from copyrighted manuals.
- Mark simulator-specific behavior explicitly.
- Do not submit classified, export-controlled, proprietary, or personally
  identifying material.

## Documentation Style

- Use concise Markdown and descriptive headings.
- Use lowercase kebab-case filenames.
- Keep examples illustrative and label assumptions.
- Preserve the semantic class and field names already used by the templates.
- Use ASCII unless an aircraft label or source term requires another character.

## Review Checklist

Before submitting a change, check that:

- Links and referenced paths resolve.
- The change does not imply official endorsement or real-world validation.
- Operational values are either sourced and scoped or clearly placeholders.
- A new format has a distinct content purpose.
- A new archetype has a distinct physical-document metaphor.
- A treatment does not duplicate an archetype.
- The design remains compatible with the semantic HTML class contract.

## Rendered Examples

Representative, source-safe PNGs may be committed under `examples/gallery/`.
Do not commit complete release archives, extracted manuals, or large source
files. Full packs belong in GitHub Releases, DCS User Files, or ignored
`output/`.

By contributing, you agree that your contribution is licensed under the
repository's MIT License.
