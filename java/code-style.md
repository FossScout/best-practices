# Java Best Practices: Code Style

## Options

### Option A: Spotless + Checkstyle + modern Java features (Recommended)
- **Description**: Auto-format with Spotless; enforce style via Checkstyle; use records, sealed classes, pattern matching.
- **Pros**: Consistent, modern, less boilerplate.
- **Cons**: Migration to modern features.
- **Best for**: All projects.

### Option B: Manual style
- **Description**: Convention only.
- **Pros**: Flexible.
- **Cons**: Inconsistent.
- **Best for**: Avoid.

## Recommendation
Option A.

## Rules
- Use records for DTOs/value objects.
- Prefer sealed classes for domain variants.
- Use `var` for local variables where type is obvious.
- Immutable collections; avoid null (Optional for returns).
- Format in CI; fail on violations.
- Avoid raw types and unchecked casts.
