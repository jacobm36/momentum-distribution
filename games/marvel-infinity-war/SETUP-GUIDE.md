# Marvel Infinity War — Momentum Core Ubuntu Setup

Prepared October 7, 2026. Installer standard: 1.0.1; package runner interface must follow the current approved Contract 1.0.0 and authoring baseline.

**Working engine:** the Linux AppImage shipped in official OpenBOR v3.0 Build 6391. Ubuntu 24.04 x86_64, keyboard and 8BitDo SNES Pro, fullscreen, and CRT scanlines TV were confirmed by Jacob during this session. This guide records a manually tested setup; it does not certify an installer package.

## Game contract

| Component | Confirmed value |
|---|---|
| Game | Marvel Infinity War by ZVitor |
| Edition | Exact upstream edition/version not established from the supplied filename |
| Content | `Marvel_Infinity_War.pak`; original file reported as approximately 560 MB |
| Original source | `/home/jake/Paks/Marvel_Infinity_War.pak` on the test machine |
| Test working directory | `$HOME/Games/OpenBOR-Test/6391` |
| Launch | `./squashfs-root/AppRun`, from that directory |
| Display | Fullscreen, CRT scanlines TV selected through the engine menus |
| Input | 8BitDo SNES Pro; Linux reported Microsoft X-Box 360 pad on USB |
| Configuration | `Saves/Marvel_Infinity_War.cfg` relative to working directory |
| State observed | `.sav`, `.hi`, `.s00`, and `.cfg` files in `Saves` |
| Logs | `Logs/OpenBorLog.txt` and `Logs/ScriptLog.txt` |

The package must generate its launcher during installation. No standalone laptop desktop launcher was requested. Final installed paths depend on the current runner implementation and selected games root; do not infer them from these temporary test paths.

## Why this engine

OpenBOR 4.0 Build 7533 initially loaded the game and accepted mapped controller input, but failed at the transition from the tutorial to `data/levels/mfa3/menu.txt`:

```text
openborvariant: System variable name not found: 'cheats'
```

The supplied 6391 test log records successful loading of character selection, tutorial, menu, and `data/levels/mfa3/porta1.txt`, followed by shutdown cleanup. Jacob confirmed controller gameplay, fullscreen, and CRT scanlines TV. Keep this exact engine distribution pinned; a newer engine is not an automatic compatibility upgrade.

The 6391 binary's log identifies itself as `OpenBOR v3.0 Build pass`, compiled December 25, 2020. Use distribution provenance and hashes rather than relying on that banner for build detection.

## Engine source and identity

Official release: https://github.com/DCurrent/openbor/releases/tag/v6391

Official archive:

```text
https://github.com/DCurrent/openbor/releases/download/v6391/OpenBOR.v3.0.Build.6391.7z
```

Archive member:

```text
OpenBOR v3.0 Build 6391/LINUX/OpenBOR/OpenBOR_3.0_6391.AppImage
```

The AppImage supplied in Jacob's working-setup archive was inspected locally:

```text
Size: 4796456 bytes
SHA-256: 35895117c2eae94867ee0b094083ae66cd3853372d7447d60cfe92fa929d73eb
```

This is the hash of the supplied, manually tested AppImage, not an independently retrieved hash of the complete upstream 7z archive. The final dependency resolver must check exact bytes before extraction/execution and accurately report upstream verification scope.

## Reproduce the manual setup

These commands document the successful test workflow. They are not the final Momentum installer entry point. Run them as the normal desktop user.

Install extraction tooling if needed:

```bash
sudo apt-get install p7zip-full
mkdir -p "$HOME/Games/OpenBOR-Test/6391"
cd "$HOME/Games/OpenBOR-Test/6391" || exit 1
curl --fail --location --retry 3 \
  --output OpenBOR-6391.7z \
  "https://github.com/DCurrent/openbor/releases/download/v6391/OpenBOR.v3.0.Build.6391.7z"
7z x -aos OpenBOR-6391.7z
cp -n \
  "OpenBOR v3.0 Build 6391/LINUX/OpenBOR/OpenBOR_3.0_6391.AppImage" \
  ./OpenBOR_3.0_6391.AppImage
```

Check the AppImage against the known tested bytes:

```bash
printf '%s\n' \
  '35895117c2eae94867ee0b094083ae66cd3853372d7447d60cfe92fa929d73eb  OpenBOR_3.0_6391.AppImage' \
  | sha256sum --check -
```

Stop on a mismatch. Extract without relying on FUSE:

```bash
chmod +x OpenBOR_3.0_6391.AppImage
./OpenBOR_3.0_6391.AppImage --appimage-extract
mkdir -p Paks
ln -s -- "$HOME/Paks/Marvel_Infinity_War.pak" \
  "Paks/Marvel_Infinity_War.pak"
./squashfs-root/AppRun
```

