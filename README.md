# Clear releases

This repository publishes signed Clear desktop releases and the over-the-air feed. Application source stays in the Clear source repository.

Clear checks:

`https://github.com/mrq-vibes/clear-releases/releases/latest/download/latest.json`

The latest GitHub release includes:

- `latest.json`, the feed for that version
- `Clear.app.tar.gz` and `Clear.app.tar.gz.sig`, the signed macOS updater archive
- `Clear_<version>_aarch64.dmg` for a manual Apple Silicon install
- `Clear_<version>_x64-setup.exe` and its `.sig`, the Windows NSIS setup
- `SHA256SUMS`

The updater accepts a package only when its signature matches the public key built into Clear. The private updater key is not stored here. These macOS archives are ad hoc signed and are not Apple notarized. The Windows setup is not Authenticode signed.

The feed is public, so an installed app can download it without a password.
