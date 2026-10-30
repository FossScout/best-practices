# Kotlin Best Practices: Testing

## Options

### Option A: JUnit5 + MockK + Testcontainers + Kotest (Recommended)
- **Description**: JUnit5 platform, MockK for mocking, Testcontainers for integration, Kotest for assertions (or standard).
- **Pros**: Rich ecosystem, coroutine support, real DB tests.
- **Cons**: Slower integration tests.
- **Best for**: Most projects.

### Option B: JUnit4 + Mockito
- **Description**: Legacy stack.
- **Pros**: Familiar.
- **Cons**: Less Kotlin-friendly.
- **Best for**: Legacy migration.

## Recommendation
Option A. Prefer fakes over mocks where feasible.

## Rules
- Name tests descriptively: `should X when Y`.
- Use `runTest` for coroutines.
- Integration tests with Testcontainers; tag with `@Tag("integration")`.
- Aim for meaningful coverage; don't chase 100%.
- Test edge cases and null paths.
- Use `@TempDir` for filesystem tests.
- Keep unit tests fast and deterministic.
