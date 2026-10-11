# Verification scope

Authoritative guide: Brutal-Doom-UZDoom-Ubuntu-Setup.md.

Build/intake, exact payload hashes/CRCs, PNG decode, synthetic lifecycle and isolated full-payload runner checks are required before publication. Actual results and immutable identity are recorded in docs/uzdoom-three-installer-report.md in the package source repository.

Graphical gameplay: NOT TESTED. No real game/engine invocation, real fresh-machine Flatpak preparation or save/relaunch certification. Historical guide observations do not become new package evidence. 0.2.0 follows the owner-confirmed canonical laptop launcher (base PK3, voxel PK3, Doom Metal WAD); that laptop observation is not package gameplay evidence. Readiness remains setup-required.

## Folder standard 0.2.0

New-install destination `~/Games/brutal-doom`. Package tests cover the recorded-folder rule: an upgrade whose receipt names an older folder directly inside the games root keeps that folder; any other mismatch is still rejected. No gameplay or fresh-machine certification claimed.
# 0.3.0 managed-binding candidate - October 10, 2026

Package self-check and 24 lifecycle tests passed, including retained helper
hash/profile checks and managed wrapper generation. Exact private runner
integration passed separate engine/game approvals, receipt binding, repeat
without file changes and refusal after descriptor drift using synthetic
Flatpak/IWAD. Canonical payload and load order are unchanged. Real UZDoom
vanilla Doom II save/reload is separately scoped engine evidence, not Brutal
Doom graphical gameplay/save acceptance. Debug-PC acceptance remains required.
