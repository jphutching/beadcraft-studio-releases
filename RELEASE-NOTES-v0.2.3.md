BeadCraft Studio 0.2.3 — a backup is checked before any of it is used, three rooms over one
chart, and the install page now says what the app actually asks for.

**What changed**

- **A backup or a project file is refused as a whole, with a reason, or it is used.** One reader now
  serves every door that takes a file: restoring a `.beadbackup`, opening a `.beadproj`, and the
  copy that travels inside the page. It refuses, before a single byte reaches the device: a manifest
  that leaves a listed file out, one that declares the wrong size, one written by a reader newer
  than this build, a path that climbs out of the archive, an entry listed twice, a checksum that no
  longer matches, and a file that is not an archive at all. A refusal leaves the design, the stash
  and the history exactly as they were. In 0.2.2 a backup whose manifest simply did not list
  `backup.json` was accepted; that is the defect this closes.
- **Edit, work and supplies — three rooms over the same saved chart.**
  *edit* paints the chart; *work* reads it (the pick-up list in reading order, the counts, and the
  way back to the chart without losing the undo history); *supplies* is the shelf (the counts you
  have taken, what an open chart still needs, and the buy list). The room you are in is kept on the
  device, not just for the session, and a fresh start opens the design you were last in.
- **Your designs as a library.** Rename a design from its row: the name travels with the design and
  the revision it replaces keeps its own name in the history. Copy one: the copy is a new design and
  the original is untouched. The design you were last in is offered at the top of the list with a
  single button.
- **Reading a chart by touch.** A tap paints one bead; a drag paints the line it crosses. A second
  finger pans and pinches, as before. The room tabs, the text switch and the design rows say what
  they are to a screen reader, a sheet takes the focus when it opens and gives it back when it
  closes, and **aA** on the home screen switches the whole app to bigger text.
- **The install page is true again.** The published page said the app asks for no permission at all
  and never touches the network. It asks for two: `INTERNET` (a version check against this
  repository's own release page, and the download if you say yes) and `REQUEST_INSTALL_PACKAGES`
  (handing a downloaded build to Android's own installer). The chart editor itself never uses the
  network and works offline.

**Permissions** (unchanged, and still only these two)

    INTERNET                      to check for and download an update you ask for
    REQUEST_INSTALL_PACKAGES      so Android will let the app hand a verified update to its installer

Nothing else: no storage, no camera, no location, no contacts, no analytics.

**Install**

If you are on 0.2.2, the app updates itself: **menu → about → look for a newer build**, then confirm
Android's install prompt. Your designs and your stash are kept.

Every earlier version installs over the top the same way:

1. Download `BeadCraftStudio-v0.2.3.apk` below, or scan the QR code (`BeadCraftStudio-v0.2.3-qr.png`,
   which carries exactly that file's address).
2. Open the downloaded file and allow installs from that app if Android asks, then tap **Install**.
3. Open **BeadCraft Studio**.

Over adb, as a separate route:

    adb install -r BeadCraftStudio-v0.2.3.apk

Every release is signed with the same key, certificate SHA-256
5295f944fd1a09061e3acd34acd5c408be89437f5b11ec897031d41690caede7, and the app refuses a build signed
with any other, so an update installs over any version you already have without uninstalling.

**File**

    BeadCraftStudio-v0.2.3.apk   172,904 bytes
    sha-256 7b97db9b2720290d25d4d704fd2bf0e4fdf55b1bc08054b00a41a6e6885713e0

Minimum Android 7.0 (API 24). versionCode 8, versionName 0.2.3.

**Proved before release**

Off-device, every suite passes with none failing: the page (75), the regression set (46), the store
(53), U01 (49), the collision pair (2), the reviewer fixtures (6), the backup and refusal set (37),
the artist set (34), the update precheck (13), the print and zip proofs, the offline and file
refusals, the storage screens (39), the layout set, the compatibility check with a v0.1.0 project,
the Java updater and policy tests (150), and the APK identity checks (assets, versionCode, and a
v1/v2/v3 signature that verifies against the key above).

The artist features are also driven on the glass-off-device, in a real browser engine: 29 checks
over the three rooms, opening the chart from work, the sheet's focus, a tap painting exactly one
bead, a drag painting a line, and the big-text switch — all passing on this build.

**Scope**

Chart-only, loom / square-stitch and peyote, as before. It does not draw a thread path or guide
construction, and the sizes it reports are nominal, from each bead line's own published footprint.
Nothing in the app has been validated against a piece worked by hand. Fuse beads are in the
catalogue and can be counted, but the layouts this build draws are not fuse-bead layouts.
