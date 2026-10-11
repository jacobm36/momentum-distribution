# HOD2 validation and acceptance evidence

Version 0.1.3 changes artwork, documentation, and version-bound fixtures only.
The lifecycle executable code remains byte-identical to 0.1.1. The launcher records
an isolated 0.1.1 install/gameplay test on Ubuntu 24.04 and a specific user Flycast
v2.7 commit. It does not claim a separate 0.1.3 gameplay run or fresh-machine coverage.

**Date:** October 6, 2026  
**Release label:** Build candidate  
**Evidence environment:** Linux x86_64 scratch workspace; Python 3.12, Bash; synthetic CUE/track bytes and a mock user Flatpak command. No original game content was accessed or redistributed. No emulator installation, graphical session or target laptop execution occurred.

## Automated results

`python3 -m unittest` from the package root discovers 22 tests: **21 PASS, 1 SKIPPED**. `python3 tests/check_package.py` also passes without bytecode environment variables or `-B`. The skipped test is optional external `jsonschema` validation, because that test dependency is absent. Runtime uses only the standard library. All protocol JSON files parse; the declared schemas are provided for Copilot's validation, but full schema-library/interoperability validation remains outstanding.

Passed mock checks cover:

- Fresh staging/publication, NDJSON parsing, monotonic intents and result proposal status.
- Repeat install with no new writes; read-only verify; checksum-valid support snapshot usable as package root after import removal.
- Missing media/wrapper repair; version collision, downgrade and out-of-scope receipt rejection.
- Existing unowned destination/integration and modified wrapper conflicts without overwrites.
- Invalid/missing/escaping CUE tracks and symlinked source rejection before installation changes.
- Missing dependency preflight followed by successful runner resolution; apply/bootstrap needs-action without game publication.
- Exact approved-byte digest binding and changed-source conflict before mutations.
- Cancellation before apply and during copying; staged partial work retained; no game publication.
- Running mock Flycast blocks lifecycle work; nonempty/truncated intent file blocks blind retry.
- Runner-helper exits 1 and 2 prevent the corresponding target mutation; helper appends and fsyncs complete records, with no package-side direct writes.
- Backup record/order/content before unchanged-byte executable-mode repair.
- Uninstall preview without installation mutations; applied exact-media removal preserves modified media, unknown saves, copied extra state, shared profile, icon, support and original source.
- Clean removal and reinstall through retained receipt/resources.
- Linux atomic no-replace publication refuses an unexpected existing empty directory.
- Actual generated wrapper execution through the mock captures exact argument array (including forwarded extra arguments after the game path) and working directory from another directory, with paths containing spaces.
- Flatpak 1.14.6-style mock rejects `--show-version`; `LC_ALL=C` metadata parsing handles `v2.7`, unknown version and an actual version mismatch.
- Context intent-helper path, environment fallback and missing-helper failure; exact result outcome values checked in files and final events.

Compatibility check: a synthetic install executed through the repository's actual `mcl_intent.py` helper, and every generated intent passed its validation/sequence checks. This is helper compatibility evidence, not a complete runner/laptop install.

Additional static checks: Bash syntax; Python syntax without cache writes; JSON parsing; exact checksum coverage/snapshot algorithm; real 256×256 PNG with valid chunk CRCs and decompression; safe single-root ZIP and extracted snapshot digest equivalence. See `tests/check_package.py`. Tests use disposable home/media/job directories; none invokes a real Flycast or alters the frontend repo.

## MC-01–MC-14, unchanged gate names

Statuses below are restricted to their stated evidence scope. A mock PASS never means target-verified.

