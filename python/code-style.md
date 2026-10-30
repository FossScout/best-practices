# Python Best Practices: Code Style

## Options

### Option A: Ruff + type hints + mypy (Recommended)
- **Description**: Ruff for lint/format; full type hints; mypy/pyright for type checking.
- **Pros**: Fast, comprehensive, modern.
- **Cons**: Type hints effort.
- **Best for**: All projects.

### Option B: flake8 + black + no types
- **Description**: Traditional.
- **Pros**: Familiar.
- **Cons**: Slower, less safety.
- **Best for**: Legacy.

## Recommendation
Option A.

## Rules
- Run ruff check + format in CI.
- Type-hint all public functions.
- Use `from __future__ import annotations` where needed.
- Prefer dataclasses/Pydantic for data.
- Avoid mutable default args.
- Use pathlib, not os.path.
