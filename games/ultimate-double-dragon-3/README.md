# Ultimate Double Dragon 3 — Momentum Core

## Published release 0.1.0

The owner reviewed this installer and approved publication on October 13, 2026.
Bring your own `UDD_3.0.pak`; there is no download. The package bundles the same
exact native OpenBOR 6391 runtime as Marvel Infinity War 0.3.0, the captured
fullscreen/shader/controller preset, the icon and the preview video. The
isolated real-runner install/verify/repair/remove/reinstall lifecycle passed
with the exact PAK. Stage transitions and the full campaign have not been
confirmed; readiness stays setup-required until you confirm the game.

Use the current privately supplied launcher with the approved OpenBOR package
list and UDD3 evidence (commits `6ec9449` and `3764f92`). The game PAK is not
included in this release.

The text below and accompanying notices are the original package documentation.


The fan-made Ultimate Double Dragon beat ’em up on native Linux OpenBOR 6391, with Jacob’s captured fullscreen, shader and controller settings. Bring your own `UDD_3.0.pak`; Momentum handles the engine, preset, launcher and library entry.

Package **0.1.0**, Contract **1.0.0**, installer standard **1.0.1**, Ubuntu **24.04 x86_64**. This is an installer build candidate with isolated lifecycle validation; packaged target gameplay acceptance remains. See TEST-REPORT.md.

## Install through Momentum

Import `ultimate-double-dragon-3-0.1.0.zip` under Local packages, review its trust/digest information, choose the folder containing `UDD_3.0.pak` (for example `UDD 3.0/Paks`), and choose the games root (default `$HOME/Games`). Review and approve the shared-software preparation (if the engine is not already prepared) and the game installation plan.

There is no download. The PAK is copied from your chosen folder after its exact size and checksum are verified; your source folder is only read. The PAK is not bundled in the installer archive or committed to Git.

| Resource | Default installed location |
|---|---|
| Game (fresh installs) | `$HOME/Games/ultimate-double-dragon-3` |
| Content | game directory: `Paks/UDD_3.0.pak` |
| Settings / progress | game directory: `Saves/` |
| Logs / screenshots | game directory: `Logs/`, `ScreenShots/` |
| Shared engine | `$HOME/.local/share/momentum-core/software/openbor/builds/6391-ef96ad2e3a64/usr/bin/OpenBOR` |
| Generated wrapper | `$HOME/.local/bin/ultimate-double-dragon-3` |
| Applications entry | `$HOME/.local/share/applications/ultimate-double-dragon-3.desktop` |
| Retained support | `$HOME/.local/share/momentum-core/packages/ultimate-double-dragon-3` |

The shared runtime is the same verified OpenBOR 6391 build used by Marvel Infinity War 0.3.0; an existing intact copy is reused. It runs from extracted regular files with bundled libraries, needs no FUSE, and is never upgraded or substituted. Missing host libraries produce a setup requirement.

The wrapper changes to the game directory and runs that engine, forwarding arguments and exit status. Fullscreen, shader and controls come from the captured `Saves/UDD_3.0.cfg`, seeded only when absent. Customized settings are never overwritten.

If a launcher or desktop entry with the same name already exists and was not created by this package (for example from a manual setup), installation stops before changing anything. Move that manual launcher aside first; your manual game folder, saves and library entry are not touched.

## Verify, repair and remove

Use Momentum’s operation flow. Verify is read-only. Repair restores missing owned PAK/wrapper files from the original source folder and refuses to overwrite modified managed files. Uninstall previews first and removes only unchanged receipt-owned game content and integration. Edited managed files block removal. Settings, saves, logs, screenshots, unknown files, artwork, support and the shared engine remain.

If installation fails partway, keep the runner’s intents, staging inventory and result evidence for reconciliation. Close OpenBOR before lifecycle operations.

## Compatibility and evidence

Official engine release: [OpenBOR v3.0 Build 6391](https://github.com/DCurrent/openbor/releases/tag/v6391). Tested AppImage SHA-256: `35895117c2eae94867ee0b094083ae66cd3853372d7447d60cfe92fa929d73eb`.

Required PAK: `UDD_3.0.pak`, 1,408,885,949 bytes, SHA-256 `95000dd09b8e7315c331dfbafec12b40714ea007e3631588f51849ce16a57884`. Different releases are rejected.

Jacob confirmed on his laptop that UDD 3.0 launches and plays on native OpenBOR 6391, and that fullscreen, the selected shader and controller settings persist after restart. Stage transitions and the full campaign have not been confirmed. This manual evidence does not certify the packaged installer on the target laptop.

Read [PLAYER-GUIDE.md](PLAYER-GUIDE.md), [SETUP-GUIDE.md](SETUP-GUIDE.md), [THIRD-PARTY.md](THIRD-PARTY.md) and [TEST-REPORT.md](TEST-REPORT.md). Artwork, engine, game and video retain their separate rights; Momentum’s MIT license applies only to its installer code and documentation.
