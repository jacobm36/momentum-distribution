# Momentum Core Distribution

Public downloads for Momentum Core's approved game installer packages.
Users should choose a game, locate their own game files, review the changes, and install.
Momentum handles package downloads and required software; GitHub sign-in is not required
to access public releases.

## Current status

The distribution repository is established, but no packages are published yet.
The House of the Dead 2 installer 0.1.1 remains private pending verification of the
bundled icon's public redistribution rights. Its released bytes will not be changed
under that version.

The launcher's in-app game catalog and download flow are a separate next step;
creating this repository does not enable those features.

## What belongs here

Only approved, redistributable installer ZIPs and their public release information.
No game data, ROMs, BIOS files, personal configuration, credentials, or private
development history.

Before each publication:

- Verify redistribution rights for all bundled code, settings, and artwork.
- Check the complete package for personal data and secrets.
- Run package tests and launcher intake validation.
- Publish a fixed version through GitHub Releases, with its ZIP SHA-256 and
  canonical package digest.
- Describe the tested platform and compatibility limits honestly.
- Never replace a published version with changed bytes; issue a new version.

Private development remains separate. Users provide their own game data locally.
Public availability is not a substitute for package validation or installation approval.
