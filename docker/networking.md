# Docker Best Practices: Networking

## Options

### Option A: Default bridge + explicit ports (Recommended for simple stacks)
- **Description**: Use default compose network; expose only needed ports; internal services communicate by service name.
- **Pros**: Simple, DNS built-in, good isolation.
- **Cons**: Less control; port conflicts on host.
- **Best for**: Most compose stacks.

### Option B: Custom networks with segmentation
- **Description**: Separate frontend/backend networks; attach services selectively.
- **Pros**: Stronger isolation, least exposure.
- **Cons**: More config.
- **Best for**: Multi-tier or security-sensitive stacks.

## Recommendation
Start with default network; add custom networks when isolation matters. Never publish DB/cache ports to host in prod.

## Rules
- Services talk via service names, not localhost/127.0.0.1.
- Publish only edge/gateway ports; bind to 127.0.0.1 for local-only.
- Use `expose` (not `ports`) for internal-only services.
- Prefer IPv6/IPv4 dual-stack awareness; avoid hardcoded IPs.
- Healthchecks over network, not exec where possible.
