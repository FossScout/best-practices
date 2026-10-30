# Gradle Best Practices: Version Catalogs

## Options

### Option A: libs.versions.toml (Recommended)
- **Description**: Centralized dependency versions in TOML catalog.
- **Pros**: Single source, IDE support, type-safe accessors.
- **Cons**: Migration effort.
- **Best for**: All projects.

### Option B: ext properties / variables
- **Description**: Define versions in build.gradle.
- **Pros**: Simple.
- **Cons**: Less tooling support.
- **Best for**: Small/legacy.

## Recommendation
Option A.

## Rules
- Define versions in `gradle/libs.versions.toml`.
- Use bundles for related deps.
- Pin versions; avoid dynamic (`+`, `latest.release`).
- Update via Renovate/Dependabot.
- Group platform BOMs where applicable.
