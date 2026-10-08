# NovaCore

A free, early-access dashboard for jailbroken PS4 consoles. Games, homebrew,
media, themes and tools in one controller-friendly interface.

## Downloads

Download PKGs from this repository's **Releases** tab. Discord membership,
donations and completed reports are not required for public TESTER downloads.
Discord is optional: https://discord.gg/cjgA8T94E

This repository contains public release information and issue forms. The full
development source is not published here; dependency and asset provenance review
is still open. Do not mistake public binary downloads for an open-source licence.

## Two distinct builds

| | TESTER | DEV |
|---|---|---|
| Purpose | Public baseline testing | Explicit experimental testing |
| File | `NovaCore-preview.115-TESTER.pkg` | `NovaCore-preview.115-DEV.pkg` |
| GoldHEN config switches | Confirmation, backups; next HEN load | Same plus plugin/patch editing |
| PS-return experiment | Excluded | Experimental; not guaranteed |
| HEN auto-start | Not established as working | Not established as working |
| LAN | Controlled rooms/text tests | Experimental features available |
| Package identity | NOVA00001 | NOVA00001 |

These are different feature builds, but they use the **same title ID** and
replace one another. They do not install side by side. Start with TESTER.
DEV is a prerelease, not an upgrade promised to be more reliable.

## Install and report

1. Read the release notes and known issues. Keep your previous package and Nova
   settings. Confirm HEN is enabled and use its normal Package Installer.
2. Compare your downloaded file's SHA-256 with `SHA256SUMS.txt`.
3. Install the chosen channel. Record any installer error; do not delete settings
   or uninstall blindly to solve a failed update.
4. Test the build. Report problems using **Issues → Bug report**.
5. Alternatively attach the matching `.txt` tester form to a GitHub issue.
   Nova also creates its form under `/data/novacore/reports/` on first launch;
   retrieve it through FTP. Existing answers are not overwritten.

Public reports must not contain passwords, account tokens, PSN identity,
console IPs or unredacted logs. Honest failures are useful. A validator can check
format and consistency; it cannot prove a person actually tested.

## Store attribution

**Homebrew Store:** Nova provides an integrated front end for catalogue metadata
from the existing [PS4 Homebrew Store](https://github.com/LightningMods/PS4-Store)
and its local cache, alongside curated official-release entries. The Store and
the homebrew apps belong to their respective developers. Reference catalogue
entries are discovery-only; they are not automatically verified installers.

**Otters PKG Store:** Nova provides a front end for **FPKGi-compatible JSON
catalogues**. See [FPKGi](https://github.com/ItsJokerZz/FPKGi). Publicly available
third-party JSON feeds and user-supplied catalogues remain third-party data;
NovaCore does not claim ownership of their contents. It is not a new proprietary
game database, nor is every Nova action delegated to the FPKGi app. TESTER does
not expose DEV catalogue/download capabilities. Public availability of a JSON
file does not establish redistribution rights for packages it references.

## Status

Preview 115: build-specific reports; GoldHEN configuration switches; LAN cover
fallback; Big Lez Rainbow theme; report identity validation. Compile/link,
package integrity and format tests passed. Runtime behavior needs console tests.

Still open: permanent PS-return reliability, HEN auto-start, launch/performance
regressions, complete metadata coverage, Linux installation, cloud gaming,
party voice chat, NEXT companion integration and local PKG installation.
No universal firmware support is claimed.

For DEV PS-button activation and testing, read [PS-BUTTON-TEST.md](PS-BUTTON-TEST.md).
Nova displays an activation confirmation/result. Check five short presses,
game transitions and deliberate exit; never treat an enable request as proof
that focus interception is working.

The report tool collects structured feedback and diagnostics for debugging.
It does not automatically repair firmware or prove test results. NEXT is a
planned companion integration; it is not currently the report validator.

## Credits and donations

Credits: WetOttersPocket and LethalLadyT, plus the upstream homebrew community.
NovaCore remains free. Optional PayPal: **NovaCore1337@yahoo.com**.
Donations do not affect downloads, reports or tester access.

See [KNOWN-ISSUES.md](KNOWN-ISSUES.md) and [CONTRIBUTING.md](CONTRIBUTING.md).
