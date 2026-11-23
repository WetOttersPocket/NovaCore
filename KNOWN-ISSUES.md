# Known issues — v1.0.4-RC2.14

The RC2.13 PKG remains on its release; RC2.14 has a separate release with installer upload pending. Latest code/build/host tests do not establish PS4 acceptance.

## Playback

- **Local MP4:** RC2.11 failed before decoding on a reported H.264/AAC file. The file's tables were valid. RC2.12/13 use a new pinned,64-bit local reader; exact metadata and first picture/audio frames passed host tests. Console playback remains unconfirmed.
- **Live channels:** current console logs show sources refusing requests and live playlists failing to open segments. The network-reader work is a candidate fix, not a guarantee all streams work. Playback is actively being fixed.
- IPTV.org is a live-channel list, not on-demand movies. Supplied logos may fail or be absent; branded fallbacks remain. Unknown geo restrictions cannot be filtered perfectly before trying playback.
- Refreshed RC2.14 adds **experimental software H.265/HEVC**, up to 1080p SDR, including 8/10-bit input converted to 8-bit output. Actual PS4 playback/performance is unverified; begin with 720p. HDR, DRM and4K remain unsupported. `hevc.off` disables only HEVC. HTTPS MP4 now uses the codec-aware FFmpeg path. MP4 is a container, not a codec guarantee. Hardware decoding and software fallback availability do not prove a given stream plays on PS4.

## Quick Menu, startup and games

- Refreshed RC2.14/helper94422 targets missing current-game status, the long return Launching screen and artwork readiness at boot. Host checks passed, console acceptance pending. Use the refreshed checksum; earlier helper94421 is superseded. Activity requires a successful running-app query and Social refresh. Return changes the completed launch-screen handling, not the underlying system focus API.


- **New report:** QM navigation can also control the dashboard/game underneath. Avoid it during live gameplay until confirmed fixed. RC2.14 is a separate input-focus candidate with host checks passed; console isolation is still unverified. It is not included in the RC2.13 download.

- Back/Close, Social font/keyboard bounds, stale top-bar focus and dedicated Profile/Friends/Messages panel fixes require repeated real-console checks.
- Startup executable-layout repair passed build checks; full HEN/auto-start flow still needs confirmation on the latest complete package. Stop on a crash; do not repeat for logs.
- USB titles failing from Sony's dashboard too have been reported. No database-corruption cause or automatic database repair is claimed. Do not delete/rebuild user data as a workaround without a separate backup/recovery plan.
- A Store press immediately after landing on the tile may still reach Sony's screen. The latest selector/redirect changes need internal/external app testing.
- PS button still opens Sony's dashboard; Nova return is **hold touchpad → Return to Nova → ✕**.
- Nova Play/System Link is game-specific. Universal replacement matchmaking is not included.

## Social and phone

- Friend/request/message operations need the service and enabled components. Latest badges and empty-list request fixes need two-tester validation.
- Game activity uses Nova's existing tracked running title; it does not identify every unrecognised app. Missing/unshared activity is hidden. Trophy totals require a Nova trophy refresh; unavailable totals show a dash.
- Nova display-name changes are limited to once per 30 days. This is not a PSN Online ID change. Sony local-name writing is not implemented; Sony profile-picture writing remains disabled pending its separate spare-profile test.
- Discord community-member feed is not enabled. QR linking does not expose all Discord friends or grant unsupported console SDK access.
- Messages pass through the server, are not end-to-end encrypted and are kept there up to 30 days.
- Real phone push service is live, with permission required. On iPhone install to Home Screen; browser/OS settings can block delivery. The closed-page delivery check still needs a real phone. Push does not auto-approve playback.

## Other

- Six languages cover the main UI; deeper pages/source content can remain English. Wider language/firmware/model testing is pending;13.52 is not confirmed.
- Some optional Series/Switch/Console Mix views and theme persistence remain under polish/testing. Earlier nebula previews are not proof of inclusion in a particular package.
- Generated images are design previews; do not treat them as hardware test results.

Keep previous builds/settings. Do not publish credentials, pairing state or private messages. See [test checklist](docs/TESTING-RC2.13.md). Historical [RC2.1 issues](docs/archive/KNOWN-ISSUES-RC2.1.md) are retained.

## New usability checks

Library category overrides, revised R3 menu and Help controls have passed host checks; test persistence, user separation and Circle/QM ownership on PS4. No category/source metadata or Sony game database edits are made. Latest optional orbisRPC 1.1 files are bundled and verified; the shared in-Nova/independent-ShellUI token-transfer wizard remains **unimplemented**. Preparing the bundle does not install, run or connect RPC.
