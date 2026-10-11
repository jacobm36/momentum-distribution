# Brutal Doom

Classic Doom II. A whole lot more impact.

## Bring your game

Select a folder containing your licensed **DOOM2.WAD**. All guide-selected mod content and artwork are bundled; no mod downloads or engine choices. Commercial base data is not included.

## Install

**Add game > Browse the package store > Brutal Doom > Choose folder > Review > Install.** Momentum prepares missing UZDoom after separate approval and copies your base files without changing originals.

Public installer **0.3.0** requires the current private Momentum launcher.
Historical public launcher downloads do not support the managed-engine contract.

Default destination: `~/Games/brutal-doom`. A supported existing UZDoom copy
keeps its existing settings/saves. Version 0.3.0 also accepts an explicitly
approved Momentum-managed isolated build when no tested copy is available.
That path has separate settings/saves under
`~/.local/share/momentum-core/state/brutal-doom/engine-profile-v1`, a hash-bound
retained launch helper and read-only game-media access. No existing profile
is imported or silently migrated. No persistent Flatpak overrides are written.

## Before playing

Confirm Brutal Doom weapons/HUD, voxel monsters and items, Doom Metal music, mouse aim/fire, movement, audio, desired display mode, save/relaunch and clean exit. Load order is brutalv21.pk3, brutalVoxelDoom2.0Complete.pk3, DoomMetalVol5.wad, matching the canonical laptop launcher. Existing UZDoom settings are preserved.

## Load order

Every launch loads `brutalv21.pk3`, `brutalVoxelDoom2.0Complete.pk3`, then `DoomMetalVol5.wad`, matching the canonical laptop setup. There is no `--metal` switch.

## Exact setup

No unrelated addon is bundled or loaded.

Verify is read-only. Repair restores missing owned files from their exact original bytes and reports edits instead of overwriting them. Uninstall preserves original data, IWAD, saves, edits, unknown files, software, art and support. Reconcile interrupted jobs before retrying.

## Credits

See [LEGAL-NOTICES.md](LEGAL-NOTICES.md) and retained [upstream credits](upstream/). Installer verification is not gameplay certification.
