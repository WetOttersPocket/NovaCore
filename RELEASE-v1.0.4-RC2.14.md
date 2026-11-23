# 🎮 NovaCore v1.0.4-RC2.14 — Quick Menu input fixes

A small follow-up to RC2.13, targeting the problem where navigating **Nova Quick Menu also moved the game or PS4 dashboard underneath**.

📦 **PKG upload pending:** the owner will attach `NovaCore-v1.0.4-RC2.14.pkg` here. The matching checksum is already attached. This is a **test candidate**—built and regression-tested on PC, with actual PS4 input isolation still awaiting confirmation.

## 🛠️ Changed and fixed

- **Quick Menu takes focus while open**, rather than passing focus through to the background.
- **Buttons and sticks are consumed by the visible menu**, including when a game is behind it.
- **Background dashboard shortcuts are blocked while QM is open**, so its navigation should not trigger Store or other dashboard actions.
- **Closing returns input normally**, including releasing held closing buttons before the background sees them.
- **Failure handling releases focus**, even if removing the menu scene fails. Existing crash guards remain.

The existing Quick Menu layout, Social gamercard, Music controls and return-to-Nova controls are retained. This does not promise to pause the game itself.

## ✅ Included from RC2.13

Friends, requests and messages in Social; green Online indicator and pink Playing line; trophy icons/counts; gamercard focus controls; local MP3 scanning/artwork; independent YouTube setup and Phone Link notifications. The local MP4 file-reader fix candidate is retained—**actual PS4 video playback is still not confirmed**.

![Gamercard design retained from RC2.13](https://raw.githubusercontent.com/WetOttersPocket/NovaCore/main/docs/screenshots/v1.0.4-rc2.13/gamercard-playing-preview.png)

*Generated desktop design preview with demonstration data, retained from RC2.13. The input fix does not redesign the menu; this is not a console screenshot.*

## 📥 Install and test

GoldHEN is required. Keep your last working package and settings. Do not update firmware for Nova.

1. Once attached, download **RC2.14** and its matching checksum from this release's Assets.
2. Install with your usual HEN Package Installer. **Open Nova once**, then fully restart and enable GoldHEN to load the updated helper.
3. **Test on Sony's dashboard first:** hold touchpad, then try D-pad, sticks, L1/R1 and Cross. Only the Quick Menu should respond.
4. Check Social submenu Back, root Circle and touchpad close. Release all buttons; normal dashboard controls should return.
5. Repeat from a **safe pause/menu screen in a game**. Check its menu/camera does not respond to QM navigation, and controls return after closing.

To return to Nova: **hold touchpad → Return to Nova → ✕**. A normal PS-button tap still opens Sony's dashboard.

## 🧪 Test status and known issues

The actual input-hook and scene functions passed computer-side checks for buttons/sticks, background shortcuts, close-release behaviour, failed scene removal and controller ownership. Social Back/Close and gamercard privacy checks also passed. The helper was built twice identically, and all **420 extracted package files** were checked.

**Those checks do not prove that every game's independent controller input is blocked on real hardware.** Please confirm on your PS4 before calling the issue fixed. Stop if input gets stuck or the console freezes; do not repeatedly reproduce it for logs.

Existing playback, startup/USB-game compatibility, Store redirection and phone-delivery checks remain open. See [known issues](https://github.com/WetOttersPocket/NovaCore/blob/main/KNOWN-ISSUES.md). An older PKG may not automatically downgrade a newer resident helper; retain your previous verified recovery files. Do not delete user data, saves or game databases to troubleshoot.

Report the exact build, console model, firmware, GoldHEN version, what was behind QM and which controls leaked. Include a photo and `qm-overlay.log` where available, with private details removed.

## 🔎 Exact package

| Item | Value |
|---|---|
| File | `NovaCore-v1.0.4-RC2.14.pkg` |
| Size | `292,683,776 bytes` |
| Package version | `03.27` |
| Resident helper | `94421` |
| SHA-256 | `34437b4ed641156f584e35f8009a58307a369daf87a8a63f1c8854ef3025c395` |

**No PKG is attached yet.** Upload only this exact build here; RC2.13 has its own release and checksum.

[Full dashboard features and RC2.13 changes](https://github.com/WetOttersPocket/NovaCore/releases/tag/v1.0.4-RC2.13) · [Changelog](https://github.com/WetOttersPocket/NovaCore/blob/main/CHANGELOG.md) · [Discord](https://discord.gg/cjgA8T94E)

NovaCore by **WetOttersPocket** 🦦. Application/plugin source remains private during the RC. Third-party components retain their licences. No private source, configuration or logs are release assets.
