# Momentum Core Distribution

Public downloads for Momentum Core's approved game installer packages.
Users should choose a game, locate their own game files, review the changes, and install.
Momentum handles package downloads and required software; GitHub sign-in is not required
to access public releases.

## Current status

The current public installer is [The House of the Dead 2 0.1.3](https://github.com/jacobm36/momentum-distribution/releases/tag/the-house-of-the-dead-2-0.1.3).
Old installer ZIP downloads have been withdrawn; use 0.1.3.

The updated Momentum launcher uses **Add game** to select HOD2 and download this
installer automatically. Supply your own Dreamcast USA CUE file and all matching
BIN tracks together in a local folder, then review and approve installation.
Manual release downloads remain available under **Add game > Advanced > Import a local package**.

### Version 0.1.3 verification

- ZIP SHA-256: `a8ba738a43edecf5f1dc3d5fcc85c7d618b731817fee4a7ad154866519a7b84f`
- Canonical package digest: `sha256:2dcab2d2c2f99ddcfdcb67d589636459902139948d2562905cc3295cea94b641`
- Target: Ubuntu 24.04 x86_64; user-scope Flycast v2.7 commit
  `86ec4d845a66ff07cdba8e003d8549e93cd7a814b519766e1f744e530c5d3e5b`.
- Installer executable code is byte-identical to the isolated gameplay-tested
  0.1.1 baseline. Version 0.1.3 passed package and synthetic
  launcher integration tests; it does not claim a separate gameplay run or
  fresh-machine certification.
- Users must confirm gameplay for their own installation.

## Catalog backend

`catalog.json` is the small public catalog consumed by the launcher. Each game
identifies one fixed GitHub Release ZIP, its byte size, ZIP SHA-256, canonical
package digest and platform. No account or hosted
application server is required. Package code is never executed from this branch.
Only the release ZIP is installed after validation and explicit user approval.

When publishing a newer package, add a new release and update its catalog record
only after verifying the downloadable asset and exact hashes. Never replace
published bytes. The initial catalog contains HOD2 only; accounts, ratings and
automatic updates are out of scope.

## What belongs here

Only approved, redistributable installer ZIPs and their public release information.
No game data, ROMs, BIOS files, personal configuration, credentials, or private
development history.

Before each publication:

- Verify redistribution rights for all bundled content.
- Check the complete package for personal data and secrets.
- Run package tests and launcher intake validation.
- Publish a fixed version through GitHub Releases, with its ZIP SHA-256 and
  canonical package digest.
- Describe the tested platform and compatibility limits honestly.
- Never replace a published version with changed bytes; issue a new version.

Private development remains separate. Users provide their own game data locally.
Public availability is not a substitute for package validation or installation approval.
