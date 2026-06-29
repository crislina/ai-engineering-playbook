# UI Principles

## Purpose

Guide frontend experience and interface decisions.

## Overall Style

- Enterprise.
- Minimal.
- Responsive.
- Consistent.
- Accessible.
- Practical over decorative.
- Clear hierarchy over visual noise.

## Required UI Workflow

AI must not jump directly into React implementation for meaningful UI work.

1. Design
   - Understand users, tasks, data density, and constraints.
   - Identify reusable components before page composition.

2. Wireframe
   - Show structure, layout, and interaction flow.
   - Keep it low-fidelity and easy to change.

3. Mockup
   - Show visual treatment, states, and responsive behavior.
   - Include empty, loading, error, and success states when relevant.

4. Approval
   - Wait for approval before implementation.
   - Present trade-offs when multiple UI directions are possible.

5. Implementation
   - Build approved components first.
   - Compose pages from reusable components.

## Design Principles

- Make primary workflows obvious and efficient.
- Use consistent spacing, typography, and interaction patterns.
- Prefer accessible controls with clear states.
- Design for loading, empty, error, and success states.
- Keep visual hierarchy aligned with user intent.

## Component-First Rule

- Design reusable components before pages.
- Build components with clear props and states.
- Avoid one-off page-only components unless reuse is unlikely.
- Prefer composition over large configurable components.

## Accessibility

- Use semantic HTML when possible.
- Ensure keyboard navigation works for interactive elements.
- Maintain sufficient color contrast.
- Provide useful labels for form controls and icon buttons.
