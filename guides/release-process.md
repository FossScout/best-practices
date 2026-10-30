# Release Process (Reusable)

This is a reusable release process guide. Adapt to project needs.

## Prerequisites
- All changes merged to main via PR with green CI and required reviews
- Changelog updated
- Version bumped appropriately

## Versioning
Follow [Semantic Versioning](https://semver.org/):
- **MAJOR**: Breaking changes
- **MINOR**: New features, backwards compatible
- **PATCH**: Bug fixes, backwards compatible

Use annotated tags: `git tag -a vX.Y.Z -m "Release vX.Y.Z"`

## Steps
1. **Prepare**: Ensure main is up to date and CI passes
2. **Update changelog**: Move entries from [Unreleased] to new version section
3. **Bump version**: Update version in project files as needed
4. **Commit**: `chore(release): vX.Y.Z`
5. **Tag**: Create annotated tag and push
6. **Release**: Create GitHub Release with notes
7. **Post-release**: Update changelog for next development cycle

## Best Practices
- Keep releases small and frequent
- Always create annotated tags
- Document breaking changes clearly
- Test release artifacts before publishing
- Follow project's release checklist
