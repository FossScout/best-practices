# Kotlin Best Practices: Code Style & Idioms

## Options

### Option A: Idiomatic Kotlin with ktlint/detekt (Recommended)
- **Description**: Leverage null safety, data classes, extension functions, scope functions; enforce via ktlint + detekt.
- **Pros**: Concise, safe, consistent.
- **Cons**: Overuse of cleverness possible.
- **Best for**: All Kotlin projects.

### Option B: Java-style Kotlin
- **Description**: Verbose, null-heavy, mutable.
- **Pros**: Familiar to Java devs.
- **Cons**: Misses Kotlin benefits.
- **Best for**: Avoid.

## Recommendation
Option A. Prefer immutability, expression functions, and null-safety.

## Rules
- Prefer `val` over `var`; immutable collections.
- Use data classes for DTOs/value objects.
- Null safety: avoid `!!`; use `?.`, `?:`, `requireNotNull` with messages.
- Scope functions: `let`/`run`/`apply`/`also`/`with` with intent.
- Extension functions for domain helpers, not utility dumping.
- Avoid `Any`/raw types; use generics.
- Run ktlint + detekt in CI; fail on violations.
