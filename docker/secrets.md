# Docker Best Practices: Secrets Management

## Options

### Option A: External secret manager + runtime injection (Recommended)
- **Description**: Store secrets in vault (Doppler, AWS SM, etc.); inject at runtime via env or mounted files; never bake into image.
- **Pros**: Centralized, rotatable, auditable.
- **Cons**: Infra dependency, setup cost.
- **Best for**: Production.

### Option B: Docker secrets / compose secrets
- **Description**: Use compose `secrets:` with files.
- **Pros**: Simple, built-in, file-based.
- **Cons**: Swarm-oriented; limited rotation tooling.
- **Best for**: Single-host / small stacks.

## Recommendation
Option A for prod; Option B acceptable for single-host. Never commit `.env` with real secrets.

## Rules
- No secrets in image layers or git.
- Use build secrets (`--secret`) only for build-time needs.
- Mount secrets read-only; restrict permissions (0400).
- Rotate on suspected exposure.
- Redact secrets in logs.
- Use `.env.example` with placeholders.