| Gate | Status | Evidence / outstanding work |
|---|---|---|
| MC-01 Complete game contract | PASS — static | Identity, platform, known launch flags, inputs, boundaries, controls and unknown version/BIOS behavior documented. Confirm actual engine flags/version on laptop. |
| MC-02 Valid package | PASS — static | One root, four entrypoints, manifest, helper, docs, checksums, real PNG; supplied protocol schemas parse. External schema validation skipped. |
| MC-03 Content selection | PASS — mock | Explicit selected source validated; receipt-owned destination reused; unsafe/unowned destinations conflict. Packaged-media/default-source precedence is N/A: v1 requires source selection and bundles no disc. |
| MC-04 Existing emulator reuse | PASS — mock | Correct user provider/scope facts reused; package runs no install/upgrade command. Real reuse/version/capabilities still pending. |
| MC-05 Missing emulator setup | NOT TESTED — real | Mock resolver boundary tested; actual official user Flathub installation belongs to runner and has not been exercised. |
| MC-06 Dependencies and failure | NOT TESTED — end-to-end | Mock needs-action, partial stage, approval/source conflicts and helper write/refusal failures pass; real network failure, safe archive intake and runner crash handling pending. |
| MC-07 Safe reinstall | PASS — mock | Unchanged assets reused, user profile/saves retained, edited managed files preserved/conflicted. Real game state persistence pending. |
| MC-08 Launch reliability | PASS — static/mock | Bash syntax; wrapper invoked from another directory through mock with exact argv and spaces. Real emulator exit/launch behavior pending. |
| MC-09 Desktop and art | NOT TESTED — target | PNG validated and desktop generated. Actual menu/icon launch and desktop-file-validator check not available here. |
| MC-10 Gameplay behavior | NOT TESTED — new package | Prior laptop setup confirmed aim/fire/off-screen reload; new package's fullscreen/Start/aim/fire/reload/exit not tested. Right-click reload unverified. |
| MC-11 State persistence | NOT TESTED — target | Existing mock profile and game-internal saves preserved; CLI settings avoid global writes. Fresh actual mappings and exit/relaunch persistence pending. |
| MC-12 Scoped uninstall | PASS — mock | Preview, exact hash-owned removals, modified/unknown state and dependency preservation. Internal state left in place; no folder recursively removed. |
| MC-13 Reinstall after removal | PASS — mock | Clean removed game reinstalled; icon/support and tombstone resources reused. Runner catalog/history behavior pending. |
| MC-14 Documentation and frontend facts | PASS — static | Manifest, README, player guide and protocol profile agree; package never writes catalog or authoritative receipt. Actual frontend profile agreement still required. |

The approved contract amends the older standard: explicit source selection, current-user Games default, dependency resolver ownership/no elevation, distinct lifecycle operations, app-native catalog proposals, retained artwork/support, and preserving unknown files override the old standalone/recursive-removal instructions. No gate IDs or their meanings are redefined.

## Not established by these tests

Safe real ZIP import/trust UI and approval decline; actual schema/runner agreement; shared dependency/user Flathub setup; exact current Flycast CLI capability/firmware/state paths; real .desktop launch; metadata/default/artwork merge and catalog-pending recovery; concurrent GUI edits; real process identity/boot/child recovery; interface quit/reopen while a job runs; power-loss durability on the laptop's filesystem; real game and fresh mappings.

Filesystem fsync calls and mutation ordering are implemented/tested selectively; a physical power-loss test was not performed. Crash intent without outcome remains uncertain and requires reconciliation. No blanket rollback guarantee is made.

## Target acceptance checklist

For additional target coverage, record actual OS/architecture/Flycast version and resolver evidence; test fresh/missing-dependency install, repeat, verify, missing-file repair, edited-file conflict, cancellation/recovery, uninstall preview/apply and reinstall. Check catalog edits/cleared artwork/history survive. The player confirms Start, mouse aim, left-click fire, off-screen reload, crosshair, fullscreen, exit and relaunch persistence. Only corresponding evidence can establish those claims.

## 0.1.4 documentation revision

The README introduction now emphasizes mouse-controlled play. Installer code, launch flags and artwork are unchanged from 0.1.3. Version-bound fixtures and checksums are updated; this revision makes no new gameplay or fresh-machine claim.

## Attribution revision 0.1.5

Documentation/version/fixture-only update from 0.1.4; runtime implementation, payload and artwork remain byte-identical. Attribution sources/upstream notices reviewed October 7, 2026. Earlier gameplay/integration evidence remains scoped to its original revision; new build/self-check/unit/intake results are recorded in docs/attribution-rollout-report.md. No new target gameplay, software installation or fresh-machine certification.

## Folder standard 0.2.0

New-install destination `~/Games/the-house-of-the-dead-2`. Package tests cover the recorded-folder rule: an upgrade whose receipt names an older folder directly inside the games root keeps that folder; any other mismatch is still rejected. A test also covers an existing system-wide Flycast: the generated launcher uses `flatpak info --system` / `flatpak run --system`, and a not-installed system-scope fact is refused (Momentum prepares only user scope). No gameplay or fresh-machine certification claimed.
# 0.3.0 managed-binding candidate - October 10, 2026

Package self-check and 25 lifecycle tests passed, including retained helper
hash/profile checks and managed wrapper generation. Exact source/media and
ordinary user/system paths remain covered. The private runner integration
passed separate engine/game approvals, receipt binding, repeat without file
changes and refusal after descriptor drift using synthetic Flatpak/media.
Real isolated engine boot/VMU persistence is separately scoped in the launcher
fallback evidence; it is not debug-PC controls/gameplay acceptance.
