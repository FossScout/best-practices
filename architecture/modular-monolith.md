# Architecture Best Practices: Modular Monolith

## Options

### Option A: Modular monolith (Recommended default)
- **Description**: Single deployable with strict module boundaries.
- **Pros**: Simpler ops, strong boundaries, easy refactor to services later.
- **Cons**: Shared DB risk if not disciplined.
- **Best for**: Most teams.

## Recommendation
Option A. Start here; split to services only when needed.

## Rules
- Enforce module boundaries (ArchUnit/Deptrac).
- Each module owns its data.
- No cross-module DB access.
- Clear public APIs between modules.
