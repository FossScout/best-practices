# Requirements: Traceability

## Options

### Option A: Bidirectional traceability matrix (Recommended)
- **Description**: Link requirements <-> design <-> code <-> tests <-> releases.
- **Pros**: Impact analysis, coverage visibility.
- **Cons**: Maintenance overhead.
- **Best for**: Regulated/complex systems.

### Option B: Lightweight linking via IDs in commits/PRs
- **Description**: Reference REQ IDs in commits and tests.
- **Pros**: Low overhead.
- **Cons**: Less formal.
- **Best for**: Agile teams.

## Recommendation
Option B minimum; Option A for regulated.

## Rules
- Reference REQ IDs in commits, PRs, tests.
- Maintain traceability matrix for regulated projects.
- Verify coverage in CI (all reqs have tests).
- Update links on requirement changes.
