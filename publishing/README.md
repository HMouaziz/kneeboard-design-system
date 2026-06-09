# Publishing Kneeboard Packs

The design-system repository documents and demonstrates the authoring system.
Complete generated packs should normally be distributed through GitHub Releases
and DCS User Files.

## Recommended Workflow

1. Author locally in ignored `output/<aircraft>/`.
2. Create a pack manifest from
   [`templates/pack-manifest-template.yaml`](../templates/pack-manifest-template.yaml).
3. Build the DCS installation structure.
4. Verify all PNGs, names, module folders, and installation instructions.
5. Create a versioned ZIP.
6. Publish the ZIP as a GitHub Release asset.
7. Publish the same ZIP on DCS User Files.
8. Add release links to the relevant example README.

## DCS Archive Structure

Start inside the user's DCS Saved Games directory. Do not assume whether the
folder is named `DCS`, `DCS.openbeta`, or something else.

```txt
Kneeboard/
  <DCS module folder>/
    aircraft_01_normal.png
    aircraft_02_reference.png
    ...
INSTALL.md
pack.yaml
```

When one pack supports multiple DCS module folders, include each folder under
the same `Kneeboard/` root.

Day and night files may be distributed together. Explain that users can install
only the variant they want or delete the unwanted files.

## GitHub Releases

Use a tag such as:

```txt
fw190-a8-kneeboard-v2.0.0
```

Attach:

- the installable ZIP
- optional contact-sheet preview
- checksums when useful

The release description should list module folders, page count, day/night
variants, source scope, installation path, and important limitations.

## DCS User Files Listing

Include:

- exact DCS module name
- pack version
- page count and variants
- installation instructions beginning at `Saved Games/<your DCS folder>/`
- source and accuracy statement
- unofficial simulation-only disclaimer
- GitHub project and release links
- several readable preview images

Avoid implying endorsement by Eagle Dynamics, the module developer, an aircraft
manufacturer, or a military organization.

## Forks and Personal Pack Repositories

Forking is supported for authors who want their aircraft profiles, content, and
examples version-controlled with the design system. It is not required.

Authors may instead:

- keep generated work local
- maintain a separate kneeboard-pack repository
- use this repository as a template/reference

Do not commit copyrighted source manuals or extracted guide text to a public
fork unless redistribution is explicitly permitted.
