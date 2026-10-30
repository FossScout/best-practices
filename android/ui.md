# Android Best Practices: UI

## Options

### Option A: Jetpack Compose (Recommended)
- **Description**: Declarative UI with Compose; Material3; theming via design tokens.
- **Pros**: Less boilerplate, state-driven, modern.
- **Cons**: Learning curve; interop with legacy Views.
- **Best for**: New apps.

### Option B: XML Views
- **Description**: Traditional View system.
- **Pros**: Mature tooling, familiar.
- **Cons**: Verbose, manual state management.
- **Best for**: Legacy maintenance.

## Recommendation
Option A for new development; migrate Views incrementally.

## Rules
- Single source of truth for UI state (StateFlow).
- Use `remember`/`rememberSaveable` appropriately.
- Hoist state; keep composables stateless where possible.
- Accessibility: content descriptions, semantics.
- Preview composables for all screens.
- Avoid business logic in composables.
