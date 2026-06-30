# Docker

## Purpose

Guide container packaging decisions.

## Rules

- Keep images small and reproducible.
- Use explicit base image versions.
- Avoid baking secrets into images.
- Run as a non-root user when practical.
- Separate build-time and runtime dependencies.
- Keep container health checks meaningful.
