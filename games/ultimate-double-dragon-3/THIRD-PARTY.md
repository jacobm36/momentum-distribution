# Third-party attribution and provenance

## Game

**Ultimate Double Dragon (UDD 3.0).** Credited on its project pages to Mr.Q! (ChronoCrash) and the GalaXiqq OpenBOR / mahcneto project and distribution pages:
https://www.chronocrash.com/forum/resources/ultimate-double-dragon.58/,
https://openborgx.wordpress.com/2024/02/12/ultimate-double-dragon-ver-1-0/ and
https://mahcneto.itch.io/ultimatedoubledragon. This package pins `UDD_3.0.pak` by size and checksum, matching Jacob’s tested copy. Complete embedded music/sprite and contributor credits remain unreviewed and retain their original rights.

Double Dragon names, characters and underlying assets belong to their respective rights holders. Momentum packaging is not endorsement or affiliation.

The PAK is not bundled, downloaded or distributed by this installer; the user supplies their own copy. No game rights are conferred by Momentum’s license.

## Engine

**OpenBOR Team**, continuing **Beats of Rage by Roel van Mastbergen and Senile Team**. [Official source/release](https://github.com/DCurrent/openbor/releases/tag/v6391). Exact source license notices retrieved at tag v6391 are retained under `upstream/LICENSE` and `upstream/engine-LICENSE`; `engine-README` and the nestegg/SDL notices are retained there too. Do not use the teams’ names to imply endorsement.

The included AppImage was supplied by Jacob after downloading official archive `OpenBOR.v3.0.Build.6391.7z`, member `OpenBOR v3.0 Build 6391/LINUX/OpenBOR/OpenBOR_3.0_6391.AppImage`. Size 4,796,456 bytes; SHA-256 `35895117c2eae94867ee0b094083ae66cd3853372d7447d60cfe92fa929d73eb`. The binary banner says Build pass / compiled December 25, 2020. We extracted only its regular `usr/` files, preserving bytes and normalizing file permissions, into a deterministic tar; `engine/runtime-index.json` binds every file and mode. No engine or library code was modified.

The runtime also carries upstream libraries: SDL2/SDL2_gfx, Vorbis/Ogg, FLAC, libvpx, libpng/zlib, PulseAudio, sndio, X11-related libraries, xkbcommon, libffi, systemd, libwrap, libdbus, libbsd, liblzma, libnsl and others listed exactly in runtime-index.json. Their licenses vary (BSD/MIT/zlib/LGPL and other terms); they are not relicensed by Momentum. Common GPL/LGPL texts are retained in `upstream/` as reference texts, not an assertion that every bundled component has that license or that this alone fulfills every source obligation. Exact library source revisions and a complete component-specific notice/source correspondence remain unverified for this older AppImage. Original engine source is available at the official tag; library source references include SDL, Xiph.org, libvpx, libpng, zlib, PulseAudio, sndio, X.org, xkbcommon, libffi, systemd, dbus and their respective upstream projects. Public binary redistribution compliance for the full dependency bundle needs that remaining review.

## Artwork and preview

The icon and preview video were supplied by Jacob, who authorized their inclusion. Creators are not established. Underlying game imagery and soundtrack retain separate rights. See assets/README.md.

## Setup preset

`seeds/UDD_3.0.cfg` is Jacob’s current working UDD configuration (352 bytes): settings only, no personal saves or high scores.

## Momentum

Installer code/documentation: Jacob McAllister and Momentum Core contributors, under the included MIT LICENSE. This license excludes the game, engine, dependent libraries, artwork, preview media and trademarks.

This is a best-effort attribution record. Unknown credits/permissions are stated explicitly; they are not silently converted into unrestricted redistribution claims.
