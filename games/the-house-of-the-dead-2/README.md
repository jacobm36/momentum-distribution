# The House of the Dead 2

Installer **0.3.0** brings the Dreamcast USA release to Momentum with fullscreen,
mouse-lightgun input and a visible crosshair. Supply
`House of the Dead 2, The (USA).cue` and every referenced BIN track together.
No ROM, BIOS or engine binary is bundled.

## Install

Use the current private Momentum launcher:
**Add game > Browse the package store > The House of the Dead 2**.
Select your original media folder and review the exact plan. Originals stay
untouched. New games default to `~/Games/the-house-of-the-dead-2`; existing
receipts retain their recorded locations.

Momentum reuses a supported user/system Flycast copy in place. An unsupported
installed engine can lead to a separately approved isolated tested build when
no supported copy exists and this is a new game installation. Missing ordinary
software is prepared only after approval; the Flatpak client requires manual
host setup if absent. No existing engine is automatically changed.

The isolated build requires at least 6 GiB free plus game media. Its per-game
HOME/XDG settings and saves are under
`~/.local/share/momentum-core/state/the-house-of-the-dead-2/engine-profile-v1`.
Ordinary reuse retains the existing Flycast profile. Receipts never silently
switch profiles.

## Play and preserve

The wrapper requests fullscreen, port-A lightgun input, mouse aim, visible
crosshair and standard aspect ratio. Confirm Start/trigger mappings, aiming,
reload, audio and exit on your hardware. Dedicated right-click reload is not
separately certified. See [PLAYER-GUIDE.md](PLAYER-GUIDE.md).

Verify checks installed files. Repair restores missing owned files and reports
edits rather than replacing them. Uninstall preserves user state, shared engine
files, artwork, support and retained receipts; reinstall does not overwrite saves.
Partial engine transactions retain journals and stop for investigation.
No automatic updates, migration or cleanup.

## Compatibility and evidence

Ubuntu 24.04 x86_64; Bash/Python 3.10+, Flatpak and suitable graphics drivers.
Requires the current private launcher with the exact package/helper contract;
historical public launcher assets do not support this revision.

These are the exact HOD2 r6 bytes that passed installer/repeat, repair,
remove/reinstall, isolated real acquisition, windowed boot and idle VMU checks.
The owner reported the candidate working successfully and approved publication.
Individual target input/fullscreen/game-earned-save actions were not separately
documented; validate them on your machine. No general hardware certification.

See [LEGAL-NOTICES.md](LEGAL-NOTICES.md) for attribution. Installer code is MIT;
third-party artwork retains its own terms. No endorsement or affiliation.
