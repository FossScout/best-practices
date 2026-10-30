# Gradle Best Practices: Publishing

## Options

### Option A: Maven Central / internal repo with signing (Recommended)
- **Description**: Publish via `maven-publish` + `signing`; automate in CI.
- **Pros**: Standard, verifiable, reproducible.
- **Cons**: Setup (GPG, OSSRH/Portal).
- **Best for**: Libraries.

### Option B: Local/file repo
- **Description**: Publish to local dir.
- **Pros**: Simple.
- **Cons**: Not shared.
- **Best for**: Internal testing.

## Recommendation
Option A for libraries; Option B for internal testing.

## Rules
- Sign all published artifacts.
- Include sources and javadoc jars.
- Use stable versioning (SemVer).
- Automate publishing from CI on tag.
- Never publish snapshots to release repo.
- Verify published artifact in a clean build.
