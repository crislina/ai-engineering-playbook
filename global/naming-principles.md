# Naming Principles

## Purpose

Keep code and documentation vocabulary clear, consistent, and domain-aware.

## Rules

- Names should describe responsibility or intent.
- Class and type names should usually use nouns.
- Method and function names should use verbs or verb phrases.
- Boolean names should read like predicates, such as `isActive`, `hasPermission`, or `shouldRetry`.
- Avoid vague names such as `data`, `info`, `manager`, `helper`, or `util` unless the meaning is obvious.
- Prefer domain vocabulary over implementation vocabulary.
- Avoid leaking database column names into API names when they are not domain terms.
