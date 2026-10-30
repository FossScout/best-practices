# Database Best Practices: Offline-First

## Options

### Option A: Local DB + sync engine (Recommended)
- **Description**: Local SQLite/Realm/WatermelonDB with background sync to server.
- **Pros**: Works offline, fast local UX, resilient.
- **Cons**: Conflict resolution complexity, storage limits.
- **Best for**: Mobile/desktop apps with intermittent connectivity.

### Option B: Online-only with caching
- **Description**: Network-first with cache fallback.
- **Pros**: Simpler.
- **Cons**: Poor offline UX.
- **Best for**: Web apps with good connectivity.

## Recommendation
Option A for mobile; Option B for web.

## Rules
- Local-first reads; queue writes for sync.
- Handle conflicts (last-write-wins or CRDT).
- Show sync status to user.
- Encrypt local store.
- Test offline scenarios.
- Prune local data periodically.
