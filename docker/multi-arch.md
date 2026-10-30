# Docker Best Practices: Multi-Arch Builds

## Options

### Option A: buildx with QEMU + manifest lists (Recommended)
- **Description**: Use `docker buildx` with multi-platform (`linux/amd64,linux/arm64`); publish manifest list.
- **Pros**: Single tag serves multiple arches; supports ARM hosts (Apple Silicon, Graviton).
- **Cons**: QEMU slow for heavy builds; emulation quirks.
- **Best for**: Published libraries/services.

### Option B: Separate per-arch tags
- **Description**: Build each arch separately with arch suffix.
- **Pros**: Faster native builds.
- **Cons**: Consumer must pick arch; more tags.
- **Best for**: Internal/perf-critical builds.

## Recommendation
Option A for published images; use native runners in CI for speed when possible.

## Rules
- Declare platforms explicitly: `--platform linux/amd64,linux/arm64`.
- Test on target arch in CI (native runner preferred).
- Avoid arch-specific base images; use multi-arch bases.
- Document supported platforms in README.
- Cache per-platform layers in registry cache.
