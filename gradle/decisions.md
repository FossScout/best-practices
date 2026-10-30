# Gradle Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Convention Plugins
- **Decision**: Convention plugins in buildSrc/included build (Option A)
- Focused plugins; apply by ID.

## Performance
- **Decision**: Caching + config cache + parallel (Option A)
- Enable all; fix incompatibilities.

## Version Catalogs
- **Decision**: libs.versions.toml (Option A)
- Pin versions; update via bots.

## Publishing
- **Decision**: Maven Central/internal with signing (Option A)
- Automate on tag; sign artifacts.
