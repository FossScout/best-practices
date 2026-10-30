# Docker Best Practices: Image Build

## Options

### Option A: Multi-stage, minimal base, non-root runtime (Recommended)
- **Description**: Multi-stage build; final stage uses slim/distroless base; run as non-root UID/GID.
- **Pros**: Small images, fast pulls, reduced attack surface, rootless-friendly.
- **Cons**: More complex Dockerfile; debugging needs tooling stage.
- **Best for**: Most production images.

### Option B: Single-stage full base
- **Description**: One stage on full OS base.
- **Pros**: Simple, easy debug.
- **Cons**: Large image, more CVEs, root by default.
- **Best for**: Dev-only or quick prototypes.

## Recommendation
Option A. Use `USER` directive with numeric UID/GID for podman/rootless compatibility.

## Rules
- Pin base image by digest or exact tag; avoid `latest`.
- Use `.dockerignore` (exclude .git, node_modules, secrets).
- Order layers: deps before source for cache.
- No secrets in layers; use build secrets (`--secret`).
- One process per container; use `exec` form CMD.
- Prefer distroless/slim for runtime; keep build tools in builder stage.
- Set `HEALTHCHECK` when a probe endpoint exists.
