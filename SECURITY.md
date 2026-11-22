# Security Policy

This repository distributes Worklog desktop application binaries only. Report suspected tampering or compromised release artifacts privately to repository maintainers using GitHub's private vulnerability reporting if enabled. Do not publish secrets in issues.

A release is trusted only after platform code signing and (on macOS) notarization have been verified. SHA-512 hashes detect accidental corruption but do not authenticate the publisher by themselves.

No installer is currently approved for automatic installation. Untrusted or unsigned packages must never be promoted to stable releases.
