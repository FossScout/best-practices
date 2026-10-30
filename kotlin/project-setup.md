# Kotlin Best Practices: Project Setup

## Options

### Option A: Gradle Kotlin DSL + version catalog + multi-module (Recommended)
- **Description**: `build.gradle.kts`, `libs.versions.toml`, modular structure.
- **Pros**: Type-safe builds, centralized versions, scalable.
- **Cons**: Slower initial setup, learning curve.
- **Best for**: Most projects.

### Option B: Groovy DSL single-module
- **Description**: Traditional `build.gradle`.
- **Pros**: Simpler, familiar.
- **Cons**: No type safety, harder to maintain at scale.
- **Best for**: Small/legacy projects.

## Recommendation
Option A. Use version catalogs and convention plugins for shared config.

## Rules
- Use Kotlin DSL; centralize versions in `libs.versions.toml`.
- Prefer multi-module: `:core`, `:api`, `:app`.
- Apply convention plugins for common config (lint, test, jvm target).
- Set `jvmTarget` consistently (e.g., 17 or 21).
- Enable `org.gradle.parallel` and caching.
- Keep `gradle-wrapper.properties` pinned.
