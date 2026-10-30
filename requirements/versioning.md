# Requirements: Versioning & History

## Options

### Option A: Semantic versioning per requirement + git history (Recommended)
- **Description**: Each requirement has version (1.0, 1.1); changes bump minor/major; git tracks full history.
- **Pros**: Precise change tracking, rollback possible.
- **Cons**: Version bookkeeping.
- **Best for**: All projects.

### Option B: Document-level versioning only
- **Description**: Single version for whole spec.
- **Pros**: Simpler.
- **Cons**: Coarse; hard to track individual changes.
- **Best for**: Small specs.

## Recommendation
Option A for individual requirements; document-level baseline versions too.

## Rules
- Version each requirement; bump on change.
- Baseline approved requirement sets (e.g., v1.0 spec).
- Keep changelog per requirement (date, author, reason).
- Use git tags for spec baselines.
- Never edit history; append changes.
