# The House of the Dead 2: laptop check and controls

This package requests mouse lightgun on Port A, visible crosshair and fullscreen. It preserves your existing Flycast mappings. Installation checks cannot prove that aiming or a fresh-machine keyboard mapping works.

1. Close any other Flycast session before installation/repair/removal.
2. Launch the installed Momentum entry, or the generated `~/.local/bin/house-of-the-dead-2` wrapper if the runner used the suggested path.
3. Confirm fullscreen and a visible crosshair. Move the mouse and check that aim tracks across the whole play area.
4. A fresh HOD2 mouse mapping seeds **middle-click Start**. An existing custom mapping is kept, so use its Start binding instead if present.
5. Confirm **left-click fires** and test **right-click reload**. Those are the shipped fresh-mapping bindings, copied exactly from the laptop. Load binding was tested historically, not actual right-click gameplay reload. The earlier laptop setup confirmed **firing off-screen reloads**; confirm both actions on your installation.
6. Check reload, then play through a short section. If aim is offset, use the game's calibration/settings and preserve the resulting state. Do not substitute widescreen hacks as an aiming fix.
7. Exit through the configured Flycast menu/exit control. Confirm Momentum stops recording the session. Exact default exit/menu keys must be checked on your installed version.
8. Relaunch and confirm mappings, calibration and progress/settings persist. Record the Flycast version and OS with the test result.

If input does not work, inspect Flycast's Mouse/Keyboard input mapping for Port A. Set/configure trigger, reload and Start as needed; mappings differ by device/version. Manual setup remains visible in Momentum. At launch only, an absent `SDL_Default Mouse_MK-51002.cfg` is seeded under the normal Flatpak `config/flycast/mappings`, or the bound managed profile's `config/flycast/mappings`. Existing edited mappings are never replaced; install, repair and uninstall leave them alone.

The launcher provides read-only access to the game folder. Ordinary Flycast reuse keeps its own user Flatpak profile; explicitly managed installs use the bound `engine-profile-v1` instead. If the emulator tries to write state beside the CUE and fails, stop and record the actual path before changing permissions or the package contract.

An installed/setup-required result means the files are installed and target/manual checks remain. Only your successful test should authorize Momentum to record user-confirmed readiness.

## Credits and attribution

See [LEGAL-NOTICES.md](LEGAL-NOTICES.md) for original game, software, artwork and mod credits, source links, applicable rights and documented follow-up. Upstream notices remain intact.
