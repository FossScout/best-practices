# Docker Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Image Build
- **Decision**: Multi-stage, minimal base, non-root runtime (Option A)
- Pin base images, use `.dockerignore`, no secrets in layers, exec-form CMD.

## Compose Orchestration
- **Decision**: Compose v2 with profiles + healthchecks (Option A)
- File named `compose.yaml`; `depends_on: condition: service_healthy`.

## Volumes & Persistence
- **Decision**: Named volumes for data, bind mounts for config/dev (Option A)
- Config read-only; podman-compatible paths; non-root writable dirs.

## Networking
- **Decision**: Default network; publish only edge ports (Option A)
- Internal services use service names; no DB ports published in prod.

## Security
- **Decision**: Rootless, scanned, least-privilege (Option A)
- Non-root numeric UID, drop caps, read-only root fs, scan in CI.

## SBOM
- **Decision**: Generate SBOM at build time with syft (Option A)
- Attach as attestation, sign with cosign, scan in CI.

## Dependency License Check
- **Decision**: Automated license scan in CI (Option A)
- Allow-list policy; fail build on disallowed licenses; include transitive deps.

## Image Registry & Tagging
- **Decision**: Immutable tags + semver + digest promotion (Option A)
- Never overwrite tags; promote by digest; sign before prod push.

## Secrets Management
- **Decision**: External secret manager + runtime injection (Option A)
- No secrets in images/git; use build secrets; `.env.example` placeholders.

## Resource Limits & Observability
- **Decision**: Explicit limits + structured logs + health/metrics (Option A)
- Set mem/cpu limits, log rotation, healthchecks, JSON logs.

## Multi-Arch Builds
- **Decision**: buildx with QEMU + manifest lists (Option A)
- Declare platforms explicitly; prefer native runners in CI.

## Dev vs Prod
- **Decision**: Compose overrides + build targets (Option A)
- Dev auto-override; prod via explicit `-f` files; resource limits in prod.
