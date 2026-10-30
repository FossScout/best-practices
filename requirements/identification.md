# Requirements: Identification

## Options

### Option A: Unique ID + structured template (Recommended)
- **Description**: Each requirement gets a unique ID (REQ-XXX) with title, description, rationale, acceptance criteria, priority, owner.
- **Pros**: Traceable, searchable, auditable.
- **Cons**: Maintenance overhead.
- **Best for**: All projects needing traceability.

### Option B: Free-form notes
- **Description**: Ad hoc requirements in docs.
- **Pros**: Fast.
- **Cons**: Ambiguous, hard to track changes.
- **Best for**: Prototypes.

## Recommendation
Option A. Store in version-controlled markdown/YAML or a requirements tool.

## Rules
- Unique immutable ID per requirement.
- Include acceptance criteria and priority.
- Link to source (stakeholder, ticket).
- Keep requirements atomic (one need per item).
- Review and approve before implementation.
