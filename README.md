![NovaCore v1.0.2-RC1](https://github.com/WetOttersPocket/NovaCore/releases/download/v1.0.2-RC1/NovaCore-v1.0.2-RC1-Banner.png)

# NovaCore 🦦

A free, customisable PS4 dashboard by **WetOttersPocket**. Your games, media, friends and tools together, with a **Quick Menu that works in Nova, on the PS dashboard and over games**.

**Current release: [v1.0.2-RC1](https://github.com/WetOttersPocket/NovaCore/releases/tag/v1.0.2-RC1)** · Release candidate · Package 03.02 · NOVA00003

**[Download the PKG](https://github.com/WetOttersPocket/NovaCore/releases/download/v1.0.2-RC1/NovaCore-v1.0.2-RC1.pkg)** · [Full release notes](https://github.com/WetOttersPocket/NovaCore/releases/tag/v1.0.2-RC1) · [Changelog](CHANGELOG.md) · [Known issues](KNOWN-ISSUES.md) · [Discord](https://discord.gg/cjgA8T94E)

Public downloads are free. Discord membership, donations and tester reports are not required.

## 🎮 Quick Menu & return to Nova

- **Hold the touchpad for about half a second** to open Nova Quick Menu in Nova, on the PS dashboard or inside a game.
- To get back quickly, open the Quick Menu, select **Return to Nova** and press **✕**.
- A normal **PS button press still opens Sony's dashboard**. Use Quick Menu for Nova Quick Return.
- Control music while playing. Favourite radio, USB/HDD MP3s and YouTube Listens are available through Music.
- Nova Friends, Messages and online shortcuts also connect to the PS dashboard's top bar. The notification bell currently uses Sony's own list.

## ✨ What's new in v1.0.2-RC1

- **Nova Dashboard Home:** weather, games, friends, news and free space, with a looping row for Continue, last music, last video, LAN party, scene news and Nova Online. A see-through info box keeps details beside your selected space. Classic Home remains in Theme → Layouts → Nova Lab.
- **YouTube:** browse, search, Watch on the TV or Listen through Quick Menu over games. No Google sign-in or PC. Personalised picks, phone pairing and your last 20 Listens.
- **World Radio:** 701 checked stations across 72 countries, organised by region and country, plus All stations, artwork, search and favourites.
- **Game cards:** R3 opens play stats, trophies and game tools. Save up to six launch setups per game for patches and GoldHEN options.
- **Phone Link:** files, keyboard input, music controls and save backups over home Wi-Fi. YouTube has its own QR pairing for sending links to the TV.
- **23 Nova achievements, monthly Wrapped, shared themes, profile pictures across Nova and friends**, and news matched to your installed games.

YouTube Watch picture/sound and Quick Menu Listen were tested on the owner's PS4. The latest Home changes, Radio loading, phone sending and other remaining checks are listed in [Known issues](KNOWN-ISSUES.md).

## 🌈 Make the dashboard yours

Choose your startup tab, layout, wallpaper, moving overlay, colours, tile size, motion, name effects, theme music, navigation sounds and PS dashboard glow. Nova Neon comes bundled, and Theme Studio lets you create your own look.

| Area | What you can do |
|---|---|
| **Library** | Browse 13 layouts, including Cover Flow, Tabletop and scrolling Star Wars-style views. Import PS dashboard folders or create your own. L3 flips the case; R3 opens game actions. R3 + △ saves the filter and layout. |
| **Stores & transfers** | Use replaceable FPKGi-format sources, a Di Play store shortcut, the Homebrew catalogue, checked Homebrew downloads, transfer history and Nova update checks. Supply only sources you have permission to use; Nova does not supply pirated games or films. |
| **Media** | NovaFlix rows and featured rotation, your own films with generated posters, M3U/M3U8 playlists, stream URLs, Jellyfin, local/USB media, Nova Cast, captures and file browsing. |
| **Music** | World Radio, favourites, your own stations, MP3s, playback controls and a mini player. Quick Menu music continues over games and the PS dashboard. |
| **Nova Online** | Friend codes, presence, messages, group chat, voice, Nova Play rooms, compatible System Link and Discord linking/Rich Presence setup. Game and service compatibility varies; Nova Play is not universal matchmaking for every game. |
| **Your profile** | Per-user pictures from the bundle or USB, trophies with icons/dates, notifications, activity, achievements and Wrapped. Nova pictures do not replace Sony's system avatar. |
| **Tools** | GoldHEN hub, PS4 Care, files/packages, system controls, scene tools, retro arcade, news, save snapshots, recovery backup, log export and screen recording. Availability depends on the console and enabled services. |

## 📥 Install / update

Test setup: **PS4 Slim, firmware 13.02, GoldHEN**. Wider compatibility is still being tested. **Do not update to firmware 14.00 for Nova.**

1. Download [NovaCore-v1.0.2-RC1.pkg](https://github.com/WetOttersPocket/NovaCore/releases/download/v1.0.2-RC1/NovaCore-v1.0.2-RC1.pkg) and compare its SHA-256 with [SHA256SUMS.txt](https://github.com/WetOttersPocket/NovaCore/releases/download/v1.0.2-RC1/SHA256SUMS.txt).
2. Copy the PKG to USB, or use FTP to place it in `/data/pkg`.
3. With HEN enabled, use **Settings → Debug Settings → Game → Package Installer** to install. Package 03.02 updates v1.0.1-RC1; it uses title ID NOVA00003.
4. **Open Nova once** to set up the bundled dashboard plugin **d46** and auto-start.
5. Do a **Full Restart**, not rest mode, then enable HEN again so the new plugin loads. If your HEN asks you to enable Nova's installed AutoRun payload, enable it in that loader.
6. On the tested startup, expect a brief black screen while the dashboard restarts, three Nova pop-ups, then around **5–10 seconds** on Sony's dashboard before Nova opens. Timing may vary.
7. Hold touchpad to open Quick Menu. It remains available across Nova, games and Sony's dashboard.

Updating does not require deleting saves or your user data. Keep a copy of the previous PKG and your Nova settings before testing an RC. Older preview packages use different identities; their archived installation notes do not describe this RC.

```text
SHA-256  f53460d2190ab81fc2c5edb73a0d90b81112379408a5c67c9c677cf92dc17eb8
```

## 🎬 Playback limits

Streams support HLS, TS, FLV, MKV and MP4, with HTTP/HTTPS, custom ports and Xtream-style URLs. Audio includes AAC, MP3, AC3 and EAC3; seeking is for non-live videos. Local MP4 and HTTPS MP4 retain the original player.

**Hardware decoding is not active in this RC.** YouTube defaults to 480p for smoother playback. H.265/HEVC, DRM and streams above 1080p are unsupported. A recognised format does not guarantee every remote source will play. Watch Together is not included.

## 📸 From the console

![YouTube browsing on PS4](https://github.com/WetOttersPocket/NovaCore/releases/download/v1.0.2-RC1/youtube-console-latest.jpg)

*Actual PS4 capture of YouTube browsing.*

![Nova Quick Menu in a game](https://github.com/WetOttersPocket/NovaCore/releases/download/v1.0.0-RC1/quick-menu-in-game.jpg)

*Quick Menu capture from the earlier RC; its appearance can vary with your theme.*

## 🧪 Help test

Read [Known issues](KNOWN-ISSUES.md), then use **Issues → Bug report**. Include the exact version, PS4 model, firmware, GoldHEN version, steps and outcome. For playback, say whether picture and sound worked. [Reporting guide](CONTRIBUTING.md).

Remove private details from screenshots/logs before sharing. Never post tokens, passwords, pairing PINs, console IPs or stream URLs containing credentials.

## 📜 Credits & source status

NovaCore by **WetOttersPocket**, with LethalLadyT, testers and the upstream homebrew community. [Third-party credits and licences](THIRD-PARTY-NOTICES.md).

This is the public **distribution and reporting** repository. NovaCore's application source remains private during the RC, with open sourcing planned after further fixes. Public binaries do not grant an open-source licence to the app; third-party licences continue to apply.

Optional PayPal: **NovaCore1337@yahoo.com**. Donations do not affect downloads or tester access. 🦦
