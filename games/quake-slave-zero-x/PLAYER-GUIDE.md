# Play Episode Enyo

You are Enyo, an elite assassin on a mission to kill the Sovereign Khan. This six-level campaign replaces Quake's familiar arsenal and enemies with the world of Slave Zero X.

Launch **Quake - Slave Zero X: Episode Enyo** from your Applications menu once installation has completed through a supporting runner. Confirm the Episode Enyo title screen, then start a new single-player game. Check the game's Options/Controls menu before playing: existing bindings are preserved, and this installer does not impose an unverified keyboard layout.

| Action | Where to confirm/change it |
|---|---|
| Look/aim and fire | Mouse settings and attack binding in Controls |
| Move, strafe and jump | Movement bindings in Controls |
| Change weapons | Weapon bindings in Controls |
| Save and load | Single-player Save/Load menus |
| Fullscreen | Requested on startup; pass `-window` to the wrapper for windowed startup |
| Exit | Open the menu with Escape and choose Quit |

These are action descriptions, not a claim that new bindings were tested. The package imports selected `.cfg` and `.sav` files from the `enyo` mod folder only; it does not copy a root `vkQuake.cfg` or force the laptop's resolution. Fullscreen is requested each launch. Set controls, resolution, and sensitivity in-game, then save early. Close normally so the engine can persist settings. Before uninstalling, back up saves/settings from the destination and your vkQuake user directory. Game-only removal keeps those files, the engine and original Quake installation.

If ordinary Quake appears instead, the launch command must include `-game enyo`. If the engine fails before the menu, consult the installer README's AppImage/Vulkan guidance.

## Credits and attribution

See [LEGAL-NOTICES.md](LEGAL-NOTICES.md) for original game, software, artwork and mod credits, source links, applicable rights and documented follow-up. Upstream notices remain intact.
