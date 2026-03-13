---
name: age-bootstrap-toolkit
description: Use when building, editing, or documenting frontend UI in this repository with the AGE Bootstrap Toolkit. Trigger for new pages, components, dashboards, forms, or layout updates that should follow the existing sci-fi Bootstrap-style CSS system instead of introducing a separate design language.
---

# AGE Bootstrap Toolkit

Use this skill for frontend work in this repo when the output should match the existing AGE visual system.

## First reads

Read only what you need, in this order:

1. `styles/age-bootstrap.css`
2. `docs/cookbook.html`
3. `index.html`

The stylesheet defines the API. The cookbook shows the intended patterns and code samples. The demo page shows how the pieces combine into a full layout.

## Goal

Build UI using the existing toolkit rather than inventing parallel styling.

The visual language is:

- deep navy / cobalt backgrounds
- electric cyan structural lines
- warning yellow and magenta-red for emphasis
- rounded futuristic panels
- uppercase display typography
- dense dashboard-style composition

## Default workflow

1. Inspect the current page or markup target.
2. Reuse toolkit classes before adding new CSS.
3. Compose layouts with `container`, `container-fluid`, `row`, and `col-*`.
4. Use existing surfaces like `panel`, `card`, `well`, `terminal`, and `stat`.
5. Use cookbook patterns as the default source for code structure.
6. Add CSS only when the toolkit genuinely lacks the needed primitive.
7. If adding CSS, extend the system in `styles/age-bootstrap.css` with reusable classes, not one-off inline styling.

## Preferred class map

Use these classes by default:

- Page shell: `age-shell`
- Top navigation: `navbar`, `navbar-inner`, `navbar-brand`, `nav`, `nav-link`
- Hero section: `hero`, `hero-radar`, `eyebrow`, `display-title`, `lead`
- Surfaces: `panel`, `panel-header`, `panel-body`, `card`, `card-header`, `card-body`, `well`, `terminal`
- Data: `table`, `progress`, `progress-bar`, `timeline`, `timeline-item`
- Status: `status-list`, `status-item`, `status-cluster`, `status-dot`
- Metrics: `kpi-grid`, `stat`, `stat-label`, `stat-kpi`, `stat-trend`
- Actions: `btn`, `btn-primary`, `btn-warning`, `btn-outline`, `badge`, `badge-success`, `badge-warning`, `badge-danger`
- Forms: `form-label`, `form-control`, `form-select`, `form-textarea`, `input-group`
- Media/docs: `gallery`, `sample-shot`, `code-block`
- Utilities: `d-flex`, `d-grid`, `align-items-center`, `justify-content-between`, `gap-*`, `mt-*`, `mb-*`, `text-*`, `w-100`

## Guardrails

- Do not add a second design system.
- Do not replace the toolkit with Tailwind, raw Bootstrap, or ad hoc utility naming.
- Do not introduce random colors outside the existing palette unless the user explicitly asks.
- Do not use inline styles for normal styling unless it is a tiny demo-only override.
- Do not create component-specific CSS if an existing toolkit class already fits.
- Keep the sci-fi tone intentional; avoid generic SaaS styling.

## When adding new CSS

Only extend `styles/age-bootstrap.css` if:

- multiple screens or components will reuse the pattern
- the missing style is clearly part of the design system
- the new class name fits the current naming approach

When you extend the toolkit:

- prefer token-driven values via `:root` variables
- keep names readable and consistent
- support mobile behavior
- verify decorative pseudo-elements do not block interaction

## Validation

After UI edits:

1. Open the page in a browser when feasible.
2. Confirm links and buttons remain clickable.
3. Check mobile stacking for `row` / `col-*` layouts.
4. Verify new sections still look coherent beside existing `panel` and `hero` patterns.

## Snippet pattern

Use this as the default skeleton for new dashboard sections:

```html
<section class="panel">
  <div class="panel-header">
    <div>
      <div class="meta-label">Section Label</div>
      <h2 class="section-title">Section Title</h2>
    </div>
    <span class="badge">Live</span>
  </div>
  <div class="panel-body">
    <!-- content -->
  </div>
</section>
```

For forms:

```html
<label class="form-label" for="field">Field</label>
<input class="form-control" id="field" />
```

For actions:

```html
<div class="input-group">
  <button class="btn btn-primary">Primary</button>
  <button class="btn btn-outline">Secondary</button>
</div>
```
