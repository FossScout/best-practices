# Testing Strategy: Contract Testing

## Options

### Option A: Pact consumer-driven contracts (Recommended)
- **Description**: Consumers define expectations; providers verify.
- **Pros**: Catches breaking changes early; decouples teams.
- **Cons**: Setup and maintenance.
- **Best for**: Microservices.

## Recommendation
Option A for multi-service; skip for monoliths.

## Rules
- Publish contracts to broker.
- Verify providers in CI.
- Version contracts.
- Test on every PR.
