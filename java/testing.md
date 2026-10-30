# Java Best Practices: Testing

## Options

### Option A: JUnit5 + Mockito + Testcontainers (Recommended)
- **Description**: JUnit5 platform, Mockito for mocking, Testcontainers for integration.
- **Pros**: Mature ecosystem, realistic integration tests.
- **Cons**: Slower integration tests.
- **Best for**: Most projects.

### Option B: JUnit4 + in-memory fakes
- **Description**: Legacy.
- **Pros**: Fast.
- **Cons**: Less modern tooling.
- **Best for**: Legacy.

## Recommendation
Option A.

## Rules
- Use JUnit5 (Jupiter) annotations.
- Prefer fakes over mocks where feasible.
- Integration tests with Testcontainers; tag separately.
- Use AssertJ for assertions.
- Keep unit tests fast and deterministic.
- Run in CI with coverage gate.
