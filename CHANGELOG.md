# Changelog

Current release notes take precedence over older claims where behaviour has changed.

## [1.0.4-RC2.13] — 2026-11-23

Release-candidate notes published ahead of the owner's PKG upload. Latest console acceptance pending. Changes below collect the private stages since public RC2.1.

### Added and changed

- **RC2.13:** gamercard Online light and separate pink Playing line using the tracked running game; no activity for hidden/sharing-off profiles. Clear stale activity at worker startup. Same local MP4 input fix asRC2.12.
- **RC2.12:** pinned read-only local media input with64-bit seeking for playback/posters; local errors no longer suggest geo-blocking. Exact reported MP4 metadata and first audio/video frames tested on a computer, not confirmed on PS4.
- **RC2.11:** explicit Nova music-folder scan;300 → 1,000 tracks; Audio>Local files; bounded MP3 embedded art; film embedded cover preference. Gamercard online/hidden indicator, trophy icons/counts, Up card focus/Cross Profile. Closing clears stale panel focus.
- **Phone service:** real Web Push, notification permission/test/off controls, Home Screen instructions, separate private subscription state, paired-phone auth, restart-safe inbox/cursors. No Friends setup required for YouTube. Six push tests +27 regression checks passed; real phone delivery needs testing.
- **RC2.10:** full IPTV.org index rather than Movies-only source; up to 20,000 entries, category ordering, logos/fallbacks, NovaFlix default view, offline/geo flags and per-session failed-channel hiding. Local films sent through FFmpeg; Capture gallery kept separate.
- **RC2.9:** dedicated top-bar Profile/Friends/Messages panels; show requests even with no accepted friends; validated badges/popups after committed sync. Custom HTTP(S), redirects and live-playlist child readers.
- **RC2.8:** Social font-cache/text bounds and42-key layout; M3U metadata/logos; deadline/cancellation checks; Captures removed only from NovaFlix.
- **RC2.7:** top-bar Profile separated from Quick Menu routing.
- **RC2.6:** submenu Back separated from full Close, input lease retained; public-only friend-code projection readable without exposing credentials; bounded network retry and gamercard layout.
- **RC2.5:** complete QM Social actions/live sync candidate; Friends/Profile together, requests/messages/history, inline controller keyboard, privacy/QR linking and chosen pictures; external Store route validation. Find before System.
- **RC2.4:** resident Social cards retained inside existing Quick Menu; fix for immediate focus-guard closing; paging/subpage Back and legacy-toggle-independent action bridge.
- **RC2.3:** executable packaging/layout repair for the malformed private build; one writable memory range and retained build guard; no user-data reset.
- **RC2.2 and preceding private stages:** Friends service update, preserved four-character code issuance with six-character readiness, native identity/requests/list/pictures/privacy, message history/unread notifications,30-day Nova-name cooldown, opt-in player discovery, Discord-link controls, full installed-app Store picker and independent YouTube device setup. Original one-to-one message retention is30days and not E2E. Existing group/voice paths retained rather than claimed reimplemented.

### Retained

Quick Menu over Nova/dashboard/games, touchpad return, music controls, themes/Theme Studio,13 Library layouts, custom start tab, folders/case actions/trophies, six main UI languages, media/Jellyfin/streams/YouTube, radio, tools/news/backups and replaceable stores. Existing privacy/off switches/crash guards remain. Nova's application/plugin source stays private.

### Still under test

Local MP4/live streams; latest startup/USB game launches; Social rendering/back/badges; phone delivery; Store redirection and theme persistence. Sony system avatar writer stays disabled; local Sony-name writing not included; Discord community-member feed not enabled. [Full known issues](KNOWN-ISSUES.md).

## [1.0.4-RC2.1] — 2026-11-21

Experimental public test; owner reports installed and running. Package integrity/identity checked. The preceding test build’s HEN-startup crash cause remains unresolved; this release does not claim a verified startup fix.

### Changed — console checks requested

- Quick Menu Music volume slider at the top, shared radio/media volume and improved theme-colour refresh.
- Top-bar panel closing/icon sizing changes, Nova-tile rotating screenshots, trophy/game artwork extraction, Store app-picker catalogue correction and failed-launch notices.
- Faster Store icon checking and a change targeting the overlapping bottom button bar; brief icon flashes may remain.
- YouTube picture/audio synchronisation, Language at the top of System settings, and Settings What’s new picture cards.
- Older Nova boot-component recognition and backed-up upgrade handling. Automatic HEN startup remains unverified.
- Video wallpaper disabled and wall resources absent from this package; static backgrounds retained. No new nebula overlay included.
- Package 03.08, title ID NOVA00003, dashboard plugin d59 / 94409.

