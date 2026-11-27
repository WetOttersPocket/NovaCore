# NovaCore changelog

## [1.1.0-rc.17] — 2026-11-27 (DEV build, package 03.51, helper 94441)

Fixes from the testers' notes on rc.15 and rc.16, plus the Nova Updates fixes from rc.16, which was never released. Console-unverified.

- New: one set of controls on every page. L2 / R2 move through the main tabs along the top and do nothing else, on Media too. L1 / R1 move through the tabs inside the page you're on and never jump to another main tab. The D-pad and left stick move around inside the tab. Off switch: /data/novacore-lab/strict-controls.off.
- Fixed: Library categories couldn't be reached with the shoulder buttons, because L1 / R1 and L2 / R2 both changed the main tab. L1 / R1 now step through the categories.
- New: L1 / R1 also switch the Settings tabs (Left / Right still work), Audio / NovaFlix / YouTube on Media, the News filters and Games / Recent on Trophies. Pages that already had their own tabs (Homebrew, Transfers, Nova Play, GoldHEN, Themes, the Store) keep them on L1 / R1.
- The hint bar at the bottom always shows L2 / R2 for the main tabs and what L1 / R1 do on that page. L2 / R2 no longer skip songs on Audio or change rows on Media; use the D-pad for rows.
- Fixed: the clock could still be wrong outside the UK. Nova now reads the time the PS4 itself shows and adds it to UTC every time, and it writes what the PS4 reports to /data/novacore-lab/clock-debug.txt, so a wrong clock can be traced from the logs. Off switch: /data/novacore-lab/clock-tz.off.
- New: Settings > System & About > Time zone fix. Leave it on Auto. If the clock is still wrong, X sets how many hours ahead of or behind UTC you are, and pressing on past -1 h and 0 goes back to Auto.
- New: a new top bar. Your picture and Nova name sit at the left end with the NovaCore logo next to your name, and the profile and trophy buttons sit beside a bigger clock at the right. Off switch: /data/novacore-lab/topbar-card.off.
- Fixed: Download on the Nova update card said "Busy. Try again in a minute." whenever Nova had checked for updates in the last minute. It now starts straight away; it only waits while a check is still running, and then says so.
- New: Left / Right move between Download (or Install), Later and Check again on the Nova update card, and X presses the one that is lit. Before, only X and Square did anything.
- Fixed: the notes in Settings > Nova updates overlapped and cut off after two lines. Each note now gets the lines it needs, and the GitHub notes wrap instead of stopping at one line.
- Carries everything from 1.1.0-rc.15 and 1.1.0-rc.16. Helper 94441 is unchanged.

## [1.1.0-rc.16] — 2026-11-27 (DEV build, package 03.50, helper 94441)

Fixes for Nova Updates found while installing rc.15 in place. Console-unverified.

- Fixed: Download on the Nova update card said "Busy. Try again in a minute." whenever Nova had checked for updates in the last minute. It now starts straight away; it only waits while a check is still running, and then says so.
- New: Left / Right move between Download (or Install), Later and Check again on the Nova update card, and X presses the one that is lit. Before, only X and Square did anything.
- Fixed: the notes in Settings > Nova updates overlapped and cut off after two lines. Each note now gets the lines it needs, and the GitHub notes wrap instead of stopping at one line.
- Carries everything from 1.1.0-rc.15. Helper 94441 is unchanged.

## [1.1.0-rc.15] — 2026-11-27 (DEV build, package 03.49, helper 94441)

Fixes from the testers' notes on rc.14, and the first Nova update that consoles on rc.14 can install in place from Nova Updates. Console-unverified.

