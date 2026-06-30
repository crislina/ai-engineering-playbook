# Component Design

Load when creating or changing reusable UI.

- Give each component one clear responsibility and a stable public API.
- Prefer composition to option-heavy components; extract only for real reuse or isolation.
- Keep domain behavior out of generic primitives.
- Support states the workflow can reach: loading, empty, error, disabled, focused, and submitted.
- Preserve stable dimensions where dynamic content could shift controls or data views.
- Interactive overlays must manage focus, keyboard dismissal, and return focus.