### Languages

- English, Español, Français, Deutsch, Italiano and Português, plus System default, under Settings → System → Language.
- Phase 1 covers main tabs, hints, Settings, Home greetings and Quick Menu blade labels; deeper pages/catalogue content remain English.
- Non-English console behaviour and automatic language detection still need testing; English system detection was confirmed.

### Retained since the last public RC

- Optional Nova Series and Nova Switch layouts, game cards that retain the layout background, Nova Theme 2 and dashboard hover-panel changes. The layouts are almost finished; details still need polishing/testing.
- YouTube, World Radio, phone controls, game setups, achievements, Wrapped and social features.

### Known issues

- Prior HEN-startup crashes remain unexplained. Owner-reported manual operation does not verify automatic startup. Stop after a crash; do not repeatedly reproduce it for logs.
- Store selection, pictures, volume/theme behaviour, bottom-bar hiding and video sync need tests in the final package.
- YouTube defaults to 480p; hardware decoding inactive; Watch Together absent. Firmware 13.52 and non-English languages unconfirmed.

### Server-side

- Nova Online counter uses a 10-minute check-in window; no installation needed for this change.

## [1.0.2-RC1] — 2026-11-19

**✨ Added**
• Nova Dashboard Home with weather, recent activity, looping spaces and an info panel.
• YouTube Watch, Listen, personalised picks and phone pairing.
• Quick Menu YouTube playback and the last 20 Listens.
• World Radio: regions, countries, artwork, search, favourites and All stations.
• R3 game cards and up to six launch setups per game.
• 23 Nova achievements and monthly Wrapped.
• Home-Wi-Fi Phone Link for files, keyboard, music and backups.
• Profile pictures across Nova/friends and theme sharing.
• Personalised news and a Your cheats feed.

**✅ Confirmed working on my PS4**
• YouTube Watch plays picture and sound.
• YouTube Listen plays through the Quick Menu.
• Video lookup gets past “Getting the video”.

**🔄 Changed**
• Media: L1/R1 switches Audio / NovaFlix / YouTube; L2/R2 switches categories.
• Music: Radio / Favourites / My stations / Queue; Audius removed.
• Nova Play is now the Nova Online space on Home.
• The dashboard bell uses Sony’s notification list for now.
• New Quick Menu plugin d46 bundled; restart fully and enable HEN after installing.

**🧪 Needs testing**
• Final Home row movement, looping, alignment and saved layout choice.
• World Radio loading and phone-to-TV video sending.
• Long-title trimming and helper recovery instructions.

**🐞 Known limits**
• YouTube defaults to 480p; hardware decoding isn’t active yet.
• Watch Together isn’t included.
• Nova’s own dashboard notification panel is temporarily off.


## [1.0.1-RC1] — 2026-11-18

### Added

- Quick Menu favourite radio and whole-tree USB/HDD MP3 scanning, with automatic next-track playback.
- My Films rows for internal/USB video, cleaner titles and generated poster thumbnails.
- FFmpeg streaming support for HLS, TS, FLV, MKV and HTTP MP4, plus HTTP/HTTPS IPTV addresses with ports.
- Bundled Nova Neon theme.

### Changed and fixed

- Release compilation and packaging fixes.
- Top-bar panels close when a game takes over or after 45 seconds idle.
- Notification and trophy artwork changes, and an attempt to hide Sony's underlying list. **Superseded in 1.0.2:** Nova's dash notification panel is off; the bell uses Sony's list.
- Hardware-first video decoding was introduced with software fallback. **Current 1.0.2 status:** hardware decoding is not active.

## [1.0.0-RC1] — 2026-11-18

- Custom dashboard, themes, library layouts and folders.
- In-game/dashboard Quick Menu, Quick Return and music controls.
- GoldHEN AutoRun startup, Nova Online, media, tools and profile features.

## Earlier preview builds

Historical notes remain in the repository as `RELEASE-*-DEV.md` and `RELEASE-*-TESTER.md`. Those package names, title IDs and experimental status descriptions apply to their original builds, not this RC.
