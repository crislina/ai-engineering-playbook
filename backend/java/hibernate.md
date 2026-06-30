# Hibernate

## Purpose

Guide Hibernate-specific persistence decisions.

## Rules

- Understand lazy loading boundaries before returning data from services.
- Avoid relying on open-session-in-view for business correctness.
- Use batching and fetch joins intentionally.
- Keep entity equality and hash code behavior stable.
- Review generated SQL for important paths.
