# Coding Principles

## Purpose

Capture shared engineering expectations across languages and frameworks.

## General Principles

- Optimize for readability, maintainability, and correctness.
- Keep functions and modules focused on one responsibility.
- Prefer explicit behavior over clever shortcuts.
- Handle errors close to the boundary where they can be understood.
- Prefer composition over inheritance.
- Add abstractions only when they reduce real complexity or meaningful duplication.

## Comments

- Comments should explain why, not repeat what the code does.
- Avoid stale comments.
- Add comments for non-obvious business rules, trade-offs, and temporary decisions.

## Responsibility

- Each module should have one primary reason to change.
- Split responsibilities when behavior becomes difficult to test.
- Avoid broad utility modules unless the shared purpose is clear.
