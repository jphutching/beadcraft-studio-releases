# BeadCraft Studio — install

BeadCraft Studio is an Android app for beadwork charts. Paint a loom / square-stitch chart
with real bead codes, count it, work out what to buy from what you already have, save the
design as a `.beadproj`, and print it as a PDF with rulers, a colour key and a row-by-row
pick-up list. It works with the phone offline: nothing is uploaded, and there is no
account, no ads and no analytics.

## What you need

* Android 7.0 (API 24) or newer.
* About 1 MB of free space. The current build is 173 KB.

## What it asks for

Two permissions, and no others:

* **Internet** — used for one thing: checking GitHub for a newer build of this app when you
  ask it to, and downloading that build if you say yes. It does not send anything about you
  or your designs.
* **Install unknown apps** — used for one thing: handing a downloaded build to Android's own
  installer, which asks you whether to install it.

It does not ask for storage, camera, location, contacts or phone access.

## Install

1. Open the [latest release](../../releases/latest) and download
   `BeadCraftStudio-v0.2.4.apk`.
2. Open the downloaded file. Android will ask whether to allow installs from that app
   (usually your browser or Files) — allow it, then tap **Install**.
3. Open **BeadCraft Studio** from your app list.

Or over adb:

    adb install -r BeadCraftStudio-v0.2.4.apk

The QR code in the latest release opens the same download.

## Updates

From 0.2.3 the app updates itself, inside the app: **menu → about this build → check for an
update**. It reads the release page for this repository, shows you the version, size and
published date, downloads the file only if you say **install it**, and then hands it to
Android's installer, which asks you to confirm. Your designs are kept — an update installs
over the old build and replaces the app, not its data.

That path has been walked on a real phone, not only in a test: 0.2.3 (versionCode 8) found
this 0.2.4 build, downloaded it, installed it over itself, and came back up as 0.2.4
(versionCode 9) with the same first-install date and the same design still open. The
screenshots are in the version 0.2.4 notes.

Two things Android itself adds to that flow, which the app does not control:

* **"Update this app?"** — Android's installer asks before replacing the app. Nothing is
  replaced until you tap it.
* **Play Protect** — on a build that did not come from Play, Play Protect may offer to scan
  the file before installing it. That is the phone's own check, it is offered once per new
  build, and it can delay the install while it runs.

The **look for a newer build once a day** switch (off by default) does exactly that: it reads
one published release note at most once a day, when no other sheet is open in front of you.
It never installs anything by itself.

If you are on 0.2.2 or earlier, the check finds a newer version but the download is refused —
those builds only know the old address GitHub used to serve release files from. Install
0.2.4 from this page once and the in-app update works from then on.

Every version has been signed with one key (certificate SHA-256
`5295f944fd1a09061e3acd34acd5c408be89437f5b11ec897031d41690caede7`), and the app refuses a
build that is not signed with it. So an update from this page always installs over the
version you already have.

## What version 0.2.4 is

0.2.4 changes one thing: the version number. It is 0.2.3, raised, so that the repaired update
path could be walked end to end on a phone from a build already in the field. Everything
below arrived in 0.2.3 and is what 0.2.4 contains.

* **A backup is checked before any of it is used.** A backup or project file is refused as a
  whole — with a sentence saying what is wrong — if its manifest leaves a file out, declares
  the wrong size, needs a newer reader than this build, names a path outside the file, lists
  a file twice, or carries a checksum that no longer matches. A refused file leaves the
  device exactly as it was. Before this version, a backup whose manifest simply left
  `backup.json` out of its list was accepted.
* **Downloading an update works.** 0.2.2 and earlier refused GitHub's current release-file
  address as a lookalike and never started the download; 0.2.3 and later accept both the old
  and the current address from GitHub's own release host, and still refuse anything else.
* **Three rooms over the same saved chart:** *edit* (paint), *work* (the chart big, for
  following it bead by bead) and *supplies* (what you have and what to buy). The app
  remembers which room you were in.
* **Your designs, as a library:** rename or copy a design from its row. A rename changes the
  name and nothing else; a copy is a new design that leaves the original alone. The design
  you were last in is offered back at the top of the list.
* **Reading a chart by touch:** a tap paints one bead; a drag paints a line of beads. The
  buttons, the room tabs and the text-size switch say what they are to a screen reader, and
  **bigger text** is a switch on the home screen.
* A design made in 0.1.0 still opens, with the same revision, beads and colours.

## Limits worth knowing

* It is a **chart** app. It does not draw a thread path or a stitch sequence and does not
  guide construction. A flat peyote chart is printed half a bead a row, the way the beads
  sit, and says so on the page.
* Colour codes and swatch colours come from each maker's catalogue. A swatch on the screen
  is a reference, not a measured colour: your beads and your screen will differ. The terms
  each catalogue is used under are printed on the key page of every PDF.
* Nothing in the app has been checked against a physically stitched piece. Counts, sizes and
  the buy list are arithmetic on the chart.
* Fuse beads (Perler and similar) are in the catalogue and can be counted, but the layouts
  this build draws are loom / square stitch and flat peyote.

## Earlier versions

[v0.2.3](../../releases/tag/v0.2.3) · [v0.2.2](../../releases/tag/v0.2.2) ·
[v0.2.1](../../releases/tag/v0.2.1) · [v0.2.0](../../releases/tag/v0.2.0) ·
[v0.1.0](../../releases/tag/v0.1.0)

Source is private; this repository holds install files only.
