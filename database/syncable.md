# Database Best Practices: Syncable

## Options

### Option A: CRDT / operational transform sync (Recommended for collab)
- **Description**: Conflict-free replicated data types for multi-device sync.
- **Pros**: Automatic conflict resolution, real-time collab.
- **Cons**: Complexity, limited data types.
- **Best for**: Collaborative editors, multi-device state.

### Option B: Server-authoritative sync with versioning
- **Description**: Client sends changes with versions; server resolves.
- **Pros**: Simpler, centralized truth.
- **Cons**: Requires connectivity for resolution.
- **Best for**: Most apps.

## Recommendation
Option B default; Option A for real-time collaboration.

## Rules
- Include version/etag on every record.
- Detect conflicts; surface to user or auto-resolve with policy.
- Idempotent sync operations.
- Retry with backoff; handle partial failures.
- Audit sync events.