If the PAK link already exists, inspect its target rather than overwriting it. A symlink was used for the manual test to preserve the original PAK. The installer will use its declared content-copy/reuse policy instead.

## Fullscreen and shader

Use the game's Options/Video Options menu to enable fullscreen and select **CRT scanlines TV**. Those choices worked on the target machine. The internal numeric shader value has not yet been decoded from the binary configuration; do not invent CLI flags or patch offsets.

The captured configuration is a 352-byte file:

```text
Saves/Marvel_Infinity_War.cfg
SHA-256: 11d2e516a0b924cb88d2fab1fe940431885d4a838cded8fb02f955989761f43a
```

Use that file as an absent-state seed only. Existing player settings take precedence. Copying a preset on every launch would discard user changes and must not be implemented.

## Controller setup

Connect the controller before launch. In Control Options, confirm **GAMEPADS ENABLED** and open Player 1. Highlight an action with the keyboard, press **Enter to activate reassignment**, release Enter, then press the controller button or direction. Select **OK** to save.

Initially the controller appeared unresponsive, including in mapping. Linux's `jstest` showed changing values, OpenBOR detected one joystick, and the screenshots showed gamepads enabled. Controller mapping subsequently worked after clarifying the reassignment interaction. Neither the classic SDL joystick setting nor a system-SDL preload restored input during the earlier tests; neither belongs in the confirmed launcher command.

Suggested layout using the letters printed on the 8BitDo:

| Action | Suggested binding |
|---|---|
| Move | D-pad, or left stick if preferred |
| Attack 1 | Y, left face button |
| Jump | B, bottom face button |
| Trait | X, top face button |
| Block | A, right face button |
| Helper | L |
| Super | R |
| Start/Pause | Start (+) |
| Screenshot | F12 on keyboard |

This layout was suggested in the session; Jacob's exact physical bindings and choice of D-pad versus stick were not individually confirmed. The captured `.cfg` is the authoritative working preset. Analog-stick mapping and simultaneous D-pad/stick support still need explicit testing.

For diagnosis only:

```bash
cat /proc/bus/input/devices
jstest /dev/input/js0
```

Device names may contain `X-Box`, so a filter searching only `xbox` can miss a detected controller. Never run the engine as root to work around input access.

## State and package requirements

The working archive includes configuration, progress, high scores, and a numbered save file. Only the `.cfg` is intended as an initial settings preset; personal `.sav`, `.hi`, and `.s00` files must not be bundled as defaults. Preserve all player state during reinstall, repair, and game-only removal.

Keep shared engine files separate from game ownership. Track precise managed files and hashes. Uninstall previews by default and stops before mutation if a managed file was edited; it preserves user-state saves/configuration, unknown files and the shared engine, and supports reinstall with retained state. Never recursively remove the test folder or original PAK source.

The private 0.2.0 package keeps the PAK external, using the pinned author-hosted download by default or an explicitly selected, exact-hash offline PAK. There is no game-bundling/finalization step. Fresh installs use `~/Games/marvel-infinity-war`; validated receipt directories remain unchanged without migration.

## Artwork, preview, and attribution

| Asset | Supplied file | Inspection |
|---|---|---|
| Icon | `MIWIcon.png` | PNG RGBA, 426 × 392 |
| Cover | `MIW.png` | PNG RGB, 600 × 900 |
| Preview | `MIW.mp4` | H.264 video, 1920 × 1080; AAC audio; 47.744 seconds |

Preserve these supplied bytes unless a format conversion is necessary and documented. Jacob identified the preview video as his own: credit **Jacob McAllister, preview video creation**. That credit does not assert ownership of depicted game content or soundtrack.

Artwork source supplied by Jacob: https://www.steamgriddb.com/game/5363244

Individual artwork creators and exact asset pages remain unverified because the page could not be retrieved. Do not infer artist names from the game listing.

Game creator: **ZVitor**. Official game information: https://www.zvitor.com/projeto/mfa3.html and https://www.chronocrash.com/forum/resources/marvel-infinity-war.138/

Engine: **OpenBOR Team**, continuation of Beats of Rage by **Senile Team**. Preserve the exact upstream engine license and third-party notices when the release source is available. The supplied capture includes the AppImage but no standalone license text; exact v6391 engine notices are now collected in the package. Complete bundled-library source/notice correspondence remains unverified.

Marvel characters, names, and underlying artwork belong to their respective rights holders. ZVitor's site identifies Marvel Comics and disclaims affiliation with Marvel Comics or Capcom. Exact embedded sprite/music contributor credits are pending review of the game release. This fan game has no inferred commercial publisher. Momentum packaging does not imply endorsement or relicense third-party content.

