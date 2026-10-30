# Release Management: Feature Flags

## Options

### Option A: Feature flag service (LaunchDarkly/Unleash/Flagsmith) (Recommended)
- **Description**: Centralized flag management with targeting and gradual rollout.
- **Pros**: Safe rollouts, instant kill switch, A/B testing.
- **Cons**: Service dependency, cost.
- **Best for**: Production services.

### Option B: Config-based flags
- **Description**: Flags in config/env.
- **Pros**: Simple, no infra.
- **Cons**: Requires redeploy to change.
- **Best for**: Small/simple apps.

## Recommendation
Option A for prod; Option B for small apps.

## Rules
- Default flags off.
- Clean up flags after full rollout (avoid flag debt).
- Document flag owner and expiry.
- Test both on/off paths.
- Use flags for risky changes and migrations.
