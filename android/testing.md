# Android Best Practices: Testing

## Options

### Option A: Unit tests (JUnit) + instrumented (Espresso/Compose) + Hilt testing (Recommended)
- **Description**: Fast unit tests for logic; Compose UI tests for screens; Hilt for DI in tests.
- **Pros**: Comprehensive, realistic.
- **Cons**: Instrumented tests slow.
- **Best for**: Production apps.

### Option B: Unit tests only
- **Description**: Logic only.
- **Pros**: Fast.
- **Cons**: Misses UI/integration regressions.
- **Best for**: Libraries.

## Recommendation
Option A. Keep instrumented tests focused on critical flows.

## Rules
- Test ViewModels with Turbine for flows.
- Use Robolectric for faster unit tests when possible.
- Fake repositories; avoid mocking everything.
- Run tests in CI on emulator (or managed devices).
- Keep tests deterministic (no real network/time).
- Aim for meaningful coverage on critical paths.
