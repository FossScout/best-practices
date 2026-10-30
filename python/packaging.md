# Python Best Practices: Packaging & Release

## Options

### Option A: Build wheel + sdist, publish to PyPI/TestPyPI (Recommended)
- **Description**: Use `python -m build`; publish via twine/uv; version via git tags.
- **Pros**: Standard, reproducible.
- **Cons**: Setup (tokens).
- **Best for**: Libraries.

### Option B: Source-only distribution
- **Description**: Ship source.
- **Pros**: Simple.
- **Cons**: Slower install, no compiled extensions.
- **Best for**: Internal scripts.

## Recommendation
Option A for libraries.

## Rules
- Build both wheel and sdist.
- Version with SemVer from git tag.
- Publish to TestPyPI first.
- Use trusted publishing (OIDC) in CI.
- Include README, license, classifiers in metadata.
