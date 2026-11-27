# BeadCraft Studio

> **This release is on hold. Please do not install it yet.**
>
> Two things are open against the build this page is about (v0.2.4): a **Play Protect
> warning** that has not been explained yet, and **catalogue rights** for the bead colour
> data it ships. A newer build, 0.2.5, is signed and has now been installed on a phone: the
> install went through Android's own installer and Play Protect raised no panel for it. That
> says nothing about the v0.2.4 warning and does not settle it. Nothing from 0.2.5 or later
> is published; whether one is published, and when, is undecided. This page will say when a
> build is one we recommend, and that is the only build this page will point at.

BeadCraft Studio is an Android app for beadwork charts. Paint a loom / square-stitch chart
with real bead codes, count it, work out what to buy from what you already have, save the
design as a `.beadproj`, and print it as a PDF with rulers, a colour key and a row-by-row
pick-up list. It works with the phone offline: nothing is uploaded, and there is no
account, no ads and no analytics.

## Status of what is on this page

| | |
|---|---|
| newest release here | v0.2.4 (versionCode 9), published 2026-11-26 |
| recommended for artists | **nothing, yet** — see the box above |
| next build | 0.2.6 (versionCode 14), signed, not published; 0.2.5 (code 10) is superseded |

The v0.2.4 files stay where they are. Earlier builds are not withdrawn and no asset has
been removed; the box at the top is the recommendation.

## What you need

* Android 7.0 (API 24) or newer.
* About 1 MB of free space. v0.2.4 is 173 KB.

## What it asks for

Two permissions, and no others:

* **Internet** — used for one thing: checking GitHub for a newer build of this app, when you
  ask it to, or once a day if you turn the daily check on, and downloading a build if you say
  yes. It does not send anything about you or your designs.
* **Install unknown apps** — the permission Android calls `REQUEST_INSTALL_PACKAGES` — used
  for one thing: handing a downloaded build to Android's own installer, which asks you
  whether to install it.

It does not ask for storage, camera, location, contacts or phone access.

## Installing, when a build is recommended

There is nothing to install from this page today: no build is recommended, and this page
carries no download link while that is true.

When a recommended build exists, installing it is:

1. Download the `.apk` from that release.
2. Open the downloaded file. Android will ask whether to allow installs from that app
   (usually your browser or Files) — allow it, then tap **Install**.
3. Open **BeadCraft Studio** from your app list.

Or over adb, from a file you already have:

    adb install -r BeadCraftStudio-<version>.apk

## The two installation codes

Both are QR codes that carry an address for the app, and they are not the same thing.

* **The permanent code** opens this repository's `/releases/latest` — whatever release
  GitHub marks as latest. It never changes. Right now it resolves to **v0.2.4**, the release
  this hold is about, so the code is correct and still not one to scan or print until
  `latest` serves an approved build.
* **A pinned code** carries the address of one exact file. The only pinned code made so far
  is for the 0.2.5 build, and that address does not resolve, because 0.2.5 has no tag and no
  release. It is a draft, and it is not to be shown to anyone until that release exists.

There is no QR on this page. Neither code should be in circulation while the hold is up, and
a code that opens an older, unapproved build is worse than no code.

## Play Protect, plainly

This app does not come from Google Play, so Play Protect looks at it when it is installed.
On a real phone, installing the build this page is about brought up Android's **"Harmful app
blocked"** panel. That is a warning, not a routine scan: the phone told the person installing
that Android had classified the app as harmful. An earlier version of this page described the
same panel as something that "may offer to scan the file" and "can delay the install". That
was wrong, and it is why this page now says what the phone showed.

The classification behind that panel is not resolved. No account of what was classified, or
why, has been obtained, so this page does not call the warning a mistake, does not call the
app safe, and does not explain it away. The hold stays until the classification is answered
and anything real behind it is fixed.

**Do not turn Play Protect off to install this app**, and do not ignore a harmful-app
warning: if Play Protect says a file is unsafe, stop and don't install it. Nothing on this
page asks you to weaken a protection.

## Updates