- Fixed: Friends, Nova Online and the Discord QR code stopped with "Couldn't securely save Friends setup" on consoles that had never set up Friends. The PS4 refuses the kind of file link Nova used to save the first Friends file (the same cause as the old database-backup error), so Nova now saves it another way. Friends you already have are untouched.
- Fixed: the clock showed the wrong time outside the UK (it was UTC). Nova now uses the PS4's own time zone and summer time on every clock. Off switch: /data/novacore-lab/clock-tz.off.
- New: 12-hour or 24-hour clock. Settings > System & About > Clock: Follow PS4, 12-hour or 24-hour.
- Fixed: Circle on a "Press X again" prompt (for example Clear artwork cache) now cancels it instead of going back to Home.
- New: a short touchpad press goes back to Home from any page. Holding the touchpad still opens the Quick Menu, and Circle stays Back and Cancel. Off switch: /data/novacore-lab/touchpad-home.off.
- New: L2 / R2 move through the main tabs on every page. On Media they still switch Audio, NovaFlix and YouTube. Off switch: /data/novacore-lab/l2r2-main.off.
- Fixed: Settings > Library & Media > Library navigation sound sent you to an old Nova app instead of switching the sounds. It now turns Nova's navigation sounds on and off.
- Fixed: the first-time setup. Every press counts (quick presses were dropped), Left / Right pick a colour, one X saves it and moves on, and one X finishes setup. Skipping setup still asks twice.
- Fixed: unlocking a Nova achievement no longer makes the dash stutter. Nova shows its own achievement card; the extra PS4 system pop-up is off unless you create /data/novacore-lab/ach-system-popup.on.
- Fixed: the profile and trophy buttons, your picture and your name at the top right have more room and no longer run into the clock.
- New: a dark Quick Menu. Settings > Appearance > Quick Menu style: Light or Dark.
- Carries everything from 1.1.0-rc.14. Helper 94441 is unchanged.

## [1.1.0-rc.14] — 2026-11-26 (DEV build, package 03.48, helper 94441)

The last update you install by hand: from here on Nova updates itself in place. Also Nova Link's home pages in the app's look, Nova Link installs without a TV prompt, a red update dot, FPKG database Repair that can actually run, and a dash helper that can't hold up Restart or Power off. Console-unverified.

