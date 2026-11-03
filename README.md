# Clear releases

This repository publishes signed Clear desktop releases and the over-the-air feed. Application source stays in the Clear source repository.

Clear checks:

`https://github.com/mrq-vibes/clear-releases/releases/latest/download/latest.json`

Each GitHub release includes:

- `latest.json`, the feed for that version
- `Clear.app.tar.gz`, the signed updater archive
- `Clear.app.tar.gz.sig`, the updater signature
- `Clear-v0.6.3-macOS-arm64.zip` for a manual macOS install, named with that version
- `SHA256SUMS`

The updater accepts an archive only when its signature matches the public key built into Clear. The private updater key is not stored here. These macOS archives are ad hoc signed for local installation and are not Apple notarized.

The feed URL has to be readable without a password. A private repository blocks the installed app from downloading updates.
