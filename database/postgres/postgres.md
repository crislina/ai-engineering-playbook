# PostgreSQL

## Purpose

Capture PostgreSQL-specific guidance.

## JSONB

- Use JSONB for flexible, semi-structured data when relational querying is not central.
- Do not use JSONB to avoid modeling important domain concepts.
- Index JSONB fields intentionally when querying them.
- Document why JSONB is used when it affects long-term schema evolution.

## Concurrency

- Use version columns or explicit locking when concurrent updates matter.
- Make conflict behavior visible through API errors.
