# Airdrop Hunter — Release

This repository distributes Android build artifacts and public release notes only.

- Application source code remains in the private `airdrop-hunter` repository.
- No backend credentials, signing keys, database secrets, or private source files belong here.
- Debug APKs produced by the initial pipeline are for installation/testing and are **not** production-signed release builds.

## Build

The `Android build` workflow is manually dispatched by the repository owner. It checks out an explicitly supplied commit from the private core repository, runs Android unit tests, assembles a Debug APK, and publishes the APK as a GitHub Release asset.

### Required repository secret

Configure `CORE_REPO_READ_TOKEN` as a fine-grained, read-only token scoped only to `xiaobai607/airdrop-hunter` with **Contents: Read-only**. Never use a broad classic PAT.

The workflow deliberately does not copy source code into this public repository, its artifacts, or its releases.
