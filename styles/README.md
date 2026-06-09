# Design Composition

The design layer describes what physical or operational artifact a kneeboard
should resemble. It is composed from three parts:

```txt
document archetype + aircraft treatment + lighting profile
```

- **Document archetype** defines the physical artifact: binder sheet, briefing
  ledger, technical field form, sortie card, or professional folio.
- **Aircraft treatment** supplies restrained aircraft, service, era, and role
  character without redefining the whole layout.
- **Lighting profile** adapts the artifact for daylight or low-glare use.

Formats remain separate. A `normal-checklist` and a `reference-table` can use
the same design profile while retaining different semantic structures.

## Start With One Sentence

Before selecting colors or fonts, complete:

```txt
This kneeboard should feel like:
________________________________
```

Examples:

- A pilot's briefing ledger from an RAF dispersal hut.
- A technical field form issued with a Luftwaffe fighter.
- A checklist sheet pulled from a punched USAF technical-order binder.
- A professional flight folio used by a demonstration team.
- A squadron sortie card carried by an interceptor pilot.

If the sentence does not imply a physical document or operational context, the
design direction is probably too superficial.

## Directories

| Path | Purpose |
| --- | --- |
| [`archetypes/`](archetypes/) | Reusable physical-document metaphors |
| [`treatments/`](treatments/) | Aircraft, service, role, and origin character |
| [`lighting/`](lighting/) | Day and low-glare adaptations |
| [`../aircraft-profiles/`](../aircraft-profiles/) | Composed profiles for aircraft examples |

The older top-level style files are composed implementations and compatibility
references. They may gradually move to explicit profiles without invalidating
existing pages.
