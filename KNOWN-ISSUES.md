# Known issues — v1.0.2-RC1

This page covers the current RC, not the archived Preview 113–121 builds.

## Confirmed on the owner's PS4

- YouTube Watch plays with picture and sound.
- YouTube Listen plays through Nova Quick Menu.
- The YouTube lookup gets past “Getting the video”.
- Earlier RC testing established Quick Menu on the PS dashboard/in games and AutoRun on the owner's PS4 Slim, firmware 13.02 with GoldHEN. This does not establish compatibility with every console or game.

## Current limits

- The PS button opens Sony's dashboard. For Nova Quick Return: **hold touchpad → Return to Nova → Cross**.
- Nova's own dashboard notification panel is temporarily off. The bell uses Sony's normal list.
- The PS4 hardware video decoder is not active in this RC. YouTube defaults to 480p for smoother playback.
- H.265/HEVC, DRM and video above 1080p are unsupported. Streams depend on their source, format and availability.
- Watch Together is not included.
- A Nova profile picture appears across Nova and Nova friends, but does not replace Sony's system profile picture.
- Nova Play/System Link supports compatible games; it does not provide universal online matchmaking.

## Latest changes needing console checks

- Dashboard becoming the default once, left/right row movement, looping, info-box alignment and remembering a later choice of classic Nova Lab.
- World Radio region/country browsing, live list loading and fallback behaviour.
- Phone-to-TV YouTube sending before opening YouTube in Nova.
- Long titles fitting Quick Menu music cards.
- Clearer helper recovery messages and re-enabling a helper that disabled itself after repeated failed starts.
- Wider firmware/model compatibility, individual game/app launches and media sources.

## If something goes wrong

After updating, open Nova once, **Full Restart**, then enable HEN again. A crash guard switches Nova to safe mode after two early plugin crashes. Do not repeatedly force a crashing feature.

For helper-not-running messages, enable GoldHEN/HEN and restart, then enable HEN after boot. The latest recovery flow can re-enable a disabled helper by pressing Cross on a game again within 15 seconds; restart with HEN afterward. This recovery flow still needs testing.

YouTube fetching can be disabled with an empty `/data/novacore/yt-console.off` file. `/data/novacore/radio-regions.off` restores classic UK Radio browsing.

Logs are under `/data/novacore-lab/`; video uses `video.log`, and YouTube uses `yt/console.log`. Include only relevant, redacted extracts in public reports. Never share credentials or pairing codes. See [how to report](CONTRIBUTING.md).
