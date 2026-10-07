# Momentum Core Distribution

Public downloads for Momentum Core's approved game installer packages.
Users should choose a game, locate their own game files, review the changes, and install.
Momentum handles package downloads and required software; GitHub sign-in is not required
to access public releases.

## Current status

The first public installer is [The House of the Dead 2 0.1.2](https://github.com/jacobm36/momentum-distribution/releases/tag/the-house-of-the-dead-2-0.1.2).
It uses original Momentum artwork, not SteamGridDB images. Installer code and
documentation are MIT licensed; the package records separate icon permissions.
The private 0.1.1 release remains unchanged and is not redistributed here.

Download the ZIP from the release, then use **Installs & jobs > Install package**
in the updated Momentum launcher. Supply your own Dreamcast USA CUE file and
all matching BIN tracks together in a local folder.

### Version 0.1.2 verification

- ZIP SHA-256: `aecc8eca957f482eb969a6837134b07ed19296b519773bf3cd02892db00eb7b3`
- Canonical package digest: `sha256:ee75c953277283f8a9d38662b13900f3ea5a6a66ed14dc6e00cfd5db6700675a`
- Target: Ubuntu 24.04 x86_64; user-scope Flycast v2.7 commit
  `86ec4d845a66ff07cdba8e003d8549e93cd7a814b519766e1f744e530c5d3e5b`.
- Installer executable code is byte-identical to the isolated gameplay-tested
  0.1.1 baseline. This artwork/documentation revision passed package and synthetic
  launcher integration tests; it does not claim a separate gameplay run or
  fresh-machine certification.
- Users must confirm gameplay for their own installation. Existing custom artwork
  and Steam lookup remain available in the launcher editor. Installation does not
  download third-party artwork.

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
