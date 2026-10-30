# Python Best Practices: Testing

## Options

### Option A: pytest + fixtures + coverage (Recommended)
- **Description**: pytest with fixtures, parametrize, coverage reporting.
- **Pros**: Powerful, readable, ecosystem.
- **Cons**: Fixture complexity.
- **Best for**: All projects.

### Option B: unittest
- **Description**: Stdlib.
- **Pros**: No deps.
- **Cons**: Verbose.
- **Best for**: Libraries avoiding deps.

## Recommendation
Option A.

## Rules
- Tests in `tests/` mirroring src.
- Use fixtures for setup; parametrize for cases.
- Aim for meaningful coverage (not 100%).
- Mock external services (responses/pytest-mock).
- Keep tests fast and isolated.
- Run in CI with coverage gate.
