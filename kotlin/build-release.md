# Kotlin Best Practices: Build & Release

## Options

### Option A: Gradle with caching, Docker image, semantic versioning (Recommended)
- **Description**: Gradle build cache + remote cache, containerize with jib or Dockerfile, version via git tags.
- **Pros**: Fast builds, reproducible artifacts, consistent deploy.
- **Cons**: Setup effort.
- **Best for**: Production.

### Option B: Manual builds
- **Description**: Ad hoc.
- **Pros**: Simple.
- **Cons**: Inconsistent, slow.
- **Best for**: Avoid.

## Recommendation
Option A. Use Jib or multi-stage Dockerfile; cache Gradle.

## Rules
- Enable Gradle build cache and configuration cache.
- Pin Gradle and Kotlin versions.
- Build container image in CI; scan for CVEs.
- Version from git tag (SemVer).
- Publish artifacts to registry (Maven Central/internal).
- Run lint + tests + detekt in CI before release.
- Keep release notes from Conventional Commits.
