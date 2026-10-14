# Marvel Infinity War — Player Guide

Connect your 8BitDo before opening the game. Pick your heroes and use the tutorial to try their attacks, movement and special abilities. Jacob’s working controller/display preset is provided for a fresh install; your existing settings always win.

For package 0.3.0, fresh installs use `~/Games/marvel-infinity-war`;
existing receipt locations are unchanged. Keep `Saves/` backed up. Repair and
game-only removal preserve customized CFG and progress and keep the shared
engine. If a managed PAK or launcher was edited, removal stops rather than
deleting those edits. Upgrading from 0.2.0 keeps your saves and settings and
moves the game to its own build-specific engine folder; the old engine folder
is left untouched. This installer has not certified target gameplay.

## Suggested 8BitDo layout

Use the letters printed on the SNES-style controller, regardless of Xbox button names shown by Linux.

| Action | Button |
|---|---|
| Move | D-pad, or map the left stick directions |
| Attack 1 | Y, left face button |
| Jump | B, bottom face button |
| Trait | X, top face button |
| Block | A, right face button |
| Helper | L |
| Super | R |
| Start / Pause | Start (+) |
| Screenshot | Keyboard F12 |

This is a suggested layout, not a decoded claim about the supplied cfg. Exact physical assignments and simultaneous D-pad/stick binding were not individually confirmed. The captured preset is the authoritative working configuration.

In Control Options, enable gamepads and enter Player 1. Highlight an action with the keyboard, press Enter to start reassignment, release Enter, then press the controller button or move the stick in the desired direction. Choose OK to save. If Linux reports an Xbox 360 pad, that is consistent with the tested controller mode.

Select fullscreen and **CRT scanlines TV** in Video Options if you change or reset settings. Exit through the game menu and relaunch to confirm settings and progress persist. Avoid force-killing the game while saving.

The tutorial-to-menu transition is the key compatibility check: OpenBOR 7533 failed there; the pinned 6391 setup progressed beyond it. If something fails, retain `Logs/OpenBorLog.txt` and `Logs/ScriptLog.txt` from the installed game directory. Confirm controller input, audio, progression and clean relaunch before marking this installation ready in Momentum.
