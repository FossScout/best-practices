# CI/CD Best Practices: Artifacts

## Rules
- Build once, promote artifact (don't rebuild per env).
- Store artifacts in registry (container/image, package).
- Tag with version + commit SHA.
- Retain N versions; prune old.
- Sign artifacts.
- Verify artifact integrity on deploy.
