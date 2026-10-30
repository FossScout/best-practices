# Android Best Practices: Release

## Options

### Option A: Signed AAB via CI + Play Console + R8 (Recommended)
- **Description**: Build signed AAB in CI; upload to Play; enable R8 shrinking/obfuscation.
- **Pros**: Smaller downloads, automated, secure keys.
- **Cons**: CI secret management.
- **Best for**: Production.

### Option B: Manual signed APK
- **Description**: Local signing.
- **Pros**: Simple.
- **Cons**: Manual, error-prone, key risk.
- **Best for**: Avoid.

## Recommendation
Option A. Use Play App Signing.

## Rules
- Never commit keystore or passwords.
- Use Play App Signing; keep upload key secure.
- Enable R8 full mode + resource shrinking.
- Keep ProGuard rules for reflection/serialization.
- Version code auto-increment from CI; version name from git tag.
- Test release build (minified) before publish.
- Monitor crash reports (Firebase/Crashlytics).
