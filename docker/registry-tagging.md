# Docker Best Practices: Image Registry & Tagging

## Options

### Option A: Immutable tags + semver + digest promotion (Recommended)
- **Description**: Tag images with semver and git SHA; promote by digest across envs; never overwrite tags.
- **Pros**: Reproducible, traceable, safe rollback.
- **Cons**: More tags to manage; registry storage.
- **Best for**: Production pipelines.

### Option B: Mutable latest + date tags
- **Description**: Overwrite `latest` on each build.
- **Pros**: Simple.
- **Cons**: Non-reproducible, risky.
- **Best for**: Dev only.

## Recommendation
Option A. Use digest references in prod compose.

## Rules
- Never overwrite a published tag.
- Tag format: `app:1.2.3`, `app:1.2.3-<shortsha>`, `app:sha-<fullsha>`.
- Retain last N tags; prune old.
- Sign images (cosign) before push to prod registry.
- Use separate registries/repos for dev and prod if possible.
- Document pull policy (`pull_policy: always` for mutable, `never` for pinned digests).
