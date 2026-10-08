# Momentum Core Distribution

Public downloads for Momentum Core's approved game installer packages.
Users should choose a game, locate their own game files, review the changes, and install.
Momentum handles package downloads and required software; GitHub sign-in is not required
to access public releases.

## Current status

Choose your next arcade run:

| Game | Installer | Bring your own |
|---|---|---|
| [The House of the Dead 2](games/the-house-of-the-dead-2/README.md) | 0.1.3 | USA CUE and matching BIN tracks |
| [Virtua Cop 2](games/virtua-cop-2/README.md) | 0.1.0 | Japan GDI and all 39 tracks |
| [Star Wars Trilogy Arcade](games/star-wars-trilogy-arcade/README.md) | 0.1.0 | `swtrilgy.zip`, kept zipped |
| [L.A. Machineguns](games/l-a-machineguns/README.md) | 0.1.0 | Japan `lamachin.zip`, kept zipped |
| [Episode Enyo](games/quake-slave-zero-x/README.md) | 0.1.0 | Quake folder with both `id1` PAKs; complete mod included |
| [Brutal Doom 64](games/brutal-doom-64/README.md) | 0.1.0 | Folder containing `DOOM2.WAD`; complete four-file mod included |
| [Duke Nukem 3D](games/duke-nukem-3d/README.md) | 0.1.1 | Registered original/Atomic `DUKE3D.GRP`; upscale, voxel and SC-55 packs included |
| [Brutal Doom](games/brutal-doom/README.md) | 0.1.0 | `DOOM2.WAD`; v21 and optional Doom Metal Volume 5 included |
| [Aliens: Eradication](games/aliens-eradication/README.md) | 0.1.0 | `DOOM2.WAD`; complete 2.0 TC and eight-map campaign included |
| [Ashes 2063: Enriched](games/ashes-2063/README.md) | 0.1.0 | `DOOM2.WAD`; exact guide-defined Enriched 2.23 PK3 included |

The new installers pass isolated installation checks; gameplay confirmation
is still required for each user's setup. Read the game page for display/control
limits. Commercial base-game data, ROMs and BIOS files are not included;
The mod packages include their complete guide-selected mod content, artwork and
attribution; required commercial base files remain user-supplied.

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
published bytes. Accounts, ratings and
automatic updates are out of scope.

## What belongs here

Only approved, redistributable installer ZIPs and their public release information.
Complete approved mod payloads can accompany their installer. No commercial
base-game data, ROMs, BIOS files, personal configuration, credentials, or private
development history.

Before each publication:

- Verify redistribution rights for all bundled content.
- Check the complete package for personal data and secrets.
- Run package tests and launcher intake validation.
- Publish a fixed version through GitHub Releases, with its ZIP SHA-256 and
  canonical package digest.
- Describe the tested platform and compatibility limits honestly.
- Never replace a published version with changed bytes; issue a new version.

Private development remains separate. Users provide their own required base-game data locally.
Public availability is not a substitute for package validation or installation approval.
