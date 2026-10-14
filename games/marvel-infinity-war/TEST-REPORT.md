# Marvel Infinity War — 0.3.0 validation

0.3.0 changes only where the shared engine lives: it requests the launcher's
build-specific OpenBOR folder (`software/openbor/builds/6391-ef96ad2e3a64`).
Engine, PAK, CFG and artwork pins are unchanged from 0.2.0.

On October 13, 2026, all **49 package unit tests passed** through
`tools/build.py --stamp` (throwaway copy and HOME), with apply proposals
reconciled by the current launcher `ownership.py`, and launcher ZIP intake passed.
New coverage: build-specific runtime path and `"layout": "build"` declaration;
the legacy `openbor/6391` launch path is rejected; an unchanged 0.2.0 wrapper is
replaced with a backup while settings, saves and the legacy engine folder are
kept; an edited wrapper blocks the upgrade unchanged.

Not yet done for 0.3.0: launcher installer evidence, the real upgrade of an
existing 0.2.0 install, and owner gameplay confirmation. The 0.2.0 notes
below remain the history for the shared lifecycle.

## 0.2.0 validation (history)

Contract 1.0.0, installer standard 1.0.1. This report covers the package-side
current Momentum integration, not the historical companion patch or a public
release. Runtime/archive pins are retained unchanged from the supplied private
installer. The game PAK is not bundled.

## Automated scope

On October 10, 2026, all **43 package unit tests passed**, including apply
proposal reconciliation against the actual current launcher `ownership.py`
(via `MCL_LAUNCHER_DIR`). The package inventory self-check passed. Tests emitted
only Python's trusted test-fixture tar extraction deprecation warning.

Run `python3 -B tests/check_package.py` and `python3 -B -m unittest -q` from
`package/` after refreshing SHA256SUMS. Test workspaces are scoped to the game
package's parent and cleaned afterwards. Synthetic PAK hashes are patched only
inside test processes; production offline intake requires the exact release.
Set `MCL_LAUNCHER_DIR` to the current launcher source to additionally reconcile
successful apply proposals using its actual unchanged ownership implementation.

Lifecycle coverage: fresh/repeated install; absent CFG seed and customized CFG
preservation; verify; missing PAK/wrapper repair; exact offline input requirements;
source/runtime tampering; cancellation and refused intents; quoted wrapper paths,
working directory, argument and exit propagation using a stub; retained-state
removal/reinstall; missing managed PAK removal; edited managed content blocks
removal; receipt-authoritative legacy destination without migration.

Online lifecycle tests stub acquisition: omitted source directory, approved
network binding, no preflight acquisition, intact repeat without download, and
missing PAK repair. Downloader tests use small synthetic ZIPs: exact member/hash,
whole-archive/hash mismatches, duplicate members, cancellation/cleanup, oversized
responses and redirects. No test downloads the real game or launches OpenBOR.

The scoped builder refreshed exact SHA256SUMS and current launcher ZIP intake
passed with no platform issues. The deterministic ZIP contains no bytecode;
all supplied runtime, AppImage, index, CFG and artwork/video payloads are
unchanged. Rebuilding uses `--stamp --skip-tests` only after the separate
43-test run above. Intake uses a project-scoped workspace. Intake success
means contract/inventory/media validity, not readiness or gameplay acceptance.

## Remaining integration and acceptance

The parent reports the exact native OpenBOR adapter, omitted online `source_dir`,
and dedicated retained cover/video support are integrated, without ownership.py
changes. Host-library checks use `ldd` on a small verified payload unpacked in
the job workspace before approval/publication, never executing the engine.
End-to-end validation must still cover persisted online/offline inputs across
install, repair and remove, receipt-authoritative destinations, separately owned
engine preparation and the exact verified native executable facts.

Real current-runner online acquisition, offline production-PAK installation,
dependency failure/cancellation/recovery, installed catalog/frontend behavior and
the parent launcher bundle are outside this package task. Target gameplay remains
unverified: controller mapping, fullscreen/CRT shader, tutorial transition, audio,
save/relaunch and clean exit still require manual confirmation. Prior user-confirmed
6391 gameplay and the PAK match are historical evidence only. Installed readiness
remains `setup-required`; no full campaign or gameplay certification is claimed.
