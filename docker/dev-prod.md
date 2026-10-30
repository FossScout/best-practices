# Docker Best Practices: Dev vs Prod

## Options

### Option A: Compose overrides + build targets (Recommended)
- **Description**: Base `compose.yaml` + `compose.override.yaml` (auto-loaded for dev) with bind mounts and debug; prod uses explicit `-f compose.yaml -f compose.prod.yaml`.
- **Pros**: Single source of truth, clear overrides, reproducible prod.
- **Cons**: Override auto-load can surprise in CI.
- **Best for**: Most teams.

### Option B: Separate files per environment
- **Description**: `compose.dev.yaml`, `compose.prod.yaml`.
- **Pros**: Explicit, no auto-load surprises.
- **Cons**: Duplication.
- **Best for**: Teams preferring explicitness.

## Recommendation
Option A with explicit prod command; disable auto-override in CI via `COMPOSE_FILE`.

## Rules
- Dev: bind-mount source, hot reload, debug ports, verbose logs.
- Prod: pinned images, no bind mounts for source, healthchecks, resource limits.
- Use multi-stage build targets: `target: dev` vs `target: prod`.
- Set resource limits (`mem_limit`, `cpus`) in prod.
- Don't run dev tools (nodemon, debuggers) in prod image.
- Keep `.env.example` committed; `.env` gitignored.
