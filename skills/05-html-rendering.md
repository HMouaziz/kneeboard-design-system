# Skill: HTML Rendering

## Goal

Render a kneeboard page using semantic HTML classes so that style guides can control the visual appearance.

## Required structure

```html
<main class="kb-page kb-style-ww2-day kb-format-normal">
  <header class="kb-header">
    <div class="kb-title">Fw 190 A-8</div>
    <div class="kb-subtitle">Anton</div>
    <div class="kb-mode">Day</div>
  </header>

  <section class="kb-section kb-section-engine-start">
    <h2 class="kb-section-title">Engine Start</h2>
    <div class="kb-row kb-critical">
      <span class="kb-label">Starter</span>
      <span class="kb-leader"></span>
      <span class="kb-value">Clutch / Pull</span>
    </div>
    <p class="kb-note">When engine kicks in.</p>
  </section>

  <footer class="kb-footer">
    <span>Page 1</span>
  </footer>
</main>
```

## Semantic classes

Use classes for meaning, not appearance:

```txt
kb-page
kb-header
kb-title
kb-subtitle
kb-mode
kb-section
kb-section-title
kb-row
kb-label
kb-leader
kb-value
kb-note
kb-condition
kb-table
kb-diagram
kb-footer
```

State classes:

```txt
kb-muted
kb-optional
kb-critical
kb-warning
kb-caution
kb-dcs-specific
```

Format classes:

```txt
kb-format-normal
kb-format-combat-fence
kb-format-weapons
kb-format-sensors
kb-format-navigation
kb-format-carrier
kb-format-engine-management
kb-format-emergency
kb-format-reference
kb-format-cockpit-controls
kb-format-mission-data
```

Style classes:

```txt
kb-style-ww2-day
kb-style-ww2-night
kb-style-cold-war-day
kb-style-cold-war-night
kb-style-modern-day
kb-style-modern-night
```

## Rendering rules

- Keep page HTML semantic and flat where possible.
- Avoid inline styles unless doing a one-off diagram.
- Avoid absolute positioning for normal checklist text.
- Use CSS variables for colors, spacing, and font settings.
- Prefer CSS grid/flex for rows and columns.
- A page may use one or two content columns, but should not require horizontal scrolling.
- Tables must remain readable when exported to PNG.

## Critical visual rule

The same content should render correctly in every style.

For example:

```html
<div class="kb-row kb-critical">...</div>
```

- WW2 Day may make it yellow.
- WW2 Night may make it dim amber.
- Cold War Day may use a boxed caution strip.
- Modern Day may use a high-contrast accent chip.
- Modern Night may use an amber outline or side marker.

The content should never say `yellow`.
