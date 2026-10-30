# Docker Best Practices: Volumes & Persistence

## Options

### Option A: Named volumes for data, bind mounts for config/dev (Recommended)
- **Description**: Named volumes for DB/data; bind mounts for config files and source in dev.
- **Pros**: Portable across docker/podman, survives container recreation, clear ownership.
- **Cons**: Named volume location opaque; backup needs `docker volume` commands.
- **Best for**: Most stacks.

### Option B: Bind mounts everywhere
- **Description**: All data under host paths.
- **Pros**: Easy backup/inspection.
- **Cons**: Permission/UID mismatches, especially rootless/podman.
- **Best for**: Dev-only.

## Recommendation
Option A. Mount config as read-only (`:ro`) where possible. Support both docker and podman by using relative paths and avoiding host-UID assumptions; prefer named volumes or `${PWD}`-relative bind paths.

## Rules
- Data dirs: named volumes (e.g., `postgres_data`).
- Config dirs: bind mount read-only (`./config:/etc/app:ro`).
- Never store state in container writable layer.
- Use consistent host paths: `./data`, `./config`, `./logs`.
- Ensure non-root UID can write to mounted dirs (chown or init script).
- Backup strategy: volume snapshots or `docker run --rm -v ... tar`.
- Podman: use `:Z`/`:z` SELinux labels when needed; rootless default.
