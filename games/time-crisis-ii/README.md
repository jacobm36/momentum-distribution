# Time Crisis II

Mouse aim. Take cover. Reload and return fire.

## Bring your game

Supply your own `timecrs2.zip` compatible with MAME 0.289. Keep it zipped.
Only this archive is copied, including safe clone subdirectories in a merged
archive; Momentum runs the exact MAME build's ROM audit. ROMs, BIOS and emulator
binaries are not included.

## Install with Momentum

Use the current privately supplied launcher, including commit `22f0cb0`.
Choose **Add game > Browse the package store > Time Crisis II**, select your
game folder, review and approve.

The installer reuses an exact supported MAME 0.289 Flatpak in user or system
scope. If none is available, it offers separately approved, pinned isolated
software preparation. Existing engines are never upgraded or downgraded.
Software preparation and game installation have separate approvals.

## Controls and presentation

- Mouse aims; left-click fires.
- Hold right-click for cover/reload; release to attack.
- Esc exits.
- Fullscreen, MAME BGFX `default` and free play retain the accepted recipe.

## Compatibility and acceptance

Ubuntu 24.04 x86_64 with the current private launcher's MAME integration.
MAME app commit:
`41ebdb5c266627f4d1f02ba11f8109e793d2381081b68afc48714dd48a703788`.
KDE runtime `org.kde.Platform/x86_64/6.11` commit:
`fe192771c0992ad873e6a9ccc6e4f087c76314ce5ced165650cc7ea045a6bbaa`.
Both are checked, including at launch.

On October 22, 2026 the owner reported testing and accepting the package-installed
0.1.0 candidate and approved public 0.1.1. Runtime, controls, lifecycle and seed
bytes are unchanged; this revision corrects public metadata/documentation and
version-sensitive fixtures. Final 0.1.1 installer checks passed real existing-MAME
install, repeat, verify, repair, removal and reinstall. Missing/incompatible-engine
approval flows passed with a synthetic engine; real network acquisition is not
claimed. No individual gameplay checklist, separate 0.1.1 play session,
universal input support or other-machine acceptance is claimed.

The manual setup previously logged 72.37% average emulation speed.
Full-speed performance is not promised.

## Seed and preservation

The owner explicitly approved public inclusion of the exact CFG and 64 KiB NVRAM
seed, including calibration, scores and bookkeeping. This is not a cleaned
factory preset. Seed files initialize only absent state on launch; existing
player state always wins.

New installs use `~/Games/time-crisis-ii`, launcher `~/.local/bin/time-crisis-ii`
and separate state under `~/.local/share/momentum-core/state/time-crisis-ii`.
The authoritative receipt records actual locations. The original manual tile,
ROM and shared MAME settings are not adopted or replaced.

Verification is read-only. Repair restores only missing owned files from exact
source bytes; edited content is retained and reported as a conflict. Removal
keeps settings, NVRAM, unknown content, original media, software and retained
support. Reconcile interrupted jobs before retrying.

## Credits

See [LEGAL-NOTICES.md](LEGAL-NOTICES.md). Existing Namco, MAME, BGFX and artwork
attribution is retained; unknown artwork provenance remains honest follow-up.
