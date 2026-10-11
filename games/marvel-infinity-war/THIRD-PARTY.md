# Third-party attribution and provenance

## Game

**Marvel Infinity War — ZVitor.** Official game information: https://www.zvitor.com/projeto/mfa3.html and https://www.chronocrash.com/forum/resources/marvel-infinity-war.138/. This package pins MIW_v112f3 and its `Marvel_Infinity_War.pak` checksum, matching the supplied historical comparison evidence. Complete embedded music/sprite and contributor credits remain unreviewed and retain their original rights.

Marvel characters, names and underlying art belong to their respective rights holders, including Marvel Comics. ZVitor’s site disclaims affiliation with Marvel Comics or Capcom. This fan game has no inferred commercial publisher. Momentum packaging is not endorsement or affiliation.

The PAK is not bundled or distributed in this installer; approved setup acquires it directly from ZVitor or uses the user's exact offline copy. Historical user-provided bundling authorization is not an independently verified upstream license, and no game rights are conferred by Momentum's license.

## Engine

**OpenBOR Team**, continuing **Beats of Rage by Roel van Mastbergen and Senile Team**. [Official source/release](https://github.com/DCurrent/openbor/releases/tag/v6391). Exact source license notices retrieved at tag v6391 are retained under `upstream/LICENSE` and `upstream/engine-LICENSE`; `engine-README` and the nestegg/SDL notices are retained there too. Do not use the teams’ names to imply endorsement.

The included AppImage was supplied by Jacob after downloading official archive `OpenBOR.v3.0.Build.6391.7z`, member `OpenBOR v3.0 Build 6391/LINUX/OpenBOR/OpenBOR_3.0_6391.AppImage`. Size 4,796,456 bytes; SHA-256 `35895117c2eae94867ee0b094083ae66cd3853372d7447d60cfe92fa929d73eb`. The binary banner says Build pass / compiled December 25, 2020. We extracted only its regular `usr/` files, preserving bytes and normalizing file permissions, into a deterministic tar; `engine/runtime-index.json` binds every file and mode. No engine or library code was modified.

The runtime also carries upstream libraries: SDL2/SDL2_gfx, Vorbis/Ogg, FLAC, libvpx, libpng/zlib, PulseAudio, sndio, X11-related libraries, xkbcommon, libffi, systemd, libwrap, libdbus, libbsd, liblzma, libnsl and others listed exactly in runtime-index.json. Their licenses vary (BSD/MIT/zlib/LGPL and other terms); they are not relicensed by Momentum. Common GPL/LGPL texts are retained in `upstream/` as reference texts, not an assertion that every bundled component has that license or that this alone fulfills every source obligation. Exact library source revisions and a complete component-specific notice/source correspondence remain unverified for this older AppImage. Original engine source is available at the official tag; library source references include SDL, Xiph.org, libvpx, libpng, zlib, PulseAudio, sndio, X.org, xkbcommon, libffi, systemd, dbus and their respective upstream projects. Public binary redistribution compliance for the full dependency bundle needs that remaining review.

## Artwork and preview

Supplied artwork listing: https://www.steamgriddb.com/game/5363244. Exact creators/image pages remain unverified. Credit **Jacob McAllister — preview video creation**, per his statement that the video is his. Underlying game imagery and soundtrack retain separate rights. See assets/README.md.

## Momentum

Installer code/documentation: Jacob McAllister and Momentum Core contributors, under the included MIT LICENSE. This license excludes the game, engine, dependent libraries, artwork, preview media and trademarks.

This is a best-effort attribution record. Unknown credits/permissions are stated explicitly; they are not silently converted into public-domain or unrestricted redistribution claims. No outside rights holder has been contacted.


## Author-hosted game acquisition (retained in 0.2.0)

ZVitor’s game page https://www.zvitor.com/projeto/mfa3.html links the direct `MIW_v112f3.zip` release hosted by ZVitor. The installer fetches this exact release; both archive and PAK checksums are pinned in download_game.py. Verified October 8, 2026 UTC: the PAK matches Jacob’s tested original byte identity. Preserve ZVitor’s game credits and Marvel/Capcom and other original contributors’ rights; download availability does not turn third-party content into Momentum MIT content. No claim of separate permission from underlying rights holders is made.
