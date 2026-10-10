# L.A. Machineguns

Two triggers. One city. Plenty of machines.

## Bring your game

Bring your compatible Japan lamachin.zip. Keep it zipped in its own folder. Game files are not included.

## Install with Momentum

**Add game > L.A. Machineguns > Choose folder > Review > Install.**

Momentum prepares required software after approval, copies your game files, and leaves the originals untouched.

## Controls

Press 3 for a credit and 1 to start. Mouse to aim; left-click or A and right-click or S operate the two triggers. Escape exits. Cabinet service/test: 5 and 6; use only when deliberately calibrating.

## Compatibility

Ubuntu 24.04 x86_64, X11, Japan lamachin ROM, pinned Supermodel 0.3a-20260928-git-8b4de23. Ordinary 1920x1080 fullscreen matches the canonical laptop launcher. The clean calibration seed restored mouse aim on the reference and debug laptops. Other ROMs/builds/layouts are not certified.

On first launch, missing `NVRAM/lamachin.nv` in the isolated state folder is
initialized from the bundled calibrated seed. Existing NVRAM is never replaced,
including on upgrade, repair or reinstall. If an older installation already has
uncalibrated NVRAM, calibrate it through AIM SET; upgrading deliberately does not
reset it. No working laptop NVRAM or scores were imported into the seed.

Your installation remains **setup required** until you confirm gameplay.

## Where it goes

Game files default to `~/Games/l-a-machineguns`.
Settings and saves stay separate in `~/.local/share/momentum-core/state/l-a-machineguns`.
The launcher is `~/.local/bin/l-a-machineguns`; support and backups remain under
`~/.local/share/momentum-core/`.

## Keep it yours

Verification is read-only. Repair restores missing owned files only from their original bytes; modified files are preserved and reported. Uninstall removes only unchanged owned resources, keeping originals, user state, required software and retained support. Reconcile interrupted jobs before retrying.

## Credits and attribution

See [LEGAL-NOTICES.md](LEGAL-NOTICES.md) for original game, software, artwork and mod credits, source links, applicable rights and documented follow-up. Upstream notices remain intact.
