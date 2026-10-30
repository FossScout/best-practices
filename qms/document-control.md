# QMS Best Practices: Document Control

## Options

### Option A: Controlled docs with version/approval/retention (Recommended)
- **Description**: Every document has ID, version, owner, approver, effective date, review cycle.
- **Pros**: Auditable, consistent, traceable.
- **Cons**: Process overhead.
- **Best for**: Regulated environments.

### Option B: Wiki/Markdown in repo
- **Description**: Version-controlled docs without formal approval.
- **Pros**: Fast, developer-friendly.
- **Cons**: Less formal audit trail.
- **Best for**: Small teams / internal.

## Recommendation
Option A for regulated; Option B acceptable for internal, with git history as audit trail.

## Rules
- Single source of truth; avoid duplicate docs.
- Version and date every document.
- Review on defined cadence (annual minimum).
- Archive obsolete docs; don't delete.
- Access control by role.
