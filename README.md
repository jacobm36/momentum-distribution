# Momentum Core Distribution

Public downloads for Momentum's currently accepted game installers.
Choose a game, locate your own game files, review and install.

## Supported catalog

| Game | Installer | Bring your own |
|---|---|---|
| [Star Wars Trilogy Arcade](games/star-wars-trilogy-arcade/README.md) | 0.2.1 | `swtrilgy.zip`, kept zipped |
| [L.A. Machineguns](games/l-a-machineguns/README.md) | 0.2.2 | Japan `lamachin.zip`, kept zipped |

These two versions were accepted by the owner on the debug laptop.
Other hardware, ROM variants and emulator builds remain unverified.
SWTA keeps stock credits (3 for credit, 1 for Start), not preconfigured free play.
L.A. Machineguns seeds only absent NVRAM with clean calibration; existing NVRAM
is never overwritten. The owner confirmed the final installation played
correctly without a manual NVRAM copy.

## Launcher

Use the [latest Momentum launcher](https://github.com/jacobm36/momentum-distribution/releases/latest).
The 2026.10.09.1 launcher includes exact evidence for both supported packages,
clear update guidance, reviewed recovery actions and release consistency checks.
Startup uses Python's built-in HTTP support and does not require `curl`.
Python 3 and `flock` must be available; Momentum does not install system
packages or request administrator access automatically.

Extract the complete launcher into a separate folder. Close the old launcher,
then run `bash start-candidate.sh`. Do not overwrite old folders or delete jobs.
Receipts and game state remain shared user data. Install shortcuts using
`bash install.sh` only when ready to point them at the new folder.
Game ZIPs download separately through **Add game**; ROMs and BIOS are not bundled.

## Withdrawn installers

All other game releases are withdrawn from the supported catalog pending
acceptance under the current installation standard. Historical release records,
tags, checksums recorded in release notes and documentation remain available for
reference. Obsolete ZIP/checksum download assets have been removed; historical
game pages describe old releases, not currently offered installers.
Withdrawal does not uninstall any existing game.
Old SWTA/L.A. Machineguns versions are likewise historical; use the versions above.
Preserve your working setups, original media, saves and journals.

## Storage and retention

Keep downloads for the current accepted installers and latest launcher.
Withdrawn versions retain small release records, source tags and test evidence,
not bulky download assets. Never upload changed bytes under an old version.
Before removing obsolete assets, verify any useful local fallback against its
published checksum. Removing release assets does not rewrite source history.

The package source repository deliberately excludes large bundled mod payloads
from Git. A local working folder can contain those files, but a clone or Git
backup alone does not preserve them. Back up required payload files separately
with their hashes, together with uncommitted source changes. Keep an old ZIP
only when it provides a useful fallback or historical comparison; do not treat
withdrawn installers as accepted replacements.

## Release verification

`catalog.json` identifies fixed release URLs, sizes, ZIP checksums, canonical
package digests and platforms. Never replace published bytes under an existing
version. Verify the uploaded anonymous downloads before promoting the catalog.

The launcher's read-only `tools/check-release.py` checks source/ZIP agreement,
immutable versions, tests, exact launcher/software evidence and catalog fields.
Its final result is `RELEASE CHECK: PASS` (exit 0) or `RELEASE CHECK: FAIL` (exit 1).
It never publishes or invents gameplay acceptance.

Only approved distribution artifacts belong here, not commercial ROMs, BIOS,
personal state, credentials or private development history. Attribution is not
a blanket redistribution license; preserve each component's actual notices.
