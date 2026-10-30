# Kotlin Best Practices: Coroutines & Concurrency

## Options

### Option A: Structured concurrency with viewModelScope/io dispatcher (Recommended)
- **Description**: Use `coroutineScope`/`supervisorScope`, appropriate dispatchers, cancellation-aware code.
- **Pros**: Safe, predictable, leak-free.
- **Cons**: Requires understanding scopes/dispatchers.
- **Best for**: Most async work.

### Option B: GlobalScope / unstructured
- **Description**: Fire-and-forget coroutines.
- **Pros**: Simple.
- **Cons**: Leaks, unhandled exceptions, no cancellation.
- **Best for**: Avoid.

## Recommendation
Option A. Never use GlobalScope in app code.

## Rules
- Use structured concurrency; tie scopes to lifecycle (viewModelScope, lifecycleScope).
- Use `Dispatchers.IO` for blocking IO, `Default` for CPU, `Main` for UI.
- Avoid blocking calls on Main dispatcher.
- Handle cancellation: check `isActive`, use `ensureActive()`.
- Use `Flow` for streams; `StateFlow`/`SharedFlow` for state.
- Use `supervisorScope` when child failures shouldn't cancel siblings.
- Test coroutines with `runTest` and `TestDispatcher`.
