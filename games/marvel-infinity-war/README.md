# Marvel Infinity War — Momentum Core

## Published release 0.2.0

The owner approved this unchanged tested installer for publication after
reporting flawless debug-PC setup and sharing a gameplay screenshot. Actual
author download and full isolated runner lifecycle passed, as did the source
and extracted launcher suites (436 cases each, 67 skipped).

Use the current privately supplied launcher with OpenBOR support. The game PAK
downloads directly from ZVitor; it is not included in this release. The bundled
OpenBOR runtime is the exact tested build 6391. Existing settings/progress are
preserved. No complete campaign or individual target checklist is claimed.

The text below and accompanying notices are the original immutable package
documentation, including its earlier private-candidate status and explicitly
recorded provenance unknowns. Publication does not rewrite those historical
records or claim blanket rights clearance.

Bring a team of Marvel heroes into ZVitor’s fan-made beat ’em up, with native Linux OpenBOR and Jacob’s captured fullscreen, CRT scanlines TV and controller settings.

Private package **0.2.0**, Contract **1.0.0**, installer standard **1.0.1**, Ubuntu **24.04 x86_64**. This is an installer build candidate, with isolated lifecycle validation; current-runner real acquisition and target gameplay acceptance remain. See TEST-REPORT.md.

## Install through Momentum

The current parent launcher integration provides the exact OpenBOR resolver and allows online jobs to omit the source input. Import `marvel-infinity-war-0.2.0.zip`, review its trust/digest information, leave Download from ZVitor checked (or choose your PAK folder in offline mode), and choose the games root (default `$HOME/Games`). Review and approve the separate shared-software preparation and game installation plans in Momentum.

The PAK is acquired from the verified author-hosted release during approved setup, or copied from your chosen folder in offline mode. It is not bundled in the installer archive or committed to Git.

The installer creates its launcher and Applications entry during installation. Nothing in this package creates a launcher on the author’s laptop while building it.

| Resource | Default installed location |
|---|---|
| Game (fresh installs) | `$HOME/Games/marvel-infinity-war` |
| Content | game directory: `Paks/Marvel_Infinity_War.pak` |
| Settings / progress | game directory: `Saves/` |
| Logs / screenshots | game directory: `Logs/`, `ScreenShots/` |
| Shared engine | `$HOME/.local/share/momentum-core/software/openbor/6391/usr/bin/OpenBOR` |
| Generated wrapper | `$HOME/.local/bin/marvel-infinity-war` |
| Applications entry | `$HOME/.local/share/applications/marvel-infinity-war.desktop` |
| Retained support | `$HOME/.local/share/momentum-core/packages/marvel-infinity-war` |

The shared runtime is prepared from the exact tested AppImage’s extracted regular files. It uses its bundled libraries through `$ORIGIN/../lib`, requires no FUSE, and is reused only if every pinned file and mode matches. Preparation does not launch the game, download software, upgrade an engine or elevate privileges. Other OpenBOR versions are never substituted. Missing host libraries produce a setup requirement.

The generated wrapper changes to the game directory and executes that shared native engine, forwarding arguments and its exit status. Fullscreen, shader and controls come from the captured binary cfg, seeded only if absent. It never overwrites customized settings. Personal `.sav`, `.hi`, `.s00` files from the working capture are excluded.

The parent resolver checks host libraries with `ldd` against the small verified
runtime payload unpacked in its job workspace before approval/publication; it
does not execute the engine. The dedicated MIW integration serves retained
cover/video from installed support. These integration facts do not certify
real acquisition or target gameplay.

## Verify, repair and remove

Use Momentum’s operation flow. Scripts require a runner-created context, saved approved-plan digest and durable intent helper; they do not prompt in a terminal or write authoritative receipts/catalog entries. Verify is read-only. Repair restores missing owned PAK/wrapper files using the original online/offline inputs, and refuses to overwrite modified managed files. Uninstall previews first and removes only unchanged receipt-owned game content and integration. Edited managed files explicitly block removal before mutation; they are never silently relinquished or deleted. Customized user-state settings, saves, logs, screenshots, unknown files, artwork, support and the shared engine remain. A removed installation can be reinstalled in its retained directory. The previous receipt’s game directory is authoritative; this version performs no folder migration.

If installation fails partway, keep the runner’s intents, staging inventory and result evidence for reconciliation. There is no blind retry or universal rollback promise. Close OpenBOR before lifecycle operations.

## Compatibility and evidence

Official distribution: [OpenBOR v3.0 Build 6391](https://github.com/DCurrent/openbor/releases/tag/v6391). Supplied tested AppImage SHA-256: `35895117c2eae94867ee0b094083ae66cd3853372d7447d60cfe92fa929d73eb`. The upstream archive was downloaded by Jacob; the authoring environment hashes his supplied copy. It has not independently downloaded and compared the complete upstream 7z.

Build 7533 failed after the tutorial with `openborvariant: System variable name not found: 'cheats'`. Jacob confirmed 6391 controller gameplay, fullscreen and CRT shader; captured logs show progression through the tutorial, menu and `porta1.txt`. The official archive PAK exactly matches Jacob’s supplied checksum; the full campaign is unverified. This manual evidence does not certify this new installer on the target laptop.

Read [PLAYER-GUIDE.md](PLAYER-GUIDE.md), [SETUP-GUIDE.md](SETUP-GUIDE.md), [THIRD-PARTY.md](THIRD-PARTY.md), and [TEST-REPORT.md](TEST-REPORT.md). Artwork, engine, game and video retain their separate rights; Momentum’s MIT license applies only to its installer code and documentation.


## Online setup in Momentum — 0.2.0

Import the 0.2.0 installer into Momentum with the matching runner/frontend adapter. Leave **Download from ZVitor** checked; the existing-file folder can be blank. Choose the destination and continue. Review the game-download card and file changes, then choose **Approve and install**. There are no terminal prompts or administrator requests. If the exact engine is missing, its existing separate preparation review appears first. This is the normal frontend approval flow, not an additional terminal gate.

For offline setup, turn **Download from ZVitor** off and choose the folder containing `Marvel_Infinity_War.pak`. The PAK must match the exact size and checksum below; missing or different releases are rejected. Originals stay untouched. Online mode extracts only the PAK; the upstream Windows executable, logs, settings and personal state are excluded. Your fullscreen/CRT/controller preset still comes from this package, seeded only when settings are absent.

The pinned author-hosted release is https://www.zvitor.com/Downloads/MIW_v112f3.zip (527,099,513 bytes). Archive SHA-256: `27660c6a6fb0a42aa0e3360412ad2a2c8356bf553737dc3519d82a962130c6d0`. Only `MIW_Definitive/Paks/Marvel_Infinity_War.pak` is extracted, with 587,045,221 bytes and SHA-256 `4b5bbda8432437c13c7ee67d850fc6b24381ba6551c4cd9becb7861348fd2551`. This exactly matches Jacob’s working PAK. Source and hashes are fixed; changed downloads or redirects fail closed rather than substituting another edition.

Allow at least 2 GiB free in both the job workspace and installation destination. Temporary downloads are deleted after completion/failure/cancellation. No network request occurs in preflight, verify or uninstall; repeat installs with intact media need no game download. Repair fetches only when the pinned owned PAK is missing. Downloads have bounded size, a 30-second socket timeout, cancellation checks between reads and a 30-minute overall limit. A failed download does not publish the game; retain the runner’s stage/journal evidence for reconciliation before retrying.

The PAK stays outside the installer ZIP and Git history. No hosted mirror or rolling latest release is used. Earlier supplied installer artifacts are not modified by this integration.