From 0.2.3 the app has a way to update itself, inside the app: **menu → about this build →
check for an update**. It reads the release page for this repository, shows you the version,
size and published date, downloads the file only if you say **install it**, and then hands it
to Android's installer, which asks you to confirm. Your designs are kept — an update installs
over the old build and replaces the app, not its data.

That path has been walked once on a real phone, between 0.2.3 and 0.2.4: the phone found the
0.2.4 build, downloaded it, and handed it to Android's installer. What happened at the
installer is not established. The record of that walk includes a Play Protect "Harmful app
blocked" panel, and the review of it found that later screenshots show 0.2.4 running, with the
same first-install date and the same design still open, but do not show how that panel was got
past. So this page does not claim the update path is proved end to end. It stays unproven
until the Play Protect finding is closed and the walk is repeated on a clean phone with the
whole sequence recorded.

Android adds two screens to that flow, which the app does not control:

* **"Update this app?"** — Android's installer asks before replacing the app. Nothing is
  replaced until you tap it.
* **Play Protect** — the warning described above, shown against the downloaded file. On this
  build it can block the install, not only hold it up.

The **look for a newer build once a day** switch (off by default) reads one published release
note at most once a day, when no other sheet is open in front of you. It never installs
anything by itself.

If you are on 0.2.2 or earlier, the check finds a newer version but the download is refused:
those builds only know the old address GitHub used to serve release files from. That is fixed
by installing a recommended build directly, once there is one; it cannot be fixed from inside
0.2.2.

Every version has been signed with one key (certificate SHA-256
`5295f944fd1a09061e3acd34acd5c408be89437f5b11ec897031d41690caede7`), and the app refuses a
build that is not signed with it. That is what makes a build from here an upgrade of the last
one rather than a second app.

## What version 0.2.4 is

0.2.4 changes one thing: the version number. It is 0.2.3, raised, so that the repaired update
path could be tried on a phone from a build already in the field. Everything below arrived in
0.2.3 and is what 0.2.4 contains.

* **A backup is checked before any of it is used.** A backup or project file is refused as a
  whole — with a sentence saying what is wrong — if its manifest leaves a file out, declares
  the wrong size, needs a newer reader than this build, names a path outside the file, lists
  a file twice, or carries a checksum that no longer matches. A refused file leaves the
  device exactly as it was.
* **Downloading an update works.** 0.2.2 and earlier refused GitHub's current release-file
  address as a lookalike; 0.2.3 and later accept both the old and the current address from
  GitHub's own release host, and still refuse anything else.
* **Three rooms over the same saved chart:** *edit* (paint), *work* (the chart big, for
  following it bead by bead) and *supplies* (what you have and what to buy).
* **Your designs, as a library:** rename or copy a design from its row.
* **Reading a chart by touch:** a tap paints one bead; a drag paints a line of beads. The
  buttons, the room tabs and the text-size switch say what they are to a screen reader, and
  **bigger text** is a switch on the home screen.
* A design made in 0.1.0 still opens, with the same revision, beads and colours.

## Limits worth knowing

* It is a **chart** app. It does not draw a thread path or a stitch sequence and does not
  guide construction. A flat peyote chart is printed half a bead a row, the way the beads
  sit, and says so on the page.
* There is **no pattern-image (PNG) export and no supplies-only PDF** in the published
  builds; the chart PDF, the `.beadproj` and the `.beadbackup` are what you can take away.
* Colour codes and swatch colours come from each maker's catalogue. A swatch on the screen
  is a reference, not a measured colour: your beads and your screen will differ. The terms
  each catalogue is used under are printed on the key page of every PDF, and the rights for
  the colour data in 0.2.4 are one of the open items above.
* Nothing in the app has been checked against a physically stitched piece. Counts, sizes and
  the buy list are arithmetic on the chart.
* Fuse beads (Perler and similar) are in the catalogue and can be counted, but the layouts
  this build draws are loom / square stitch and flat peyote.

## Earlier versions

v0.2.3 · v0.2.2 · v0.2.1 · v0.1.0 — still in this repository for the record, on the same hold
as v0.2.4, and not offered here as installs.

Source is private; this repository holds install files only.
