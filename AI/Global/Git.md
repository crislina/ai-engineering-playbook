# Git

## Purpose

Define practical source-control habits for this repository.

## Branching

- Keep branches focused on one coherent change.
- Use descriptive branch names.
- Prefer prefixes such as `feature/`, `fix/`, `refactor/`, `docs/`, `test/`, and `chore/`.
- Example: `feature/template-approval-workflow`.
- Avoid mixing formatting-only changes with behavior changes.

## Commits

- Use Conventional Commit format.
- One feature equals one commit whenever practical.
- Group related edits together.
- Do not mix refactor with feature work unless the refactor is required for that feature and approved.
- Do not commit generated files unless they are intended project artifacts.

## Conventional Commit Examples

- `feat: add template approval workflow`
- `fix: handle missing placeholder values`
- `docs: update API behavior rules`
- `test: add regression coverage for renewal flow`
- `refactor: extract template mapping service`

## Commit Message Rules

- Use the imperative mood.
- Keep the subject concise.
- Explain why in the body when the change is not obvious.
- Mention migrations, breaking changes, or manual steps.

## Pull Requests

- Summarize intent, key changes, and validation.
- Link related issues or decisions.
- Call out breaking changes, migrations, and known risks.
