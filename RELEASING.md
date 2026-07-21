# Releasing

Published versions must be reproducible from Git. The Convertigo project version and Git tag must always match.

1. Update `version` in `c8oProject.yaml` and the matching section in `CHANGELOG.md`.
2. Open the project with the declared Convertigo template and verify that the mobile builder compiles the demo page without errors.
3. Commit the complete release state.
4. Create an annotated tag named `v<project-version>`, for example `v8.4.0.1`.
5. Push both the release commit and its tag.

Consumers should depend on a release tag. The `master` branch represents the current development state and must not be used when a reproducible delivery is required.
