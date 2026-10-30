# Gradle Best Practices: Convention Plugins

## Options

### Option A: Convention plugins in buildSrc or included build (Recommended)
- **Description**: Shared build logic as plugins applied to modules.
- **Pros**: DRY, type-safe, centralized config.
- **Cons**: Initial setup; plugin publishing.
- **Best for**: Multi-module projects.

### Option B: Copy-paste build.gradle.kts
- **Description**: Duplicate config per module.
- **Pros**: Simple.
- **Cons**: Drift, maintenance burden.
- **Best for**: Small projects.

## Recommendation
Option A. Use included build for sharing across repos.

## Rules
- Put shared config in convention plugins.
- Keep plugins focused (jvm, android-app, android-lib).
- Apply plugins by ID in modules.
- Version plugins via version catalog.
- Avoid logic in build.gradle.kts beyond applying plugins.
