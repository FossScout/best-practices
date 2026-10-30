# Java Best Practices: Build & Release

## Options

### Option A: Gradle/Maven + container image + SemVer (Recommended)
- **Description**: Build JAR, containerize (Jib/Dockerfile), version from git tag, publish to registry.
- **Pros**: Reproducible, standard.
- **Cons**: Setup effort.
- **Best for**: Production.

### Option B: Manual builds
- **Description**: Ad hoc.
- **Pros**: Simple.
- **Cons**: Inconsistent.
- **Best for**: Avoid.

## Recommendation
Option A.

## Rules
- Build fat/uber JAR or layered image.
- Use Jib or multi-stage Dockerfile.
- Version from git tag (SemVer).
- Publish artifacts to Maven repo; image to registry.
- Scan images for CVEs.
- Run lint + tests + static analysis in CI.
