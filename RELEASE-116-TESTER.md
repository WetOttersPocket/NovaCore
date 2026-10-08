# Preview 116 TESTER / 5.121

Public maintenance candidate; previous 115 remains available. Dashboard styling
is unchanged. DEV and TESTER still share NOVA00001 and replace one another.

Changes:
- Circle cancels a pending soundtrack-fade launch and restores ambient audio.
- The pending title is tracked by ID, not list index. If it disappears after a
  rescan, the launch is cancelled instead of launching a different selection.
- Empty selections and Nova itself are rejected before entering the launch fade.
- LAN cached-art fallback is independent of the installed icon, so a failed icon
  no longer selects itself again as its own fallback.
- New Store cover requests wait until controller navigation has been idle for
  500 ms. Existing work is not claimed to stop instantly.
- Creates the 116 report under /data/novacore/reports without overwriting answers.

Companion report/bot updates: accept case/spaces in known answer choices, reject
duplicate fields, give allowed-answer hints, reconnect after disconnects and
check recent missed submissions. These run on the PC/server, not inside the PKG.

TESTER excludes PS-return injection and plugin/patch writes. No HEN auto-start
or permanent PS-return fix is claimed. GoldHEN config changes apply on next load.

Verification: both PS4 targets compiled/linked; package checks and report tests.
Real-console checks needed: cancel fade, launch selected title after refresh,
audio recovery, LAN artwork, and navigation latency. No zero-lag claim.
