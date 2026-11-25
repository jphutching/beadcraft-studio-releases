# BeadCraft Studio — install

BeadCraft Studio is an Android app for beadwork charts. Paint a loom / square-stitch
chart with real bead codes, count it, work out what to buy from your stash, save the
project as a `.beadproj`, and print the chart as a PDF with rulers, a colour key and a
row-by-row pick-up list.

It asks for no permission at all — not even network access. It has no account, no ads and
no analytics, and it works with the phone offline.

## What you need

* Android 7.0 (API 24) or newer.
* About 4 MB of free space.

## Install

1. Open the [latest release](../../releases/latest) and download
   `BeadCraftStudio-v0.1.0.apk`.
2. Open the downloaded file. Android will ask whether to allow installs from that app
   (usually your browser or Files) — allow it, then tap **Install**.
3. Open **BeadCraft Studio** from your app list.

Or over adb:

    adb install -r -g BeadCraftStudio-v0.1.0.apk

Updates install over the top and keep your designs.

## What version 0.1.0 is

The first runnable build. It is a chart app: loom / square stitch only, chart-and-counts
only — it does not draw a thread path or guide construction. Sizes it reports are nominal,
from each bead line's own footprint. Every screen in it was driven on an Android 13
device at 1920 x 1200 before release.

Released versions are signed with one key, so an update from this page always installs
over the version you already have.
