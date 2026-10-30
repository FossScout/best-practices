# Android Best Practices: Lifecycle & State

## Options

### Option A: ViewModel + StateFlow + SavedStateHandle (Recommended)
- **Description**: ViewModel exposes StateFlow; SavedStateHandle for process death.
- **Pros**: Survives config changes and process death; testable.
- **Cons**: Boilerplate for simple screens.
- **Best for**: Most screens.

### Option B: Direct in Activity/Fragment
- **Description**: State in UI layer.
- **Pros**: Simple.
- **Cons**: Lost on config change, leaks.
- **Best for**: Avoid.

## Recommendation
Option A. Use sealed classes for UI state.

## Rules
- ViewModel never holds Context/View references.
- Use `repeatOnLifecycle` for flow collection in UI.
- Handle process death via SavedStateHandle.
- Keep one StateFlow per screen representing full UI state.
- Use `SharingStarted.WhileSubscribed` for upstream flows.
- Cancel work in onCleared.
