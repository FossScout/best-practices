# Docker Best Practices: SBOM

## Options

### Option A: Generate SBOM at build time with syft (Recommended)
- **Description**: Use `syft` to generate SBOM (SPDX/CycloneDX) during CI build; attach to image via attestation.
- **Pros**: Accurate, automatable, supports vulnerability scanning (grype).
- **Cons**: Extra CI step; SBOM can drift if not regenerated.
- **Best for**: Production images and compliance.

### Option B: Registry-native SBOM (Docker Scout / cosign attest)
- **Description**: Use registry tooling to generate/attach SBOM.
- **Pros**: Integrated, less custom scripting.
- **Cons**: Vendor lock-in, less control.
- **Best for**: Teams on managed registries.

## Recommendation
Option A in CI; attach SBOM as OCI artifact/attestation; sign with cosign.

## Rules
- Generate SBOM for every released image.
- Store SBOM alongside image (registry attestation or artifact).
- Sign images and SBOMs (cosign / sigstore).
- Scan SBOM with grype/trivy in CI; fail on critical CVEs.
- Keep SBOM format standard (SPDX or CycloneDX).
- Regenerate SBOM on base image updates.
