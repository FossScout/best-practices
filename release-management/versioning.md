# Release Management: Versioning

## Options

### Option A: Semantic Versioning (Recommended for libraries)
- **Description**: MAJOR.MINOR.PATCH; breaking changes bump major.
- **Pros**: Clear compatibility signal.
- **Cons**: Major bumps can be frequent.
- **Best for**: Libraries/APIs.

### Option B: Calendar Versioning (CalVer)
- **Description**: YYYY.MM.MICRO.
- **Pros**: Time-based, no semantic debate.
- **Cons**: No compatibility signal.
- **Best for**: Apps/services with continuous deploy.

## Recommendation
SemVer for libraries; CalVer or git SHA for services.

## Rules
- Never reuse or move tags.
- Pre-release suffixes (rc, beta) for previews.
- Automate version from git tags.
- Document versioning policy.
