# Ultimate Double Dragon 3 — 0.1.0 validation

Contract 1.0.0, installer standard 1.0.1. Built from the Marvel Infinity War
0.3.0 OpenBOR lifecycle with the download path removed: `source_dir` is
required and must contain the exact `UDD_3.0.pak` (1,408,885,949 bytes,
SHA-256 `95000dd09b8e7315c331dfbafec12b40714ea007e3631588f51849ce16a57884`).
The engine runtime, AppImage and runtime index are byte-identical to Marvel
0.3.0 and use the same build-specific folder `openbor/builds/6391-ef96ad2e3a64`.

## Automated scope

Package unit tests run through `tools/build.py --stamp` in a throwaway copy and
HOME. Synthetic PAK hashes are patched only inside test processes. Coverage:
fresh/repeated install; absent CFG seed and customized CFG preservation;
verify; missing PAK/wrapper repair; exact source requirements and wrong-release
rejection; source change after approval; runtime tampering; cancellation and
refused intents; quoted wrapper paths, working directory, arguments and exit
status with a stub engine; retained-state removal/reinstall; edited managed
content blocks removal; receipt-authoritative destination without migration;
build-specific runtime path with the legacy path rejected.

No test launches OpenBOR or uses the real PAK. The owner’s copy of the real PAK
was hashed and matches the pinned size and SHA-256.

## Prior manual evidence

On October 12, 2026 Jacob confirmed on his laptop that UDD 3.0 launches and
plays on native OpenBOR 6391, and that fullscreen, the selected shader and
controller settings persist after restart. The seeded CFG is his current
working file (October 13), which differs from the October 12 capture in one
display/shader byte.

## Remaining acceptance

Packaged installation through Momentum on the target laptop, controller input,
fullscreen/shader, audio, stage transitions, save/relaunch and clean exit still
require owner confirmation. Installed readiness remains `setup-required`; no
full campaign or gameplay certification is claimed.
