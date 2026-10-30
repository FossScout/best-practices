# Java Best Practices: Concurrency

## Options

### Option A: Virtual threads + structured concurrency (Java 21) (Recommended)
- **Description**: Use virtual threads for IO-bound work; structured concurrency APIs.
- **Pros**: Massive scalability, simple code.
- **Cons**: Java 21+; pinning pitfalls.
- **Best for**: IO-heavy services.

### Option B: Platform thread pools (ExecutorService)
- **Description**: Traditional fixed thread pools.
- **Pros**: Mature, well-understood.
- **Cons**: Limited scalability.
- **Best for**: CPU-bound or legacy.

## Recommendation
Option A on Java 21+; Option B otherwise.

## Rules
- Use virtual threads for blocking IO.
- Avoid synchronized blocks that pin virtual threads; use ReentrantLock.
- Use ExecutorService/CompletableFuture for composition.
- Never create unbounded threads.
- Handle interrupts and cancellation.
- Test concurrency with stress tests.
