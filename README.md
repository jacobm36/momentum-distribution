# Momentum Core Distribution

**Community games. Arcade oddities. Boomer shooters.**
All the stuff enthusiasts love, without the setup pain.

Momentum Core is not a ROM frontend. It is a Linux game compatibility and
packaging platform. Each package carries a tested setup: the engine, launch
settings, controls, presentation and preserved player state. You bring your own
game files where required.

- **OpenBOR:** fan-made beat 'em ups, packaged and made Linux-native.
  OpenBOR, without the setup.
- **Momentum Mouse Arcade:** light-gun and rail-shooter games adapted to mouse
  controls. Point, click, play.
- **Boomer Shooters:** classic engines and modern mods, curated into a polished
  library. Classic engines. Modern mods. Less setup.

Public package downloads for six owner-approved games.
The Momentum frontend remains private; this repository publishes game installers,
not a new launcher release.

## Supported catalog

| Pillar | Game | Runtime | Installer | Bring your own |
|---|---|---|---|---|
| OpenBOR | [Marvel Infinity War](games/marvel-infinity-war/README.md) | OpenBOR 6391 | 0.2.0 | Direct ZVitor download or exact offline PAK |
| Momentum Mouse Arcade | [Star Wars Trilogy Arcade](games/star-wars-trilogy-arcade/README.md) | Supermodel | 0.2.1 | `swtrilgy.zip`, kept zipped |
| Momentum Mouse Arcade | [L.A. Machineguns](games/l-a-machineguns/README.md) | Supermodel | 0.2.2 | Japan `lamachin.zip`, kept zipped |
| Momentum Mouse Arcade | [The House of the Dead 2](games/the-house-of-the-dead-2/README.md) | Flycast | 0.3.0 | USA CUE and all referenced BIN tracks |
| Boomer Shooters | [Brutal Doom](games/brutal-doom/README.md) | UZDoom | 0.3.0 | `DOOM2.WAD` |
| Boomer Shooters | [Episode Enyo](games/quake-slave-zero-x/README.md) | vkQuake | 0.3.0 | Quake `id1/pak0.pak` and `id1/pak1.pak` |

Catalog entries carry optional `pillar` and `runtime` fields that the current
launcher uses to group the store and show runtime badges. Older launchers
ignore them.

Marvel Infinity War 0.2.0 is the unchanged r1/r2 game package. The owner reported
flawless debug-PC setup and supplied a gameplay screenshot, then approved
publication. Its native OpenBOR 6391 runtime is bundled; the game PAK is not.
Exact author acquisition and install/verify/repair/removal/reinstall passed
isolated runner tests. Individual target acceptance checks and full campaign
coverage are not claimed.

The owner approved publication on October 10, 2026 after successful private
testing. This is not certification of every hardware platform or every action.
HOD2 and Brutal Doom 0.3.0 are the exact r6 candidate package bytes. Enyo 0.3.0
is the source-only publisher-download installer: its installer/download flow
was checked separately; earlier gameplay acceptance covered 0.2.2's matching
mod/fullscreen recipe, not a separately observed 0.3.0 target checklist.

SWTA and L.A. Machineguns are unchanged. SWTA uses stock credits, not a free-play
preset. L.A. Machineguns seeds only absent NVRAM with clean calibration.

## Required launcher

Use the current privately supplied Momentum Core Launcher, including commits
`96d726f` (tested engine selection and isolated fallback) and `be6480c`
(installed-game import). Historical public launcher downloads do not support
these new package revisions. Marvel Infinity War additionally needs the current
private launcher's OpenBOR adapter and exact 0.2.0 evidence, included in the r2
private candidate. No new frontend download is published here.

In Momentum choose **Add game > Browse the package store**, select a game and
provide the required original files. Review software/source preparation and
game installation separately. A missing host prerequisite needs manual system
setup; installers do not request administrator access automatically.

HOD2 and Brutal Doom reuse exact supported existing engines in place. When an
installed copy is unsupported and no supported copy is found, a new installation
can offer a separately approved tested isolated build. Each managed game has
separate settings/saves; existing installations are not automatically migrated.
Allow 6 GiB for isolated Flycast or 4 GiB for UZDoom, plus game copies.
There are no automatic engine updates, profile migrations or shared cleanup.

Enyo reuses verified mod files/cache or offers a separately approved direct
publisher download. No Enyo mod files or commercial base-game files are bundled.

## Historical installers

Only the six entries above are current supported downloads. Earlier incorrect
or withdrawn installers are not restored to the store. Historical release
records and source tags remain references, not accepted replacements.
Withdrawal does not uninstall existing games. Preserve working setups, original
media, settings, saves and journals.

## Release integrity and retention

`catalog.json` records immutable release URLs, sizes, ZIP SHA256 values, canonical
package digests and platforms. Checksum sidecars accompany each installer.
Verify anonymous uploaded downloads before promoting the catalog; never replace
published bytes under an existing version.

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