- New: Nova Link's home pages match the app. Games, Sleep, Status, Gallery and the media remote open from the Nova Link tiles with the same look as the app. A paired phone skips the second PIN; the 4-digit PIN stays as a fallback. Home Wi-Fi only.
- New: each of those tiles opens the right screen (/home#games, #sleep, #status, #gallery, /remote). An older Nova build still opens the home or remote page, and may still ask for the PIN until you install this one.
- The PS4 still asks before it starts a game, deletes a package, or goes to rest or powers off.
- Nova Link features stay on by default. Off files under /data/novacore-lab/ (phone-link.off and the nl-*.off files) and the two-crash guards are only safety nets.
- New: packages from your phone install straight away. When Nova Link sends a PKG, Nova downloads and checks it, then hands it to the PS4 installer with no X press on the TV. Off switch: /data/novacore-lab/nl-autoinstall.off.
- New: a red dot when a Nova update is waiting. It shows on SETTINGS and on Settings > Nova updates while an update is available, downloading or ready, until you install it or choose Later. Off switch: /data/novacore-lab/update-badge.off.
- New: Nova updates install in place. Press Install and Nova closes; the dash helper checks the package again, removes the old Nova, installs the new one and opens Nova again. No more deleting Nova by hand, and your settings, themes and fonts stay. Works from the update after this one, once the PS4 has restarted with dash helper 94441. Off switch: /data/novacore-lab/helper-update.off.
- Fixed: FPKG database recovery only ever got as far as the scan. The backup step works since rc.13, each step now shows a tick, and Repair checks GoldHEN's BinLoader first (GoldHEN ships it switched off). If it is off, X twice switches it on in GoldHEN's settings for you; after a restart and HEN load, Repair runs.
- Fixed: Community fonts kept on the Nova server showed no example until you downloaded them. Nova now fetches the checked font file in the background so every card shows the font itself (`community-font-preview.off`).
- Fixed: the dash helper could hold up Restart or Power off while it was busy (for example waiting on the network). It now lets go after 1.5 seconds, and it stays completely idle if the Nova app has been deleted (dash helper 94441).
- Carries everything from 1.1.0-rc.13. Helper 94441 replaces 94440.

## [1.1.0-rc.13] — 2026-11-26 (DEV build, package 03.47, helper 94440)

Fixes from the rc.12 test, on top of rc.12. The first build offered to consoles through Nova Updates. Console-unverified.

- Fixed: Create and verify database backup (Tools > FPKG database recovery) stopped with "Backup read-back failed. Repair refused." Nova now saves each backup file the plain way and reads every file back to check it. If anything still goes wrong, the message says which file and why.
- New: your Nova name at the top right. The name you set now shows there, on Nova Series pages and on your Quick Menu profile, instead of your PSN name.
- New: community theme wallpapers on the cards. Each theme in Community shows its own wallpaper behind its name, so you can see what you're getting. Off switch: /data/novacore-lab/community-art.off.
- New: a full view of a community theme. X opens it big, with its wallpaper, colours and creator; Square installs it and Circle goes back. Off switch: /data/novacore-lab/community-view.off.
- New: a Text fonts tab in Community, beside Title fonts. Text fonts change the smaller text (menus, lists, buttons and descriptions) and Title fonts change the big titles and headings; every card says which. 39 new text fonts from the Google Fonts collection, including Inter, Roboto, Open Sans, Montserrat, Atkinson Hyperlegible and JetBrains Mono. They live on the Nova server and download when you get one, so Nova itself stays small. Off switch: /data/novacore-lab/community-textfonts.off.
- New: a download bar in the "Get this font" box. It fills while Nova downloads (or checks) the font and adds it to My fonts, then the box closes by itself. Both buttons in the box are now easy to read on every theme.
- Fixed: a theme you shared in Community said "Made by NovaCore" when you started it from a built-in theme. New uploads carry your Nova name, and your older uploads show it on your PS4.
- Carries everything from 1.1.0-rc.12. Helper 94440 is unchanged.

## [1.1.0-rc.12] — 2026-11-25 (DEV build, package 03.46, helper 94440)

Fixes from the rc.11 test, on top of rc.11. Console-unverified.

- Fixed: H.265 (HEVC) videos stuttered while H.264 played smoothly. H.265 now decodes on 5 threads instead of 2, and above 720p the frames nothing else depends on skip the extra smoothing pass, as H.264 already does. Off switch: /data/novacore-lab/hevc-boost.off.
- Fixed: sharing a theme with a big wallpaper failed. Nova now shrinks the wallpaper to a JPEG of at most 1 MB (up to 1920x1080) for the upload copy only; your theme on the PS4 keeps its original picture. Off switch: /data/novacore-lab/wall-shrink.off.
- Theme uploads write the wallpaper size and the server's answer to Nova's log, so a failed upload says why.
- New: L2 and R2 badges on either side of the Media tabs (Audio, NovaFlix, YouTube), so you can see which buttons switch them.
- Carries everything from 1.1.0-rc.11. Helper 94440 is unchanged.

## [1.1.0-rc.11] — 2026-11-25 (DEV build, package 03.45, helper 94440)

Your requests from the rc.10 test, on top of rc.10. Console-unverified.

- New: L1 / R1 move through the top tabs everywhere again, Media included, and L2 / R2 switch between Audio, NovaFlix and YouTube. The hint text under the Media tabs is gone. Off switch: /data/novacore-lab/media-l2r2.off.
- New: Square on the Audio page steps through the sources (Radio, Favourites, Local music, My stations, Queue, Playlists) and then the bottom bar (Local media, Nova Cast, Jellyfin, Captures, Add station; X opens it). On a track or station Square adds it to a playlist. Off switch: /data/novacore-lab/audio-square.off.
- New: Save to playlist in a YouTube video's menu, next to Watch and Listen.
- New: getting a font in Community > Fonts opens a small "Get this font" box instead of jumping to Theme Studio. The font goes into My fonts, and Theme Studio's font lists show only None, Bebas Neue and My fonts. Off switches: /data/novacore-lab/font-popup.off, /data/novacore-lab/my-fonts.off.
- New: a Text font row in Theme Studio. It changes Nova's normal text (menus, lists and descriptions), not just the big headlines. Off switch: /data/novacore-lab/text-font.off.
- New: 19 text fonts in Community > Fonts: Poppins (Light, Regular, Medium), Lato (Light, Regular), Carlito (Regular, Bold), Liberation Sans, Serif and Mono (Sans and Serif also in Bold), DejaVu Sans, Sans Condensed, Serif and Sans Mono, Source Code Pro, Lora and Caladea. Every font card now says what it is for: headlines, text, or both.
- Fixed: a playlist no longer plays a favourite station after a song. Playlist songs play once and Nova picks the next song itself (dash helper 94440). Off switch: /data/novacore-lab/radio-once.off.
- Community themes can have wallpapers up to 5 MB (was 1.1 MB). The community server needs its matching update before uploads over 1.1 MB go through.
- Carries everything from 1.1.0-rc.10. Helper 94440 replaces 94439.

## [1.1.0-rc.10] — 2026-11-25 (DEV build, package 03.44, helper 94439)

Fixes from the rc.8 console test, on top of rc.9. Console-unverified.

- New: Playlists in the Quick Menu's Music tab. Pick a playlist and play its songs, with next and previous. MP3s and radio play as they are; YouTube songs play when Nova has saved their sound. Off switch: /data/novacore-lab/qm-playlists.off.
- Fixed: Media no longer jumps to Pulse. L1 on the first Media page, R1 on the last one and L1/R1 while a video plays now stay in Media, as Themes does since rc.9. Off switch: /data/novacore-lab/media-edge.off.
- Fixed: the PS Store "update needed" screen. The helper holds the Store tile's focus for 1.5 s when the focus blinks off, so X opens the Store through Nova. Off switch: /data/novacore-lab/store-sticky.off.
- Fixed: the top bar popping up while you scroll the main tiles after closing it with O. It now only opens after a recent Up press. Off switch: /data/novacore-lab/toprow-recentup.off.
- Fixed: Nova Link's two-crash guards now check only the first minute of each session. Before, they restarted every minute, filled the log and could switch a feature off for a later crash.
- Carries everything from 1.1.0-rc.9, including the Themes Community L1/R1 fix, Nova Link and playlists. Helper 94439 replaces 94438.

## [1.1.0-rc.9] — 2026-11-25 (DEV build, package 03.43, helper 94438)

Navigation fix on rc.8; its feature set and unchanged helper are carried forward. Console-unverified.

- New: dedicated L1/R1 navigation for Layouts & Themes. Community stays in the theme browser instead of jumping to News; Theme Studio and open theme dialogs consume the buttons without changing the page.
- Fixed: playlist picker and keyboard inputs cannot switch the underlying page. Shoulder inputs stay captured while the picker is open and briefly after adding or cancelling.
- Carries every rc.8 feature, including Nova Link, playlists, Community sharing and likes, and the existing update system. Helper 94438 is unchanged.

# Changelog

Current release notes take precedence over older claims where behaviour has changed.

## [1.1.0-rc.8] — 2026-11-25 (DEV build, package 03.42, helper 94438)

Nova Link build on top of 03.41: Phone link starts by itself, and your phone gets a PKG manager, a media remote and Nova Link at home (start games, sleep timer, open links, status, gallery, alerts and bug reports). The YouTube wall opens on Popular now and music again. The dash helper is unchanged (94438). Console-unverified.

- New: Phone link starts by itself, so every Nova Link feature works on your home Wi-Fi without a trip to Settings. Its address and PIN are in Settings > Phone link, and turning it off there is remembered. Off switch: /data/novacore-lab/phone-link.off.
- New: Nova Link PKG manager. Update your homebrew from Nova's own list and tidy old .pkg files in /data/pkg from your phone. The TV asks "Delete this file?" before anything is removed. Off switch: /data/novacore-lab/nl-pkg-extras.off.
- New: a media remote on your phone. Play / pause, back and forward 10 s, previous and next, volume, and what's playing with its picture, for NovaFlix, YouTube and Radio. It works on your home Wi-Fi while Nova is on the TV. Off switch: /data/novacore-lab/nl-remote.off.
- New: start a game from your phone, with a launch profile if you have one. The TV asks "Start this game?" first. Off switch: /data/novacore-lab/nl-launch.off.
- New: sleep timer from your phone. Rest mode in 15, 30, 60 or 90 minutes, or after this game, and the TV counts down for 60 seconds first so anyone playing can cancel. Off switch: /data/novacore-lab/nl-sleep.off.
- New: open links from your phone. Send a YouTube or direct video link and it plays on the PS4 after you say yes on the TV. Other web pages don't open on the PS4 yet. Off switch: /data/novacore-lab/nl-openlink.off.
- New: your PS4 on your phone. See the Nova version, free space, how long it has been on, the last install and your biggest games, and save your screenshots and clips to the phone. Off switches: /data/novacore-lab/nl-status.off and /data/novacore-lab/nl-gallery.off.
- New: phone alerts and bug reports. Pick which alerts reach your paired phone (Nova achievement, install finished, Nova update ready, a feature switched itself off); the pop-up only says your PS4 has news. One tap saves Nova's logs to your phone with tokens, PINs, friend codes and user names hidden. Off switches: /data/novacore-lab/nl-alerts.off and /data/novacore-lab/nl-bugreport.off.
- Nova Link phone page: a slow, blurred cyan, pink and navy background moves behind the cards. It pauses when the page is hidden, stays still if your phone asks for less motion, and has a Moving background switch.
- YouTube: the wall opens on Popular now (the most-viewed recent videos), then the music rows, then Picked for you from what you watch and listen to, then Watch again.
- Every Nova Link feature is on by default and has a two-crash guard: if Nova stops twice in a feature's first minute, that feature switches itself off and the rest of Nova carries on.
- Carries everything from 1.1.0-rc.7 (03.41): Playlists, the video player bar, Community sharing and likes, and NovaLink Send PKG on by default.

## [1.1.0-rc.7] — 2026-11-25 (DEV build, package 03.41, helper 94438)

Feature build on top of 03.40: Playlists in Music, a control bar in the video player, one-press theme sharing and real likes in Community, and NovaLink Send PKG on by default (Nova still asks on the TV before anything installs). The dash helper is unchanged (94438). Console-unverified.

- New: Playlists in Music. Make, rename and delete playlists, play all, shuffle, repeat one or all, and move or remove songs. Songs can come from your HDD or USB, radio, Jellyfin and YouTube.
- New: a control bar in the video player for films, your own videos and YouTube: previous, back 10 s, play / pause, forward 10 s, next, volume, and a seek bar with time, length and how much has loaded.
- Add to playlist from the music page, a YouTube video, the Quick Menu's Music tab and the video player. Playlists are kept on the console and survive restarts.
- Playlists: YouTube songs are fetched fresh each time they play. A file that has moved is skipped with a note. Deleted playlists go to Recently deleted, where you can bring them back.
- Video player: pick the audio track when a video has more than one. The bar hides after 4 seconds and comes back on any button.
- Playlists and the video player bar each have their own off switch: /data/novacore-lab/playlists.off and /data/novacore-lab/player-controls.off.
- New: share a theme in one press. Community > My uploads > Share a theme shows which of your themes goes up (Square picks another). X, then X on "Share this theme with everyone?", and a progress sheet ends with "Shared!" or says why not. With no saved theme, X opens Theme Studio with "Save and share with the community" ready. Off switch: /data/novacore-lab/community-share1.off.
- New: real likes on community themes. Square likes or unlikes a theme: one like per console, counts come from the Nova community server and stay after a restart, and you can't like your own. Until likes are switched on on the server, Nova says so instead of showing a fake like. Off switch: /data/novacore-lab/community-likes.off.
- Community: no demo themes. An empty store no longer shows sample cards; it says "No community themes yet. Be the first to share one." with a Share button, and shows plain Loading and server-down messages. Off switch: /data/novacore-lab/community-nodemo.off.
- Community: smoother page. The theme grid scrolls past four cards, every upload in My uploads can be reached, Triangle refreshes the same page, messages wrap inside the side column and the card button says Install. Off switch: /data/novacore-lab/community-polish.off.
- New: NovaLink Send PKG is on by default. Nova still asks "Install this package?" on the TV, and nothing installs until you confirm. An earlier Off in Settings stays off. Off switch: /data/novacore-lab/pkg-send.off.
- Carries everything from 1.1.0-rc.6 (03.40): the Quick Menu takes the controller over games, in-app updates check GitHub, rounded Home card corners, the top bar only on the dash.

## [1.1.0-rc.6] — 2026-11-25 (DEV build, package 03.40, helper 94438)

Fix build on top of 03.39: the ShellUI top bar only on the PS dash (the Quick Menu still opens everywhere), the controller stays with the open menu and the game under it stops moving, Nova starts on the Default tab and in-app updates really check GitHub. Console-unverified.

- New: the PS dash top bar only answers on the dash. Nova checks which screen ShellUI has in front, so X in HEN, Debug Settings, Package Installer, the Store, games or the power screen goes to that screen again and never opens a Nova top bar panel. The left-stick top bar fix still works on the dash. Off switch: /data/novacore-lab/fg-gate.off.
- New: an open Quick Menu or top bar panel keeps the controller you are using, so the dash underneath no longer moves while you navigate it. Off switch: /data/novacore-lab/qm-pad-owner.off.
- New: Nova starts on your Default tab. An "open Nova on a tab" request left behind while Nova was closed (more than 45 s old) is ignored, so the first start no longer lands on Notifications. Off switch: /data/novacore-lab/open-stale.off.
- Quick Menu: opens everywhere, as in 03.39 - hold the touchpad (or use Nova's Quick Menu button) in games, apps, HEN, the Store or on the dash. Only the top bar's own routes (X on a top bar icon, the Store or What's New tile) wait for the dash. Off switch for those routes: /data/novacore-lab/fg-gate.off.
- New: the game no longer moves under the Quick Menu. While the menu is open over a game or app it takes the controller, the same way the PS4's own menu does, and gives it back the moment the menu closes. If anything stalls it hands the controller back by itself within 3 s. Off switch: /data/novacore-lab/qm-game-input.off.
- Updates: in-app updates really check GitHub now. 03.37 to 03.39 were built as "Public test", so Settings > Nova updates said "only in DEV builds" and Nova never looked for an update. Nova also no longer offers the version you already have, or an older one unless the signed update is marked ROLLBACK. Off switch: /data/novacore-lab/ota.off.
- Home: rounded cards keep their round corners. The Video, Music, News and Nova Online pictures, their dark fade and the focus light now follow the card's own corner radius, also with a rounder theme, when a card is focused and while a picture loads. Homebrew store tiles and banners do the same. Off switch: /data/novacore-lab/tile-corners.off.
- Carries everything from 1.1.0-rc.5 (03.39): YouTube fresh links and clear errors, hover pictures, power-off guards.

## [1.1.0-rc.5] — 2026-11-25 (DEV build, package 03.39, helper 94435)

Fix build on top of 03.38: YouTube refused links (fresh links, clear errors) and PS dash hover pictures. Console-unverified.

- New: YouTube keeps playing when a link is refused. If YouTube refuses the video or sound link part-way (HTTP 403), Nova asks for fresh links and carries on from the same spot, up to twice per link. Off switch: /data/novacore-lab/yt-403.off.
- New: clear YouTube errors. A link YouTube still refuses ends with "YouTube stopped sending this video (HTTP 403)" instead of "Video finished", and a refused sound link stops with an error instead of playing silent video. Off switch: /data/novacore-lab/yt-403.off.
- New: PS dash game tiles show their own pictures again. While a game's picture loads, the hover box stays empty and fills in a moment later; it no longer keeps the What's New or news picture. Off switch: /data/novacore-lab/hover-picfix.off.
- PS dash: a normal power-off can no longer switch off the What's New icon or the hover box. The icon needs two failed starts (was one) and both crash counts clear after 60 s of normal running. Off switch: /data/novacore-lab/d64-guards.off.
- YouTube server: the resolver (2026.11.25-1, already live on the Nova server) checks each link and renews the visitor id when YouTube refuses it. No console change needed.
- Carries everything from 1.1.0-rc.4 (03.38).

## [1.1.0-rc.4] — 2026-11-25 (DEV build, package 03.38, helper 94434)

Fix build on top of 03.37: first-start traces, no second helper, top bar, IPTV headers, Community fonts and upload, faster What's New hover. Console-unverified.

- New: Community fonts show in their own font. Each specimen is drawn in that font; at most 4 are kept in memory. Off switch: /data/novacore-lab/community-fonts-live.off.
- New: Upload card in Community > My uploads, with clear steps and a plain message when the community server isn't available. Off switch: /data/novacore-lab/community-nav2.off.
- New: per-channel playlist headers. IPTV channels that need their own User-Agent or Referer (#EXTVLCOPT or url|User-Agent=...) now send them. Off switch: /data/novacore-lab/stream-headers.off.
- Community: every button now lands on the right screen. O goes back one step, Up reaches the tabs and + Create a theme, and X on a font opens Theme Studio with that font. Hints follow the focus.
- Theme Studio: the headline font list starts with a real "None" (standard Nova text) that clears the choice. Off switch: /data/novacore-lab/font-none.off.
- Top bar: the stick now works like the d-pad (past 0.45 counts as Up/Down). Off switch: /data/novacore-lab/toprow-stick.off.
- Top bar: opens when the PS4 can't say whether a game has focus. Off switch: /data/novacore-lab/toprow-focusunknown.off.
- PS dash: hovering What's New, the Nova tile or your profile row no longer stutters. Pictures and files are read off the drawing thread. Off switch: /data/novacore-lab/wn-perf.off.
- Home: Nova no longer loads a second home-screen helper while the running one is busy. Off switch: /data/novacore-lab/shellui-fallback-guard.off.
- First start: every boot step is written to novacore-lab-boot.txt, and a root window that didn't open is retried once. Off switches: boot-steps.off, boot-root-retry.off.
- Every change has its own off switch, and two unfinished runs switch it off automatically (<name>.disabled).
- Carries everything from 1.1.0-rc.3.

## [1.1.0-rc.3] — 2026-11-25 (DEV build, package 03.37, helper 94433)

Combined DEV build: in-app updates from GitHub, NovaLink Send PKG, a new boot animation, plus update notes in every build. Console-unverified.

- Settings > Nova updates now shows this console's own NovaCore version (NOVA00003), not the old Nova title.
- Every build carries its own update notes ("In this build"), so they show even offline. PS dash: hover the Nova tile for this build's new features; What's New scrolls 20 live Nova Pulse stories.
- Latest GitHub release notes appear on the same page when online (information only).
- New: signed in-app updates from GitHub releases (dev channel). Nova checks at start and every 6 hours.
- Only updates signed with WetOttersPocket's key are accepted; size and SHA-256 are checked before anything installs.
- WetOttersPocket's update signing key is now built in (fingerprint ff6dcb5f...e765), so update checks are on; anything not signed with it is refused.
- When an update is found: a PS4 pop-up, a NovaCore entry in Notifications and an update card in Settings.
- The update card: Download, then Install with one confirm press, or Later. GoldHEN, ini files and other apps are always refused.
- Off switch: /data/novacore-lab/ota.off. Two interrupted checks in a row turn checks off automatically.
- New: NovaLink Send PKG. Send a package from your phone (link, file or home Wi-Fi); Nova downloads and checks it, then asks "Install this package?" on the TV.
- Nothing installs without your X press. O keeps the file in /data/pkg. Never shown over a game or a video.
- Off until you turn on Settings > System & About > NovaLink: send packages. Off switch: /data/novacore-lab/pkg-send.off.
- Phone link (home Wi-Fi, port 8780): sent packages now wait for X on the TV instead of installing straight away.
- New boot animation (neon NC) while Nova loads your covers; boot now waits at most 12 s for covers before showing the dashboard. Off switch: /data/novacore-lab/bootanim.off.
- New Community page under Personalisation: Themes, Fonts and My uploads, matching the published preview. Off switch: /data/novacore-lab/community-gallery.off.
- Two unfinished starts of the new Community page fall back to the previous Community tab automatically (community-gallery.disabled).
- Theme Studio can use the 34 verified catalogue fonts. Fonts you add yourself stay on this console only. Off switch: /data/novacore-lab/user-fonts.off.
- Community likes and the public fonts route are prepared but remain off until the nova-themes sidecar is turned on. Demo themes are never uploaded.
- Smoother dashboard (Perf packs 1 and 2): animations no longer jump on a busy frame; logs, bridge files and Friends updates no longer hold up drawing; PS dash: Nova's work spread over frames. Same look, same speed.
- Covers coming into view load first while you scroll. Home, Quick Menu, Nova Play and the new Community page do much less work every frame (Community no longer writes files every frame).
- Perf off switches in /data/novacore-lab: perf-<name>.off (dt, uitrace, ttarm, bridgeio, upload, textfit, scrollwarm, lanmemo, friendspoll, rowcache, cgate, stallprobe) or perf.off. Frame times: perf.log.
- PS Store button: pressing X now opens just your chosen app. Sony's "update required" screen no longer pops up behind it.
- Fixed a false "could not be opened" message after the Store button opened your app.
- Carries everything from 1.1.0-rc.2: smoother 1080p film playback (video-smooth.off) and the Friends request, presence and picture fixes.

## [1.1.0-rc.2] — 2026-11-24 (DEV build, package 03.36, helper 94431)

- MediaSmooth: 1080p H.264 deblocks reference frames only, so films from the HDD keep sound and picture in step (video-smooth.off).
- Friends: requests no longer repeat, removed friends stay removed, request rows show pictures, online status uses the server clock, "Last online N days ago".

## [1.0.4-RC2.18] — 2026-11-24 (test pre-release, helper 94429)

Combines private RC2.15–17 with RC2.18. Console-unverified; Community host and revised server name allowance await deployment.

- Theme Store create tile and 59-row editor, visible palettes, Home/Library/QM samples, storage wallpaper picker and name/save/save-copy/upload choices.
- Expanded materials, borders, colours, fonts, moving overlays and sounds; per-theme card-size/depth settings. Bebas Neue font/licence bundled.
- Community catalogue/previews/separate-copy install and opt-in upload prepared; independent host tested but not deployed.
- Nova Play main tab restored; Social Lounge with in-page Friends/requests/messages/profile and existing room compatibility.
- Layout order: Nova Dashboard, Nova Lab, Nova Series, Nova Switch, then remaining layouts. Saved IDs retained.
- Shared request-alert deduplication, avatars/last-online fallback, activity queries and consistent Nova cosmetic labels. No real PSN/account changes; Sony native-picture writer stays disabled.
- QM CAPS/abc and L2 toggle. Two-name-changes/60-days client copy; matching server patch staged only.
- Current top-icon focus handling rejects stale game focus. Dedicated panels and existing QM/input safeguards retained.
- Playback crash/pixelation changes: software H264 routing, versioned crash guard, clearer resolver errors, same-packet retry and normal filtering.
- Manual internal FPKG recovery: read-only scan, verified backup, double confirmation, separate pinned DB Rebuilder v0.2, result check and Apollo restore guidance. External-only entries report-only; not run on console.
- Ordinary notices shortened to 2.5 seconds and deduplicated. Native content safe area; wallpaper full bleed.
- Native/SELF/PKG checks passed; all 437 extracted files verified. Helper reproducible with baseline imports. Hardware acceptance pending.

[Full notes and testing](RELEASE-v1.0.4-RC2.18.md)

## [1.0.4-RC2.14] — 2026-11-23 (QM hotfix 94424)

Sorry for the extra download, everyone. The last update reduced dashboard lag, but it also stopped the Quick Menu and top-bar panels from opening on the reported console. Thanks for sticking with the testing and letting me know ❤️

- 🔘 Corrected the compatibility check that blocked the menu on firmware without certain menu-focus features.
- 🧭 Kept the opening controls active while skipping unnecessary hidden-menu redraws.
- 🏎️ Kept the lag reductions. The owner reported less dashboard lag and working game-hover panels in the previous build.
- 📦 Only the bundled helper changed. The Nova app, settings and other RC2.14 additions stay in place.

**Install over RC2.14 → open Nova once → fully restart PS4 → enable GoldHEN normally.** Then hold touchpad and check the dashboard Profile/Friends/Messages panels.

Build and computer-side checks passed. **Hotfix console confirmation is pending**, including game-input isolation. Check the game underneath stays still while using QM; close it and report if it responds.

[Corrected PKG](https://github.com/WetOttersPocket/NovaCore/releases/download/v1.0.4-RC2.14/NovaCore-v1.0.4-RC2.14-QM-HOTFIX-94424.pkg) · SHA-256: `2880de4fec6dd5280608f98af7bb5ec4c408f87b3f09933c65c7fbedbbc159e2`.

## [1.0.4-RC2.14] — 2026-11-23 (refreshed)

- 🎞️ Experimental FFmpeg software HEVC up to 1080p SDR; H264 hardware/software decoders retained. HDR/DRM/4K rejected; console acceptance pending. HTTPS MP4 uses FFmpeg.
- 💬 Official orbisRPC 1.1 ELF/Setup PKG bundled with pinned GitHub digests; explicit prepare action updated. No auto-install/start/link or credential access.
- 🕹️ Removed overlapping L3/R3 + Triangle actions/hints; Library save-view moved to R3 menu and default tab remains in Settings.
- 🗂️ Added saved per-user Automatic/Games/Apps/Classics Library overrides, with validated atomic storage and no source metadata/database writes.
- ❓ Added in-app Help & FAQ, Phone Link/YouTube/Discord distinctions, original orbisRPC logo and credits. Shared RPC token-transfer wizard remains unimplemented.

- 🎮 Running-game detection independent of Nova's launch state, including Sony-launched games; catalogue names and existing running-app queries, without changing the launch/watchdog state.
- 🟢 Resident activity publishing/renewal to Friends, clear on game close and retry on failure. Existing offline/privacy controls retained.
- ⚡ Explicit QM Return clears a completed launch screen without waiting for the old 20-second heuristic. Actual console return speed unverified.
- 🌌 Boot minimum seven seconds plus stable visible-artwork readiness; existing loading ring and bounded fallback retained.
- 🔘 Existing RC2.14 focus/input fixes retained: background shortcuts suppressed, visible-menu input consumed and focus released on close/failure. Real game input isolation remains unverified.
- 🏎️ Hidden Quick Menu avoids repeated UI updates, profile-picture scans share a short per-user cache, and idle game discovery is rate-limited. Immediate opening and final close cleanup retained; console performance unverified.
- Helper **94422**, package **03.27**, same public RC2.14 release. Updated checksum supersedes the initial candidate. Two reproducible helper builds, unchanged imports/warnings, full package verification and host regression checks passed. **Historical helper 94422: superseded by hotfix 94424 above.**

## [1.0.4-RC2.13] — 2026-11-23

The owner has attached the RC2.13 PKG and matching checksum. Latest console acceptance pending. Changes below collect the private stages since public RC2.1.

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
