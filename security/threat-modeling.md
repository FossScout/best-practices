# Security Best Practices: Threat Modeling

## Options

### Option A: STRIDE per feature + data flow diagrams (Recommended)
- **Description**: Identify threats (Spoofing, Tampering, Repudiation, Info disclosure, DoS, Elevation) per feature.
- **Pros**: Systematic, early risk discovery.
- **Cons**: Time investment.
- **Best for**: New features and releases.

## Recommendation
Option A. Lightweight threat modeling for each significant change.

## Rules
- Create data flow diagrams for new features.
- Document threats and mitigations.
- Review in design phase, not post-hoc.
- Reassess on architecture changes.
- Track mitigations as tasks.
