# Testing Strategy: Final Decisions

Default rules to follow unless explicitly overridden.

## Test Pyramid
- **Decision**: Pyramid (many unit, fewer integration, few E2E) (Option A)

## Contract Testing
- **Decision**: Pact for multi-service; skip for monoliths

## Performance Testing
- **Decision**: Baseline + load tests before releases in staging

## Mutation Testing
- **Decision**: Run on critical code/core logic (Option A)

## Test Data
- **Decision**: Factories/builders, deterministic, anonymized
