# The House of the Dead 2: laptop check and controls

This package requests mouse lightgun on Port A, visible crosshair and fullscreen. It preserves your existing Flycast mappings. Installation checks cannot prove that aiming or a fresh-machine keyboard mapping works.

1. Close any other Flycast session before installation/repair/removal.
2. Launch the installed Momentum entry, or the generated `~/.local/bin/house-of-the-dead-2` wrapper if the runner used the suggested path.
3. Confirm fullscreen and a visible crosshair. Move the mouse and check that aim tracks across the whole play area.
4. Use your configured **Start** binding to enter the game. If it is missing, open Flycast's input settings and bind Start for your keyboard. No particular default key is claimed here.
5. Confirm left-click fires. The earlier laptop setup confirmed **firing off-screen reloads**. Dedicated right-click reload has not been verified; do not rely on it.
6. Check reload, then play through a short section. If aim is offset, use the game's calibration/settings and preserve the resulting state. Do not substitute widescreen hacks as an aiming fix.
7. Exit through the configured Flycast menu/exit control. Confirm Momentum stops recording the session. Exact default exit/menu keys must be checked on your installed version.
8. Relaunch and confirm mappings, calibration and progress/settings persist. Record the Flycast version and OS with the test result.

If input does not work, inspect Flycast's Mouse/Keyboard input mapping for Port A. Set/configure the trigger and Start as needed; mappings differ by device/version. An absent fresh profile is intentionally left for Flycast to create, and manual setup remains visible in Momentum.

The launcher provides read-only access to the game folder. Normal Flycast profile storage remains its own user Flatpak profile. If the emulator tries to write state beside the CUE and fails, stop and record the actual path before changing permissions or the package contract.

An installed/setup-required result means the files are installed and target/manual checks remain. Only your successful test should authorize Momentum to record user-confirmed readiness.

## Credits and attribution

See [LEGAL-NOTICES.md](LEGAL-NOTICES.md) for original game, software, artwork and mod credits, source links, applicable rights and documented follow-up. Upstream notices remain intact.
