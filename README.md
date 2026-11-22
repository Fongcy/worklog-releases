# Worklog Desktop Releases

This public repository is dedicated to distributing **signed** Worklog desktop installers and update metadata. Application source code remains in a private development repository.

## Publication policy

- **No unsigned installer may be published as an official release.**
- Windows installers require Authenticode code signing.
- macOS installers require Developer ID signing and Apple notarization.
- Only reviewed builds from the private development repository may be promoted.
- Release tags use `vMAJOR.MINOR.PATCH` and assets must match the tag.
- Do not store source code, credentials, signing keys, or CI tokens here.
- Do not upload internal unsigned test builds to public Releases.
- Keep existing release assets immutable; publish a new version for changes.

## Current status

The release channel is initialized, but **no production desktop release has been published**. The desktop client must not enable automatic installation until a trusted signing and end-to-end upgrade process is verified.

## Platforms

- Windows x64: signed NSIS installer.
- macOS x64 / arm64: notarized DMG and ZIP update assets.

## Release acceptance checklist

1. Review source and CI results.
2. Build in a protected trusted runner.
3. Sign binaries and notarize macOS.
4. Generate and verify hashes and update metadata.
5. Test clean installation and upgrades on supported platforms.
6. Approve publication and upload to this repository.
7. Verify public anonymous access to release metadata and downloads.
