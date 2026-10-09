# Preview 121 TESTER / 5.131

Preview 121 is the next public TESTER candidate. It keeps experimental
developer-only PS-button and HEN-start probes out of the public package while
retaining the Store download and closed System Link test paths.

Changes:
- Adds `Transfers > R3 Direct Package` for an authorised final HTTP/HTTPS PKG
  URL, a display name and its exact byte size. Nova validates the fields and
  requires a second confirmation before handing the job to PS4 Downloads.
- Supports private FPKGi-format Games and DLC catalogue URLs through Nova's
  Store front end. The URL used as each `DATA` key is preserved as its package
  source, so catalogue owners can switch an entry to a faster authorised direct
  provider without changing Nova.
- Adds safe deletion of one explicitly selected downloaded `.pkg` file after a
  two-press confirmation. Installed games, saves and Library collections are
  outside this action.
- Mirrors existing PS dashboard folders at the start of the Library filters,
  using their names and dashboard order. Last Played remains the fallback when
  no folders are available.
- Keeps Store downloads and System Link enabled for this focused TESTER pass.

Provider speed is not generated or proxied by Nova. A source must be a real
direct file URL: opening it in a browser should immediately start the file.
Landing pages, login bypasses and host scraping are not supported. Test only
content you are authorised to access and begin with a small disposable package.

Console verification is required for BGFT registration, provider/TLS
compatibility, exact-size handling, suspend/resume, selected-file deletion,
dashboard-folder parity, game launching and two-console System Link messaging.

