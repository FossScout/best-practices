# Kotlin Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Project Setup
- **Decision**: Gradle Kotlin DSL + version catalog + multi-module (Option A)
- Convention plugins; pinned JVM target; cached builds.

## Code Style & Idioms
- **Decision**: Idiomatic Kotlin with ktlint/detekt (Option A)
- Prefer val, data classes, null safety; enforce in CI.

## Coroutines & Concurrency
- **Decision**: Structured concurrency (Option A)
- No GlobalScope; appropriate dispatchers; Flow for streams.

## Testing
- **Decision**: JUnit5 + MockK + Testcontainers (Option A)
- runTest for coroutines; prefer fakes; fast unit tests.

## Architecture
- **Decision**: Clean Architecture + DI + modules (Option A)
- Domain framework-free; use cases; UDF.

## Build & Release
- **Decision**: Gradle caching + container image + SemVer (Option A)
- CI gates: lint, tests, detekt; scan images.
