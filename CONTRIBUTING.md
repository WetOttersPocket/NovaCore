# Help test NovaCore

Download the current release candidate from [Releases](https://github.com/WetOttersPocket/NovaCore/releases). No Discord account, payment or application is required.

## Report a bug

Use **Issues → Bug report** and include:

1. Exact Nova version and package revision (current: v1.0.2-RC1 / 03.02).
2. Console model, firmware and exact GoldHEN/HEN version.
3. Steps, expected result, actual result and any error code.
4. Whether you fully restarted and enabled HEN after updating.
5. Relevant screenshots or redacted log extracts, if available.

For playback, include the source type and format, whether picture/sound worked and whether the issue occurs in Nova or Quick Menu. Never include a stream URL containing a password or account key.

For Quick Menu/return, say where you were (Nova, Sony dashboard or game) and which controls you used. The expected quick return is **hold touchpad → Return to Nova → Cross**; a normal PS tap still opens Sony's dashboard.

Logs are under `/data/novacore-lab/`: playback uses `video.log`, YouTube uses `yt/console.log`. Do not reproduce a console freeze repeatedly just to obtain logs. Remove credentials, tokens, pairing PINs, console IPs and private account details before posting.

## Suggestions

Search existing issues, then use **Feature request**. Explain what you want to do and how the change would help. Failures are useful feedback; please distinguish observations from guesses.

This repository is for public distribution, documentation and reporting. NovaCore's app source is not published here. See [known issues](KNOWN-ISSUES.md) and [third-party notices](THIRD-PARTY-NOTICES.md).