Jacob requested PAK bundling and stated it is free to distribute. Record that statement as user-provided provenance, not an independently verified creator license. Free availability alone does not establish redistribution rights. Since the PAK is absent, its embedded notices and exact redistribution basis remain unreviewed.

## Evidence and next acceptance checks

**Confirmed manually:** native engine startup, controller operation, fullscreen, selected CRT shader, and progression beyond the tutorial with the supplied 6391 engine. Local log inspection confirms successful loading of the next menu and `porta1.txt`.

**Inspected locally:** working archive inventory, AppImage/configuration hashes, image formats/dimensions, video codecs/duration, and test log transitions. No gameplay was executed in the authoring environment.

**Not yet tested:** complete campaign, reconnect/multiplayer/rumble, exact stick mappings, clean-exit/relaunch persistence, fresh installer configuration seeding, engine provisioning through the runner, desktop launch, uninstall/reinstall, current frontend intake, and PAK finalization.

The current private repositories were read through the GitHub connection. The installer is built against the real Contract 1.0.0 lifecycle and intake, with a companion narrowly scoped OpenBOR runner adapter. No repository ZIP is needed. See the package TEST-REPORT.md and external integration validation for the actual tested scope.

Before marking the package target verified, test fresh installation, existing engine reuse, clean gameplay exit/relaunch, tutorial-to-next-area transition, controller/display persistence, game-only removal and retained-state reinstall. Report MC-01–MC-14 individually, separating static checks, synthetic installer tests, actual installer tests, and Jacob's manual gameplay evidence.

## Installer package produced

The 0.1.0 candidate includes the engine, cfg seed, supplied media, lifecycle scripts, tests and attribution. Its companion runner adapter must be integrated before importing the package. Default destination: `$HOME/Games/Marvel Infinity War`; native shared engine: `$HOME/.local/share/momentum-core/software/openbor/6391/usr/bin/OpenBOR`. The wrapper is generated by installation, changes to the game directory and executes that engine.

Select the directory containing your PAK as the source. Only the PAK is copied, into `Paks/`; originals and other source files remain intact. For a later self-contained release, use the accompanying finalizer to add the original PAK, increment the version, regenerate checksums, run tests/intake and produce a deterministic ZIP with matching runner evidence. Never alter already imported bytes under the same version.

Isolated lifecycle tests now cover seeding, repair, repeated installation, safe removal and retained-state reinstall. Actual packaged gameplay, Applications launch and clean-exit/relaunch persistence remain target acceptance tasks. No remote push was performed.


## Online setup in Momentum — 0.2.0

Import the 0.2.0 installer into Momentum with the current runner/frontend integration. Leave **Download from ZVitor** checked; online contexts may omit `source_dir` entirely and the existing-file folder can be blank. Choose the destination and continue. Review the game-download card and file changes, then choose **Approve and install**. There are no terminal prompts or administrator requests. If the exact engine is missing, its existing separate preparation review appears first. This is the normal frontend approval flow, not an additional terminal gate.

For offline setup, turn **Download from ZVitor** off and choose the folder containing `Marvel_Infinity_War.pak`. Its size and SHA-256 must match the pins below. Originals stay untouched. Online mode extracts only the PAK; the upstream Windows executable, logs, settings and personal state are excluded. Your fullscreen/CRT/controller preset still comes from this package, seeded only when settings are absent.

The pinned author-hosted release is https://www.zvitor.com/Downloads/MIW_v112f3.zip (527,099,513 bytes). Archive SHA-256: `27660c6a6fb0a42aa0e3360412ad2a2c8356bf553737dc3519d82a962130c6d0`. Only `MIW_Definitive/Paks/Marvel_Infinity_War.pak` is extracted, with 587,045,221 bytes and SHA-256 `4b5bbda8432437c13c7ee67d850fc6b24381ba6551c4cd9becb7861348fd2551`. This exactly matches Jacob’s working PAK. Source and hashes are fixed; changed downloads or redirects fail closed rather than substituting another edition.

Allow at least 2 GiB free in both the job workspace and installation destination. Temporary downloads are deleted after completion/failure/cancellation. No network request occurs in preflight, verify or uninstall; repeat installs with intact media need no game download. Repair fetches only when the pinned owned PAK is missing. Downloads have bounded size, a 30-second socket timeout, cancellation checks between reads and a 30-minute overall limit. A failed download does not publish the game; retain the runner’s stage/journal evidence for reconciliation before retrying.

The PAK stays outside the installer ZIP and Git history. No hosted mirror or rolling latest release is used. No current-runner real acquisition or target gameplay certification is claimed by this package task; see TEST-REPORT.md.
