# Release Status

Conflu release status is recorded in GitHub release notes and in the attached `distribution-state.json` asset.

Core channels:

- `github_release_assets`
- `distribution/public-root`

Secondary channels:

- `npm`
- `homebrew` (planned)

States:

- `draft`: release artifacts are not public yet.
- `candidate`: release artifacts exist and are awaiting promotion.
- `public_rc`: release candidate is public and core channels are healthy.
- `public_ga`: stable release is public and core channels are healthy.
- `public_degraded`: public release is usable but one or more selected secondary channels is unhealthy.
- `revoked`: release is no longer recommended.

For each release, inspect:

- `current_state`
- `selected_channels`
- `channel_status`
- `core_verification`

