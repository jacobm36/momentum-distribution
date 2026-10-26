# Momentum Core Distribution

**Community games. Arcade oddities. Boomer shooters.**
All the stuff enthusiasts love, without the setup pain.

Momentum Core is not a ROM frontend. It is a Linux game library plus a
compatibility and packaging platform. The launcher can hold any game you can
launch on Linux; packages add a tested setup: the engine, launch settings,
controls, presentation and preserved player state. You bring your own game
files where required.

The catalog currently specializes in three areas, and grows one real game at a
time:

- **OpenBOR:** fan-made beat 'em ups, packaged and made Linux-native.
  OpenBOR, without the setup.
- **Momentum Mouse Arcade:** light-gun and rail-shooter games adapted to mouse
  controls. Point, click, play.
- **Boomer Shooters:** classic engines and modern mods, curated into a polished
  library. Classic engines. Modern mods. Less setup.

Public package downloads for eleven owner-approved games.
The [Momentum launcher is public](https://github.com/jacobm36/momentum-core-launcher/releases).
This repository publishes game installers, not launcher downloads.

## Supported catalog

| Pillar | Game | Runtime | Installer | Bring your own |
|---|---|---|---|---|
| OpenBOR | [Marvel Infinity War](games/marvel-infinity-war/README.md) | OpenBOR 6391 | 0.3.0 | Direct ZVitor download or exact offline PAK |
| OpenBOR | [Ultimate Double Dragon 3](games/ultimate-double-dragon-3/README.md) | OpenBOR 6391 | 0.1.0 | Exact `UDD_3.0.pak` |
| Momentum Mouse Arcade | [Star Wars Trilogy Arcade](games/star-wars-trilogy-arcade/README.md) | Supermodel | 0.2.2 | `swtrilgy.zip`, kept zipped |
| Momentum Mouse Arcade | [L.A. Machineguns](games/l-a-machineguns/README.md) | Supermodel | 0.2.3 | Japan `lamachin.zip`, kept zipped |
| Momentum Mouse Arcade | [Virtua Cop 2](games/virtua-cop-2/README.md) | Flycast v2.7 | 0.1.3 | Japanese GDI and all 39 referenced tracks |
| Momentum Mouse Arcade | [Time Crisis II](games/time-crisis-ii/README.md) | MAME 0.289 | 0.1.1 | `timecrs2.zip` compatible with the pinned build |
| Momentum Mouse Arcade | [The House of the Dead 2](games/the-house-of-the-dead-2/README.md) | Flycast | 0.3.1 | USA CUE and all referenced BIN tracks |
| Boomer Shooters | [Brutal Doom](games/brutal-doom/README.md) | UZDoom | 0.3.0 | `DOOM2.WAD` |
| Boomer Shooters | [Brutal Doom 64](games/brutal-doom-64/README.md) | UZDoom | 0.3.0 | `DOOM2.WAD` |
| Boomer Shooters | [Episode Enyo](games/quake-slave-zero-x/README.md) | vkQuake | 0.3.0 | Quake `id1/pak0.pak` and `id1/pak1.pak` |
| Boomer Shooters | [Duke Nukem 3D](games/duke-nukem-3d/README.md) | Native EDuke32 | 0.2.0 | Registered original/Atomic `DUKE3D.GRP` |

Catalog entries carry optional `pillar` and `runtime` fields that the current
launcher uses to group the store and show runtime badges. Older launchers
ignore them.

Marvel Infinity War 0.3.0 keeps the same game, settings preset and OpenBOR 6391
bytes as 0.2.0, but prepares the engine in Momentum's build-specific folder
`openbor/builds/6391-ef96ad2e3a64`. Upgrading from 0.2.0 keeps the game folder,
settings and saves, backs up the old launcher script and leaves the legacy
`openbor/6391` folder in place. Install/verify/repair/removal/reinstall and the
0.2.0-to-0.3.0 upgrade passed isolated runner tests with the exact PAK; the owner
then upgraded a real 0.2.0 installation, reported it looks great and approved
publication on October 13, 2026. The runtime is bundled; the game PAK is not.
Individual target acceptance checks and full campaign coverage are not claimed.
The 0.2.0 source tag remains for traceability; its obsolete download was removed.

Ultimate Double Dragon 3 0.1.0 was approved for publication on October 13, 2026.
It shares Marvel's exact OpenBOR 6391 runtime and build-specific folder; you
supply the exact `UDD_3.0.pak` (no download). The isolated real-runner lifecycle
passed with the exact PAK. The owner previously confirmed play with persistent
fullscreen, shader and controller settings on a manual 6391 setup; stage
transitions and the full campaign are not claimed.

The owner approved publication on October 10, 2026 after successful private
testing. This is not certification of every hardware platform or every action.
Historical HOD2 0.3.0 and Brutal Doom 0.3.0 are the exact r6 candidate package bytes. Enyo 0.3.0
is the source-only publisher-download installer: its installer/download flow
was checked separately; earlier gameplay acceptance covered 0.2.2's matching
mod/fullscreen recipe, not a separately observed 0.3.0 target checklist.

SWTA 0.2.2 and L.A. Machineguns 0.2.3 seed missing NVRAM with the owner's
working Free Play state, including explicitly approved scores/bookkeeping.
These are not cleaned factory presets. Existing player NVRAM is never replaced.
Virtua Cop 2 0.1.3 and HOD2 0.3.1 seed missing title-specific mouse mappings
with the owner's right-click reload binding. Personal mappings stay intact.
All four include a description, portrait Grid art, a genuine screenshot and a
preview video. This is the baseline for new/revised packages; historical
immutable releases are not rewritten. Exact package and isolated synthetic
installer checks passed; new-revision gameplay acceptance remains separate.

Virtua Cop 2 0.1.2 uses a copy-only migration into the package-ID game folder;
the previous folder and separate game state are retained. The owner reported
that the game works great and confirmed gameplay acceptance on their setup on
October 15, 2026; specific checklist items and compatibility with other
hardware/platforms were not reported. Its earlier 0.1.0 release remains
withdrawn and unchanged.

Brutal Doom 64 0.3.0 was approved for publication on October 13, 2026.
Package checks and synthetic installer lifecycle/managed-engine tests passed;
graphical gameplay and save/relaunch acceptance have not been reported for this
revision. Its four mod files, artwork and load order are unchanged from 0.1.x.
Readiness remains setup-required until the player confirms the game.

## Required launcher

Duke Nukem 3D 0.2.0 requires launcher preview.2 or newer for bundled EDuke32
preparation and screenshot retention. Its owner-accepted package reuses the
exact working engine/source pair and three enhancement packs, with the owner's
revised description and existing-user artwork/description preservation.

The four presentation/preset revisions above require the current privately
supplied launcher with generic package cover/Grid/video retention and their
exact installer evidence. The earlier 2026.10.25 preview.1 preparation ZIP
predates this support. Historical public launchers cannot install these
revisions; no new launcher is published by this package release.
The matching private preparation bundle is
`Momentum-Core-Launcher-2026.10.25-preview.2-package-presets-private.zip`
(SHA256 `e32b5b90456be30f7ecb24f2cfea9d85fb0ebd6a12bf6e81805cf388db3592f1`).
Its exact evidence, package/source bytes, catalog and checksums were checked
together. The canonical laptop checkout also contains this support.

Time Crisis II 0.1.1 requires the private launcher's MAME adapter and exact-byte
installer evidence in commit `22f0cb0`. The owner reported testing and accepting
the matching package-installed 0.1.0 candidate and approved publication on
October 22, 2026. The runtime, controls and exact seed are unchanged. Public
inclusion of the seed's calibration, scores and bookkeeping is explicitly
owner-approved; it is not a cleaned factory preset. Final 0.1.1 real
existing-engine lifecycle checks passed. Synthetic missing/incompatible-engine
tests do not establish real network acquisition. No full-speed, individual
gameplay checklist or other-machine claims are made.

Use the current privately supplied Momentum Core Launcher, including commits
`96d726f` (tested engine selection and isolated fallback) and `be6480c`
(installed-game import). Historical public launcher downloads do not support
these new package revisions. Marvel Infinity War additionally needs the current
private launcher's OpenBOR adapter with build-specific runtime folders and the
exact 0.3.0 evidence (commits `6a59195` and `9613e2a`). No new frontend
download is published here.

Ultimate Double Dragon 3 0.1.0 additionally requires the approved OpenBOR
package list and its installer evidence in private launcher commits `6ec9449`
and `3764f92`.

Virtua Cop 2 0.1.2 additionally requires the exact installer evidence in private
launcher commit `1ca410e`.

Brutal Doom 64 0.3.0 additionally requires the exact installer evidence and
managed binding registration in private launcher commit `1890ee9`.
UZDoom 5.0.1 is its supported build; Brutal Doom's
additional 5.0.3 evidence does not apply to this package.

In Momentum choose **Add game > Browse the package store**, select a game and
provide the required original files. Review software/source preparation and
game installation separately. A missing host prerequisite needs manual system
setup; installers do not request administrator access automatically.

HOD2, Brutal Doom and Brutal Doom 64 reuse exact supported existing engines in place. When an
installed copy is unsupported and no supported copy is found, a new installation
can offer a separately approved tested isolated build. Each managed game has
separate settings/saves; existing installations are not automatically migrated.
Allow 6 GiB for isolated Flycast or 4 GiB for UZDoom, plus game copies.
There are no automatic engine updates, profile migrations or shared cleanup.

Enyo reuses verified mod files/cache or offers a separately approved direct
publisher download. No Enyo mod files or commercial base-game files are bundled.

## Historical installers

Only the ten entries above are current supported downloads. Obsolete pre-release
assets and release pages, including old launcher downloads, were removed on
October 25, 2026. Git commits and tags remain intact for traceability, not as
supported installer replacements. Historical checksum files remain available
in Git history rather than the current repository root.
Removing downloads does not uninstall existing games. Preserve working setups,
original media, settings, saves and journals.

## Release integrity and retention

`catalog.json` records immutable release URLs, sizes, ZIP SHA256 values, canonical
package digests and platforms. Checksum sidecars accompany each installer.
Verify anonymous uploaded downloads before promoting the catalog; never replace
published bytes under an existing version.

During pre-release development, retain only catalog-current package downloads
and their checksum sidecars. When retiring a version, remove its release page
and assets without deleting its Git tag or rewriting source history.

The launcher's read-only `tools/check-release.py` verifies source/ZIP agreement,
immutable versions, package tests, exact software/helper evidence and catalog
fields. Installer verification remains distinct from gameplay confirmation.

Large bundled mod payloads are not tracked in the private package source Git
repository. Keep their exact files/hashes separately; a source clone alone does
not reproduce those archives.

Game/mod/artwork credits and applicable notices are retained in each game's
documentation and package. Installer-code licensing does not relicense
third-party content. Commercial ROMs, BIOS, personal state, credentials and
private development logs do not belong in this repository.
