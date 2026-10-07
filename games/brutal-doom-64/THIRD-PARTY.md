# Third-party provenance and scope

## Bundled mod

Brutal Doom 64 by Sergeant Mark IV, release v2.0. Author-hosted ModDB page: https://www.moddb.com/mods/brutal-doom-64/addons/brutal-doom-64-version-10 (URL retains the older version-10 slug). Original `Brutal_Doom_64_V2.zip`: 214,514,406 bytes, MD5 `866db5692b2d28564364cd51484d06d3` matches the publisher page; downloaded SHA-256 `550a3ddcf3b9b18663ceb22619c878ebccf4c661c145f2ced8ca31cad1a2ae50`. Downloaded through the page's public ModDB mirror on October 7, 2026 UTC. Checksum is an integrity check, not an author signature.

The four files under upstream `Brutal Doom 64/skins/` are bundled byte-for-byte at `game-data/mods/BrutalDoom64/`. Linux filename capitalization and engine load order match the supplied working guide. All embedded maps, gameplay, sprites, sounds, announcer and music remain inside their original containers. No install-time mod download. `bd64mapsV2.pk3` is a **PWAD** despite its suffix. The gameplay ZIP contains repeated lump names; neither its contents nor their ordering were rewritten.

| File | Bytes | Actual format | SHA-256 |
|---|---:|---|---|
| `bd64gamev2.pk3` | 20,999,627 | ZIP/PK3 | `4bfb1681d76b82c495863a6a4217e96f0ea5769db31073759ddf7169a92fc17b` |
| `bd64mapsV2.pk3` | 70,485,838 | PWAD | `f5898170724ab2b65a3b7251753be8f9afbf8a2bc18a30534ead90ec9465906a` |
| `STAnnouncerPack.pk3` | 13,358,028 | ZIP/PK3 | `730a80c27c8261b9b3713608de89da26bb2aa47e71cc106a5e49d8b09f2aedc1` |
| `ZD64MUSIC.PK3` | 125,856,833 | ZIP/PK3 | `a4ae0348cc0a7c4266b513562c8b5410d6d4882f0fc33fee0adefb18410cbc7e` |

Original `BD64 README.txt` and `CHANGELOG.txt` are retained unchanged in `upstream/` with filename spaces changed to hyphens. The Windows Zandronum engine, its engine support PK3s, DLLs, executables and configuration are not part of the working UZDoom mod set and are excluded. No commercial Doom II IWAD is included.

Credits remain in the upstream README, including Sergeant Mark IV, Kaiser, Nightshade, Kaal979, Cage, Scalliano, Dr Doctor, soundtrack contributors and testing contributors. Installer MIT licensing does not relicense mod assets or music. Bundling follows the user's explicit complete-mod/artwork redistribution instruction; no separate broad asset license is invented.

## Artwork

Supplied `MomentumCore.zip`, `GamesRepo/momentum-core-launcher/media/brutal-doom-64/icon.ico`, decoded at its native 150 × 150 resolution and losslessly converted to PNG. The separate icon named in the setup guide is not asserted to be byte-identical. Original art attribution/license were not supplied for this exact ICO; upstream launcher art credits talisagoat, but authorship of the supplied ICO is not independently established. User-authorized supplied artwork remains excluded from the installer-code MIT license.

## Shared software and input

UZDoom is separately resolved from Flathub (`org.zdoom.UZDoom`), https://flathub.org/en/apps/org.zdoom.UZDoom and https://github.com/UZDoom/UZDoom. No engine binary/runtime is bundled. Doom II IWAD is user-selected, copied without touching the original, and retained on removal. Existing sandbox settings/saves and personal artwork are preserved.
