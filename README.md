# BeadCraft Studio

> **0.2.6 is published, and it is the build this page points at.**
>
> 0.2.6 opens a project that names a bead maker this build does not carry, stops renaming a
> design behind your back, finds stock you counted under an older spelling, makes colour part
> of a design's identity, lets you set the colour of a code the maker leaves open, and follows
> the phone's own text size.
>
> Three things are open, and they are written here rather than smoothed over: the **Play
> Protect classification** of the earlier v0.2.4 build is still unexplained; **permission to
> redistribute the bead catalogue** has been drafted as a letter and has not been sent, so
> none is granted (the build ships the maker's codes and names only, never an image or a
> colour value); and **TalkBack has not been tested** against this build's chart. The Play
> Protect history below is about v0.2.4; what is known about 0.2.6 is said in its own section.

BeadCraft Studio is an Android app for beadwork charts. Paint a loom / square-stitch chart
with real bead codes, count it, work out what to buy from what you already have, save the
design as a `.beadproj`, and print it as a PDF with rulers, a colour key and a row-by-row
pick-up list. It works with the phone offline: nothing is uploaded, and there is no
account, no ads and no analytics.

## Status of what is on this page

| | |
|---|---|
| newest release here | v0.2.6 (versionCode 14), published 2026-11-27 |
| recommended for artists | **v0.2.6**, with the three opens named at the top of this page |
| earlier builds | 0.2.5 (code 10) was never released; 0.2.4 (code 9) and older are superseded by 0.2.6 |

The v0.2.4 files stay where they are. Earlier builds are not withdrawn and no asset has
been removed; the box at the top is the recommendation.

## What you need

* Android 7.0 (API 24) or newer.
* About 1 MB of free space. 0.2.6 is 173 KB.

## What it asks for

Two permissions, and no others:

* **Internet** — used for one thing: checking GitHub for a newer build of this app, when you
  ask it to, or once a day if you turn the daily check on, and downloading a build if you say
  yes. It does not send anything about you or your designs.
* **Install unknown apps** — the permission Android calls `REQUEST_INSTALL_PACKAGES` — used
  for one thing: handing a downloaded build to Android's own installer, which asks you
  whether to install it.

It does not ask for storage, camera, location, contacts or phone access.

## Installing 0.2.6

* The app itself: [BeadCraftStudio-v0.2.6.apk](https://github.com/jphutching/beadcraft-studio-releases/releases/download/v0.2.6/BeadCraftStudio-v0.2.6.apk) — 172,904 bytes, SHA-256
  `8ce0e72a5e553bc2268456109498f1e592672d027eb53cc36fbf7a5997dda759`.
* The same app as one page you can open in any browser, to look without installing:
  [BeadCraftStudio-v0.2.6.html](https://github.com/jphutching/beadcraft-studio-releases/releases/download/v0.2.6/BeadCraftStudio-v0.2.6.html).
* That release also carries `SHA256SUMS.txt`, so you can check both files yourself.

Installing from the download:

1. Tap the `.apk` link and let it download.
2. Open the downloaded file. Android will ask whether to allow installs from that app
   (usually your browser or Files) — allow it, then tap **Install**.
3. Open **BeadCraft Studio** from your app list. On a build that is new to your phone, Play
   Protect may show the warning described below; read that section before you decide.

Or over adb, from a file you already have:

    adb install -r BeadCraftStudio-v0.2.6.apk

Your designs are kept. 0.2.6 installs over an earlier build as an upgrade of the same app, not
as a second app, because every build from 0.1.0 onwards is signed with the same key.

## The two installation codes

Both are QR codes that carry an address for the app, and they are not the same thing.

* **The permanent code** opens this repository's `/releases/latest` — whatever release GitHub
  marks as latest. It never changes, and today it resolves to **v0.2.6**:
  ![permanent code](https://github.com/jphutching/beadcraft-studio-releases/releases/download/v0.2.6/BeadCraftStudio-latest-qr.png)
* **The pinned code** carries the address of one exact file — the 0.2.6 APK — so it keeps
  working whatever `latest` later points at:
  ![0.2.6 code](https://github.com/jphutching/beadcraft-studio-releases/releases/download/v0.2.6/BeadCraftStudio-v0.2.6-qr.png)

The pinned code above was drawn from the download address GitHub published for that file once
the release existed, so it resolves. A pinned code is the one to print or hand to someone; the
permanent code follows whatever this page recommends.

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

What is known about 0.2.6: it was installed on a phone over adb, and Play Protect raised no
panel. That is worth less than it sounds — an `adb install` does not take the same path as
opening a downloaded file — so it does not settle the v0.2.4 warning, and this page does not
treat it as if it did. Nobody has yet walked the download-and-tap path on 0.2.6 and recorded
what the phone showed.

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

## What version 0.2.6 is

0.2.6 is about files and colours that already exist.

* **A project made for a bead maker this build does not carry opens, and can be exported as it
  is.** Its codes, names and bead sizes are read from the maker row and bead rows written
  inside the file, instead of being refused because this build's catalogue lacks them.
* **A design is never renamed behind your back.** If a file spells a code an older way, the app
  shows you what the catalogue answers and leaves your design alone; moving it to the
  catalogue's spelling is something you ask for, it is written down, and one tap undoes it.
* **Stock counted under an older spelling is found, and settled once.** Two spellings of one
  bead are never added together silently: they read as unsettled, you choose, and the choice is
  recorded. A bead the catalogue does not carry keeps its count where it was.
* **Colour is part of a design's identity.** Two charts of the same beads in different colours
  are two designs, and a project written by an older build still opens and still verifies.
* **You set the colour.** This catalogue publishes no colour value, so a code is drawn in a
  colour you pick, one entry at a time, undoable in a step, printed in the PDF key, and marked
  as yours rather than as the maker's. A code whose maker does publish a colour keeps it.
* **The phone's text size works.** At Android's larger-text setting the app now draws larger
  text; earlier builds ignored it.
* **The catalogue is guarded.** A build refuses to ship a row with no source, a colour the
  maker did not publish, or a row credited to the wrong maker.

The catalogue is MIYUKI Delica 11/0, 1,288 codes, read from the manufacturer's own pages. TOHO
and PRECIOSA are not in this build.

## What version 0.2.4 was

0.2.4 changes one thing:0.2.4 changes one thing: the version number. It is 0.2.3, raised, so that the repaired update
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
* Bead codes and names come from the maker's catalogue. The colour a code is drawn in is the
  one **you** set, not one the maker published: it is a reference, and your beads and your
  screen will differ. Anything shipped from a catalogue has its terms printed on the key page
  of every PDF. Permission to redistribute the MIYUKI code list is not granted; the letter
  asking for it is drafted and has not been sent.
* Nothing in the app has been checked against a physically stitched piece. Counts, sizes and
  the buy list are arithmetic on the chart.
* Fuse beads (Perler and similar) are in the catalogue and can be counted, but the layouts
  this build draws are loom / square stitch and flat peyote.

## Earlier versions

v0.2.4 · v0.2.3 · v0.2.2 · v0.2.1 · v0.1.0 — still in this repository for the record. The
hold described above was against v0.2.4; 0.2.6 is the build this page recommends, with the
three opens at the top of the page still open. 0.2.5 was signed and never released.

Source is private; this repository holds install files only.
