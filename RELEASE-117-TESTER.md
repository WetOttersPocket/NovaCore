# Preview 117 TESTER / 5.124

Preview 117 is the next public test candidate. DEV and TESTER use the same
`NOVA00001` title ID and replace one another; do not try to keep both installed.

Changes:
- Adds a safe Game Toolbox for rebuilding Nova's own library index, renaming a
  title inside Nova, hiding/restoring it inside Nova, and launching installed
  Apollo Save Tool or Itemzflow Game Manager.
- Keeps PS4 system-database rebuilding in Sony Safe Mode. Nova does not rewrite
  the system database or package metadata.
- Fixes System Link room creation for game names longer than 32 bytes or names
  containing symbols such as the trademark character.
- Adds time-of-day profile greetings and the `What are we playing today?` home
  subtitle.
- Adds the Library Downloading view for Nova-owned transfer jobs.
- Detects and launches an installed NEXT System Control app from its Nova tile.
- Updates credits to WetOttersPocket, LethalLadyT and KillerNoS / NEXT System
  Control, with larger readable text.
- Uses distinct TESTER and DEV report IDs so the same Discord bot can validate
  both channels without confusing their forms.

TESTER keeps risky developer-only controls locked. System Link rooms and group
messages are included for the requested closed multi-console test. Package
downloads remain disabled in TESTER.

Console verification is still required for game launching, room creation on two
consoles, trophies, cover-loading latency, theme persistence and PS-button return.

