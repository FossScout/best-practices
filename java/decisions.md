# Java Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Project Setup
- **Decision**: Maven/Gradle + modules + LTS JDK (Option A)

## Code Style
- **Decision**: Spotless + Checkstyle + modern Java (Option A)

## Concurrency
- **Decision**: Virtual threads on Java 21+ (Option A); platform pools otherwise

## Testing
- **Decision**: JUnit5 + Mockito + Testcontainers (Option A)

## Build & Release
- **Decision**: Gradle/Maven + container image + SemVer (Option A)
