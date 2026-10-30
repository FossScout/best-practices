# Python Best Practices: Project Setup

## Options

### Option A: pyproject.toml + src layout + uv (Recommended)
- **Description**: Modern PEP 621 project with `src/` layout, managed by uv.
- **Pros**: Standard, fast, reproducible.
- **Cons**: uv newer tooling.
- **Best for**: New projects.

### Option B: setup.py + requirements.txt
- **Description**: Legacy.
- **Pros**: Familiar.
- **Cons**: Deprecated patterns.
- **Best for**: Legacy maintenance.

## Recommendation
Option A. Use `src/` layout and pyproject.toml.

## Rules
- Use `src/<package>/` layout.
- Pin Python version in `.python-version` and pyproject.
- Use virtual env per project.
- Commit lockfile.
- Configure tooling in pyproject (ruff, mypy, pytest).
