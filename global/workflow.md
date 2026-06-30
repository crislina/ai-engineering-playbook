# Workflow

## Purpose

Define a reusable workflow for AI-assisted engineering work.

## Required Flow

1. Read relevant playbook files.
2. Understand the request, affected scope, and expected result.
3. Identify ambiguity, risk, and dependencies.
4. Plan the smallest useful change.
5. Implement only the agreed or clearly requested scope.
6. Run the smallest meaningful validation first.
7. Broaden validation when shared behavior or critical paths are touched.
8. Summarize what changed, what was validated, and what remains risky.

## Working Rules

- Preserve existing project style unless there is an explicit reason to change it.
- Keep unrelated cleanup out of focused tasks.
- Surface blockers early with concrete options.
- Make assumptions visible.
- Prefer incremental, reviewable changes.

## Definition of Done

- The requested change is implemented or the limitation is clearly documented.
- Relevant validation has run, or the reason it could not run is stated.
- The final response names changed files and follow-up risks.
