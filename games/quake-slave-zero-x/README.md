# Quake - Slave Zero X: Episode Enyo

Six levels. One assassin. Become Enyo and hunt the Sovereign Khan through an
industrial nightmare built on Quake.

## Bring your Quake

Choose your Quake folder containing **id1/pak0.pak** and **id1/pak1.pak**.
Momentum reuses verified Episode Enyo files or downloads them directly from the
publisher after separate approval. No mod files are included in this installer.
An optional existing Enyo folder can be selected instead of downloading.

## Install with Momentum

**Add game > Browse the package store > Episode Enyo > Choose folder > Review > Install.**

Public installer **0.3.0** requires the current private Momentum launcher.
Historical public launcher downloads do not support its publisher-source flow.

Momentum reuses the approved vkQuake AppImage or prepares it after a separate
download approval. Then review the game-file plan. Original files stay untouched.

## Play it your way

Use the game's Controls menu for movement, mouse aim, fire and weapon bindings.
Fullscreen is requested on startup without copying laptop display settings or
forcing a resolution. Existing controls and saves are preserved. Pass `-window`
to the launch wrapper for windowed startup. Escape opens the menu. Save early,
then check save/load and relaunch.

## Compatibility

Ubuntu 24.04 x86_64, the pinned official vkQuake 1.36.0 AppImage, FUSE 2 support
and a working Vulkan driver. No Snap fallback or automatic engine upgrades.
Installer testing is separate from gameplay: your library entry remains
**setup required** until you confirm display, controls, audio and save/relaunch.

## Keep it yours

Game files default to `~/Games/quake-slave-zero-x`, with sibling `id1` and
`enyo` folders. Existing `enyo` CFG/SAV files are copied from your selected
Quake folder; unrelated mods are not. Originals, copied base data, saves,
settings and modified files are preserved.

Verify checks without changing game files. Repair restores missing files from
their original bytes. Uninstall removes unchanged owned mod/integration files,
not your base data, state or shared engine. Retained receipts allow reinstall
without overwriting retained saves.

The launcher is `~/.local/bin/quake-slave-zero-x`. Lifecycle support and backups
remain under `~/.local/share/momentum-core/`. See the player guide for play notes
and the separate test report for verification scope.

## Credits and attribution

See [LEGAL-NOTICES.md](LEGAL-NOTICES.md) for original game, software, artwork and mod credits, source links, applicable rights and documented follow-up. Upstream notices remain intact.
