# Docker Best Practices: Compose Orchestration

## Options

### Option A: Compose v2 with profiles and healthchecks (Recommended)
- **Description**: `compose.yaml` (canonical name) with services, healthchecks, `depends_on` with condition, profiles for optional services.
- **Pros**: Standard, readable, supports `docker compose` and `podman compose`.
- **Cons**: Profile complexity grows; need discipline.
- **Best for**: Most multi-service stacks.

### Option B: Multiple compose files merged
- **Description**: base + override files (`compose.override.yaml`).
- **Pros**: Clean dev/prod separation.
- **Cons**: Merge semantics can surprise.
- **Best for**: Dev/prod parity needs.

## Recommendation
Use `compose.yaml` as base + `compose.override.yaml` for dev; profiles for optional services. Healthchecks on all services.

## Rules
- File name `compose.yaml` (preferred over docker-compose.yml).
- Always define `healthcheck` for services others depend on.
- Use `depends_on: condition: service_healthy`.
- Prefer environment files (`.env`) but never commit secrets; use `.env.example`.
- Use named volumes for persistent data; bind mounts for dev source.
- Set `restart: unless-stopped` for long-running services.
- Keep one compose file per stack; avoid giant monoliths.
