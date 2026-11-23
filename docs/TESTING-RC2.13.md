# RC2.13 test checklist

The latest candidate is not confirmed on hardware. Check each result as Pass / Fail / Not tested. Stop after a freeze; never repeat one just for logs.

1. **Setup:** model, firmware, exact GoldHEN version; manual Nova launch; restart/HEN; auto-start outcome.
2. **Games:** internal and external-drive launch; exact title/error; whether Nova, the game or the console failed; Quick Menu and return to Nova.
3. **Social:** gamercard visible immediately; Up focus/Cross Profile/Down back; online light; current-game pink line; Appear offline and sharing-off hide activity; trophy icons/counts after Refresh.
4. **Friends:** existing identity preserved; new setup; add/accept/decline/block/remove; pictures/names; activity/privacy; request badge clears after sync.
5. **Messages:** send/reply/history; unread marker clears on reading; one notification per new event; Circle/hold-touchpad do not freeze the menu.
6. **Dashboard:** Profile/Friends/Messages open their own panels; main tiles do not reopen them; Store launches the selected installed app, including external-drive targets.
7. **Music:** Radio/Favourites/Local files/My stations/Queue; HDD and USB MP3s; artwork; pause/resume/stop/volume in Nova, dashboard and games.
8. **Video:** local H.264/AAC MP4; USB video; supplied channel; custom/Jellyfin source if used; picture AND sound; pause/resume/seek (non-live); close safely; failed source ends with a clear error.
9. **Phone:** YouTube without Friends setup; QR pairing; notifications enabled; Test; closed-page approval prompt; Off retains pairing; Unpair revokes it; server restart retains pairing.
10. **Regression:** Library layouts/themes, game actions, captures gallery, trophies, tools, news and settings still behave as before.

Report build/model/firmware/HEN, steps and exact error. Attach relevant exported logs after redacting secrets, friend codes, messages and personal data. Do not upload raw configuration, tokens or pairing state. Older screenshots/mock-ups are not console-test evidence.
