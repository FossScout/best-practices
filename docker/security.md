# Docker Best Practices: Security

## Options

### Option A: Rootless, scanned, least-privilege (Recommended)
- **Description**: Run containers rootless (podman default / docker rootless); drop capabilities; read-only root fs; scan images.
- **Pros**: Strong isolation, fewer CVE impact, compliance-friendly.
- **Cons**: Some apps need root; volume permission handling.
- **Best for**: Production and shared hosts.

### Option B: Standard docker with hardening
- **Description**: Non-root USER but daemon root.
- **Pros**: Easier; broad compatibility.
- **Cons**: Daemon root risk remains.
- **Best for**: Dev and trusted environments.

## Recommendation
Option A for production; Option B acceptable for dev. Always set `USER`, drop caps, read-only root fs where feasible.

## Rules
- Run as non-root (numeric UID/GID for podman).
- `--cap-drop=ALL`, add back only needed caps.
- Read-only root filesystem: `read_only: true` + tmpfs for writable paths.
- No secrets in images/env files committed; use docker secrets or external secret manager.
- Scan images in CI (trivy/grype).
- Pin and update base images regularly.
- Avoid `privileged: true`; avoid mounting docker socket unless necessary.
- Use `no-new-privileges:true`.
