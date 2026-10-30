# Gradle Best Practices: Performance

## Options

### Option A: Caching + configuration cache + parallel (Recommended)
- **Description**: Enable build cache, configuration cache, parallel execution, daemon.
- **Pros**: Dramatically faster builds.
- **Cons**: Some plugins incompatible with config cache.
- **Best for**: All projects.

### Option B: Defaults
- **Description**: No tuning.
- **Pros**: Simple.
- **Cons**: Slow.
- **Best for**: Avoid.

## Recommendation
Option A. Fix config-cache incompatibilities.

## Rules
- `org.gradle.caching=true`
- `org.gradle.configuration-cache=true`
- `org.gradle.parallel=true`
- Use remote build cache in CI.
- Avoid dynamic versions.
- Profile with `--profile` / build scans.
- Keep build scripts lean.
