# Python Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Project Setup
- **Decision**: pyproject.toml + src layout + uv (Option A)

## Code Style
- **Decision**: Ruff + type hints + mypy (Option A)

## Testing
- **Decision**: pytest + fixtures + coverage (Option A)

## Dependencies
- **Decision**: uv/pip-tools with lockfile (Option A)

## Packaging & Release
- **Decision**: Wheel + sdist to PyPI (Option A)
- Trusted publishing via CI.
