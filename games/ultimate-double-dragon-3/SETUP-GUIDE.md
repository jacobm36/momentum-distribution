# Ultimate Double Dragon 3 — Setup Guide

## What you need

- Ubuntu 24.04 x86_64 with Momentum Core.
- Your own copy of UDD 3.0. The folder you select must contain `UDD_3.0.pak`
  with exactly 1,408,885,949 bytes and SHA-256
  `95000dd09b8e7315c331dfbafec12b40714ea007e3631588f51849ce16a57884`.
  Official pages: https://mahcneto.itch.io/ultimatedoubledragon and
  https://openborgx.wordpress.com/2024/02/12/ultimate-double-dragon-ver-1-0/
- About 1.5 GiB free in the games root.

You can check the PAK yourself with `sha256sum "UDD 3.0/Paks/UDD_3.0.pak"`.

## Install

1. In Momentum, open the package store, choose Local packages and import
   `ultimate-double-dragon-3-0.1.0.zip`.
2. Choose the folder containing `UDD_3.0.pak` and the games root.
3. If OpenBOR 6391 is not prepared yet, review and approve its preparation.
   An intact copy from Marvel Infinity War 0.3.0 is reused.
4. Review the file changes and choose Approve and install.

Only the PAK is copied. Executables, settings, saves and other files in the
source folder are never imported, and the source is never modified.

## Existing manual setups

A manual launcher at `~/.local/bin/ultimate-double-dragon-3` or desktop entry at
`~/.local/share/applications/ultimate-double-dragon-3.desktop` is not owned by
this package, so installation stops before writing anything. Move those two
files aside (for example add `.manual-backup`) and retry. A manual game folder,
its saves and any existing library entry are left alone; Momentum adds the
packaged game as a separate library entry if the id is already in use.

To carry over existing settings or progress, copy your manual `Saves/` files
into `~/Games/ultimate-double-dragon-3/Saves/` after installation while the game
is closed. The packaged preset is only seeded when `Saves/UDD_3.0.cfg` is absent.

## Troubleshooting

| Problem | What to do |
|---|---|
| “Selected PAK does not match” | The PAK is a different release or damaged. Use the tested UDD 3.0 PAK. |
| “Existing integration is unowned” | Move the manual launcher/desktop entry aside, as above. |
| Windowed or different controls | An existing cfg was preserved. Change options in-game and save normally. |
| Controller unresponsive | Connect before launch, enable gamepads, and press Enter before each binding. |
| Missing host libraries | Install the libraries named in the setup requirement; the engine is not changed. |
