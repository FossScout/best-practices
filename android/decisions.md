# Android Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Project Structure
- **Decision**: Multi-module by feature + core (Option A)
- Build types/flavors; R8 in release.

## UI
- **Decision**: Jetpack Compose (Option A)
- State hoisting; stateless composables; previews.

## Lifecycle & State
- **Decision**: ViewModel + StateFlow + SavedStateHandle (Option A)
- repeatOnLifecycle; sealed UI state.

## Testing
- **Decision**: Unit + instrumented + Hilt testing (Option A)
- Turbine for flows; fakes over mocks.

## Release
- **Decision**: Signed AAB via CI + Play (Option A)
- Play App Signing; R8 full mode; version from git tag.
