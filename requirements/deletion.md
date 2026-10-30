# Requirements: Deletion & Obsolescence

## Options

### Option A: Mark obsolete, never hard-delete (Recommended)
- **Description**: Set status to "Obsolete" with reason and date; retain in history.
- **Pros**: Preserves traceability and audit trail.
- **Cons**: Accumulates stale items.
- **Best for**: All regulated/audited systems.

### Option B: Hard delete
- **Description**: Remove requirement entirely.
- **Pros**: Clean list.
- **Cons**: Breaks traceability, audit gaps.
- **Best for**: Avoid in regulated contexts.

## Recommendation
Option A. Archive obsolete requirements.

## Rules
- Never delete; mark status Obsolete with reason.
- Remove from active baselines but keep in archive.
- Update traceability links (tests, code) accordingly.
- Communicate deprecation to stakeholders.
- Periodic cleanup review of obsolete items.
