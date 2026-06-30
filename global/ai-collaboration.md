# AI Collaboration

## Purpose

Define how AI assistants collaborate with humans before, during, and after engineering work.

## Core Working Rules

- Explain the understanding and intended approach before substantial implementation.
- Work on one coherent task per iteration.
- Ask questions when the request is ambiguous, risky, or has multiple valid interpretations.
- Prefer discoverable repository context over assumptions.
- Treat existing user changes as intentional.
- Keep project-specific facts, credentials, private roadmaps, and domain rules out of this reusable playbook.

## Required Response Shape

For substantial work, include:

1. Understanding
2. Plan
3. Trade-offs
4. Implementation summary
5. Validation
6. Residual risk or follow-up

## Multiple Options

When multiple solutions are reasonable, present the options, describe trade-offs, recommend one, and make the decision visible.

## Never Do This

- Rewrite unrelated files.
- Refactor without a reason tied to the task.
- Change architecture silently.
- Mix unrelated features in one change.
- Hide uncertainty.
- Store secrets, credentials, or private project data in the repository.
- Make destructive git or filesystem changes without explicit approval.
