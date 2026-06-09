# Skill: Design Composition

## Goal

Choose a believable document identity before designing headers, frames, colors,
or typography.

## Step 1: Write the artifact statement

Complete:

```txt
This kneeboard should feel like:
________________________________
```

The answer should describe a physical document in an operational context.

Good:

```txt
A checklist sheet pulled from a punched USAF technical-order binder.
```

Weak:

```txt
A green American Cold War style.
```

## Step 2: Select an archetype

Choose the closest guide in `styles/archetypes/`.

Ask:

- What object is this page?
- How is it held, filed, carried, or issued?
- What visual motif communicates that before the aircraft name is read?
- Does this archetype work across checklist, reference, combat, and emergency
  formats?

Create a new archetype only when the physical-document metaphor is genuinely
different.

## Step 3: Select an aircraft treatment

Choose or create a guide in `styles/treatments/`.

Treatments may define restrained palette, insignia, title typography,
cockpit-language conventions, era and role character, and limited
aircraft-specific motifs. They must not redefine document structure.

## Step 4: Select lighting

Use the guides in `styles/lighting/`. Day and night variants should retain
identical content, section order, page count, and recognizable artifact
identity.

## Step 5: Record the aircraft profile

Create `aircraft-profiles/<aircraft>.yaml`:

```yaml
aircraft: Example Aircraft
module: ExampleModule
artifact_statement: A concise physical-document description.
design:
  archetype: squadron-sortie-card
  treatment: example-treatment
  lighting: [paper-day, low-glare-night]
formats: [normal-checklist, reference-tables]
```

## Review Questions

- Is the artifact recognizable without relying on national flag colors?
- Does the treatment support rather than replace the archetype?
- Is the header/frame motif distinct for a functional reason?
- Can related aircraft share most of this profile without forced novelty?
- Does the night version still resemble the same physical object?
