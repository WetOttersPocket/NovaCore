# Known issues — v1.0.4-RC2.1

- **Unresolved startup issue:** the preceding 03.07 test build froze/crashed during HEN startup. Troubleshooting did not identify the cause. RC2.1 is reported running by the owner; automatic HEN startup remains unverified. Stop testing if a crash occurs.
- Verified package identity: **03.08**, bundled dashboard plugin **d59 / 94409**. These package checks do not establish that all runtime features work.
- Store shortcut selection, trophy artwork, bottom-bar hiding, theme refresh, media volume and YouTube sync need testing in the final package.
- A Store press immediately after landing on its tile may still reach Sony’s screen.
- Firmware 13.52 is not confirmed. The owner’s established test setup is PS4 Slim / 13.02 / GoldHEN. Do not update firmware for Nova.
- YouTube defaults to 480p. Hardware video decoding is not active. Watch Together is not included.
- Nova’s dashboard notification panel remains off; the bell uses Sony’s normal list.
- Nova Theme 2 may need selecting again after reboot.

## Reporting and controls

Hold touchpad → Return to Nova → Cross for Quick Return. A normal PS tap still opens Sony's dashboard.

Keep your previous working package. Do not repeatedly reproduce a freeze or restart the console just to get logs. Report the exact build, console model, firmware, HEN version, steps and outcome. Redact credentials, account details and pairing codes. See [reporting guide](CONTRIBUTING.md).
