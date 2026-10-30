# Release Management: Changelog

## Options

### Option A: Keep a Changelog + auto-generation (Recommended)
- **Description**: Follow Keep a Changelog format; generate from Conventional Commits (release-please/semantic-release).
- **Pros**: Consistent, automated, readable.
- **Cons**: Requires commit discipline.
- **Best for**: All projects.

## Recommendation
Option A.

## Rules
- Maintain CHANGELOG.md in repo.
- Sections: Added, Changed, Deprecated, Removed, Fixed, Security.
- Link to issues/PRs.
- Automate generation in CI on release.
- Keep unreleased section for upcoming changes.
