# Testing Strategy: Test Pyramid

## Options

### Option A: Pyramid (many unit, fewer integration, few E2E) (Recommended)
- **Description**: Broad unit base, integration middle, thin E2E top.
- **Pros**: Fast, cheap, reliable.
- **Cons**: Integration gaps if misapplied.
- **Best for**: Most systems.

### Option B: Trophy (more integration)
- **Description**: Kent C. Dodds model.
- **Pros**: Tests real behavior.
- **Cons**: Slower.
- **Best for**: Frontend-heavy apps.

## Recommendation
Option A default; Option B for UI apps.

## Rules
- Unit tests for logic; integration for boundaries; E2E for critical flows.
- Keep E2E suite small and stable.
- Run unit on PR; integration on merge; E2E on staging.
- Avoid testing implementation details.
