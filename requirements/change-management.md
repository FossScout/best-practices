# Requirements: Change Management

## Options

### Option A: Change request + impact analysis + approval (Recommended)
- **Description**: Formal change request, impact analysis (scope, cost, risk), review, approval before edit.
- **Pros**: Controlled, traceable, reduces scope creep.
- **Cons**: Slower.
- **Best for**: Regulated/production systems.

### Option B: Direct edit with PR review
- **Description**: Edit requirement in PR; reviewers approve.
- **Pros**: Fast, lightweight.
- **Cons**: Less formal impact analysis.
- **Best for**: Agile teams, low-regulation.

## Recommendation
Option A for regulated; Option B for agile. Either way, track changes in version control.

## Rules
- Every change references a change request/ticket.
- Update affected requirements' version and changelog.
- Re-review acceptance criteria after change.
- Notify stakeholders of changes.
- Keep change history (who, when, why).
