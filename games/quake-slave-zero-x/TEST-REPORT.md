# Episode Enyo verification scope

## Publisher-download revision 0.3.0

No mod PAK is included in the package. The source declaration pins the publisher
page/upload ID, archive and PAK sizes/hashes. Package checks verify no bundled
PAK; lifecycle tests use a separately supplied synthetic PAK and verify the same
fullscreen, preservation, repeat, repair and removal behavior. The launcher
owns separate approval, publisher download and retained verified source cache.
Earlier acceptance applies to 0.2.2, not automatically to this new installer.

The supplied candidate was adapted to the current Momentum runner and the
working guide's `enyo` layout. No engine/game process is launched by these
automated checks. Installer evidence does not certify gameplay.

## Package checks executed

- Plain-Python package self-check passes without changing the snapshot.
- **19 package tests passed**: synthetic PACK files and mock engine execution
  cover install/repeat, read-only verify, missing-file repair, preservation,
  edited-file conflicts, invalid media, approval/source tamper, cancellation,
  helper refusal, uncertain intents, wrapper argv/cwd/exit, receipt scope and
  retained-save/base-data reinstall.
- Exact supplied mod SHA-256 and PACK structure independently verified:
  277,593,155 bytes, **605 entries**, including `progs.dat` and `maps/start.bsp`.
- The actual bundled mod, artwork, protocol, scripts and documentation are
  covered by `SHA256SUMS`. Safe ZIP intake validates the canonical digest.
- The proposed package-owned engine adapter was replaced with runner-owned
  approved vkQuake preparation; software transaction tests live in the launcher.

## MC-01 through MC-14

| Gate | Evidence scope | Remaining target checks |
|---|---|---|
| MC-01 Complete game contract | Static guide/profile checked | Exact packaged gameplay |
| MC-02 Valid package | Checksums, manifest, PNG, PACK, ZIP intake | None for static intake |
| MC-03 Content selection | Synthetic base data and bundled complete mod | Real user selection |
| MC-04 Existing engine reuse | Exact AppImage bytes; read-only detection | FUSE mounting and Vulkan presentation |
| MC-05 Missing engine setup | Runner-owned separate download approval | Fresh-machine graphical launch |
| MC-06 Dependencies/failure | Tamper/cancel/helper/uncertain-intent tests | Power-loss and graphical failure |
| MC-07 Safe repeat install | Synthetic no-op and edited-file conflicts | Runtime setting persistence |
| MC-08 Launch reliability | Exact guide args, spaces, cwd/exit forwarding | Actual vkQuake launch |
| MC-09 Desktop/art | Valid supplied PNG and absolute desktop entry | Desktop menu/cache behavior |
| MC-10 Gameplay | NOT TESTED for this package | Title, movement, aim/fire, audio, display, exit |
| MC-11 State persistence | Original CFG/SAV/base/unknown files preserved | Real save/load/relaunch |
| MC-12 Scoped uninstall | Exact unchanged managed resources only | Real player installation |
| MC-13 Reinstall after removal | Retained-save/base-data case tested | Runtime save continuity |
| MC-14 Frontend facts | Exact provider/build/package evidence required | User play confirmation |

The launcher verifies only the pinned 1.36.0 AppImage, x86_64 ELF header,
FUSE2 and Vulkan loaders without running the engine. These checks do not prove
FUSE mounting, GPU suitability, fullscreen, input or gameplay. Readiness remains
**setup required**. No HOD2 gameplay evidence is inherited.

The repository's separate installer report records actual runner, public
download and GUI acceptance results. No unrelated working configuration, save,
mod or original game data is changed during testing.

## Attribution revision 0.1.1

Documentation/version/fixture-only update from 0.1.0; runtime implementation, payload and artwork remain byte-identical. Attribution sources/upstream notices reviewed October 7, 2026. Earlier gameplay/integration evidence remains scoped to its original revision; new build/self-check/unit/intake results are recorded in docs/attribution-rollout-report.md. No new target gameplay, software installation or fresh-machine certification.

## Folder standard 0.2.0

New-install destination `~/Games/quake-slave-zero-x`. Package tests cover the recorded-folder rule: an upgrade whose receipt names an older folder directly inside the games root keeps that folder; any other mismatch is still rejected. No gameplay or fresh-machine certification claimed.

## Portable recipe review 0.2.1

Clarifies that the launch wrapper forces only `-basedir` and `-game enyo`; no fullscreen/display override is added. Selected Enyo `.cfg`/`.sav` files may be imported from the chosen game source, but a root `vkQuake.cfg` is not copied. Synthetic tests verify the argv and config-source boundary. Real display/input/gameplay behavior remains unverified.

## Fullscreen startup 0.2.2

The wrapper now adds `-fullscreen` without a resolution override or configuration
write. Pinned vkQuake 1.36.0 video initialization recognizes this flag and gives
explicit `-window` precedence. Mock-engine tests check default argv, forwarding
of `-window`, cwd/exit propagation and unchanged source configuration. These
checks do not certify graphical fullscreen presentation on the target machine.
