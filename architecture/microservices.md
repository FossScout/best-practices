# Architecture Best Practices: Microservices

## Rules
- Split only when scale/team demands.
- Each service owns its data; no shared DB.
- Async messaging for decoupling.
- API contracts versioned.
- Observability and resilience (circuit breakers, retries).
- Start with modular monolith; extract when justified.
