# Git Best Practices: Tagging & Versioning

## Options

### Option A: Semantic Versioning with annotated tags (Recommended)
- **Format**: `vMAJOR.MINOR.PATCH` (e.g., v1.2.3)
- **Pros**: Clear compatibility signal, tooling support, automation-friendly.
- **Cons**: Requires discipline; breaking changes bump major.
- **Best for**: Libraries and versioned products.

### Option B: CalVer
- **Format**: `YYYY.MM.DD` or `YYYY.MM.MICRO`
- **Pros**: Time-based clarity, no semantic debate.
- **Cons**: Doesn't convey compatibility.
- **Best for**: Apps/services with continuous deployment.

## Recommendation
Use **SemVer** for libraries; **CalVer** or git SHA for deployed services. Always use annotated tags.

## Rules
- Tag on main only, after CI green.
- Annotated tags: `git tag -a v1.0.0 -m "..."`.
- Push tags: `git push origin --tags` or specific tag.
- Never move or delete published tags.
- Automate releases via CI (release-please, semantic-release).
- Keep a CHANGELOG.md.
