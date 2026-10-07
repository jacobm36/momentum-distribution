# Momentum Core Distribution

Public downloads for Momentum Core's approved game installer packages.
Users should choose a game, locate their own game files, review the changes, and install.
Momentum handles package downloads and required software; GitHub sign-in is not required
to access public releases.

## Current status

The current public installer is [The House of the Dead 2 0.1.3](https://github.com/jacobm36/momentum-distribution/releases/tag/the-house-of-the-dead-2-0.1.3).
It restores the original HOD2 icon by **t00ny**, via
[SteamGridDB](https://www.steamgriddb.com/profile/76561199032730738/icons/1).
Installer code and documentation are MIT licensed; third-party artwork is excluded.
The package records attribution and the project owner's approved distribution basis
under SteamGridDB's user-content terms. This is not a claim of separate creator
permission or unrestricted rights to underlying game artwork.
Old installer ZIP downloads have been withdrawn; use 0.1.3.

Download the ZIP from the release, then use **Installs & jobs > Install package**
in the updated Momentum launcher. Supply your own Dreamcast USA CUE file and
all matching BIN tracks together in a local folder.

### Version 0.1.3 verification

- ZIP SHA-256: `a8ba738a43edecf5f1dc3d5fcc85c7d618b731817fee4a7ad154866519a7b84f`
- Canonical package digest: `sha256:2dcab2d2c2f99ddcfdcb67d589636459902139948d2562905cc3295cea94b641`
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
