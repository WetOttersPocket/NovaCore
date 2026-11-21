# Changelog

Current release notes take precedence over older claims where behaviour has changed.

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