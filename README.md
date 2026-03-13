# AGE Bootstrap Toolkit

![AGE Bootstrap Toolkit logo](./assets/age-toolkit-logo.svg)

This is a Bootstrap-style frontend CSS toolkit for command-center and sci-fi dashboard interfaces.

The visual direction is inspired by the system UI seen in the anime "Gundam AGE".

## Live demo

[https://badleo.github.io/age-bootstrap-toolkit/](https://badleo.github.io/age-bootstrap-toolkit/)

## Repository structure

```text
.
├─ index.html
├─ README.md
├─ CONTRIBUTING.md
├─ LICENSE
├─ assets/
│  └─ age-toolkit-logo.svg
├─ styles/
│  └─ age-bootstrap.css
├─ docs/
│  └─ cookbook.html
└─ .github/
   └─ workflows/
      └─ pages.yml
```

## Files

- `index.html`: demo page showing the design language and core components.
- `docs/cookbook.html`: cookbook-style documentation page with rendered examples and code snippets.
- `styles/age-bootstrap.css`: theme tokens, responsive grid, utilities, and component styles.

## Core features

- Bootstrap-format layout classes: `container`, `container-fluid`, `row`, and `col-*`.
- Reusable UI surfaces: `panel`, `card`, `well`, `terminal`, `stat`, `badge`, `table`.
- Form primitives: `form-control`, `form-select`, `form-textarea`, `input-group`, `btn`.
- Theme tokens via `:root` CSS variables for palette, spacing, radii, and shadows.
- Publish-safe demo and cookbook pages using toolkit-native sample blocks.

## Contributing and license

- Contribution guidelines: `CONTRIBUTING.md`
- License: `LICENSE` (MIT)

## Extending it

Override the `:root` variables in `styles/age-bootstrap.css` to create variants without changing the component API. New modules should compose the existing surfaces and utility classes rather than introducing one-off styling patterns.
