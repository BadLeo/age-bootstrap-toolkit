# Contributing

## Scope

This repository contains a static frontend CSS toolkit and demo pages. Keep
changes aligned with the existing AGE visual system and class naming.

## Setup

No build step is required. Open `index.html` directly in a browser, or serve
the repository root with a simple static file server.

Example:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## Guidelines

- Reuse existing toolkit classes before adding new CSS.
- Extend `styles/age-bootstrap.css` with reusable primitives, not one-off page
  rules.
- Keep demo content publish-safe and self-contained.
- Preserve relative links so the site works on GitHub Pages.

## Pull Requests

- Describe the user-facing or developer-facing change clearly.
- Include screenshots for visual changes when practical.
- Mention any browser testing or manual verification performed.

