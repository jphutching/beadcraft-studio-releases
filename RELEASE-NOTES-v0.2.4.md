# beadcraft studio 0.2.4

this builds on 0.2.3 and changes one thing: the version number.

## why a build that changes nothing

0.2.3 was put on a phone and its own update check found this release, offered it,
and then refused the download with "the release's file is not where github serves
release files". the cause was in the update policy: github used to answer a release
download with

    release-assets.githubusercontent.com/github-production-release-asset-2e65be/...

and now answers with

    release-assets.githubusercontent.com/github-production-release-asset/<id>/<uuid>?sp=r&...

so the address was refused as a lookalike, and the download never started.

0.2.3 carries the repair — it was rebuilt today with both shapes accepted, and the
phone it was installed on is the one that found the fault. 0.2.4 is the same studio
as 0.2.3 with the version raised, published so that the repaired path could be
walked on a real phone from a build in the field: check → download → install, one
version up, designs intact.

## what it means for a phone already out there

- on 0.2.3: the update check works, and this release is what it installs.
- on 0.2.2 or earlier: the check still finds a newer version, but the download is
  refused, because those builds only know the old address. install 0.2.3 or later
  from the release page once and the update check works from then on.

## walked on a phone, not only in a test

on an s23 ultra already carrying 0.2.3 (versionCode 8), the app's own check found this
release, offered it as 0.2.4, downloaded it, and handed it to android's installer. the
installer asked "update this app?", play protect offered its scan on a build that did not
come from play, and the install then completed:

    before   versionCode 8   0.2.3   first install 2026-11-25 17:38:38
    after    versionCode 9   0.2.4   first install 2026-11-25 17:38:38 (unchanged)
    design   rev 0bee82e6, 5 beads, 30 x 24 — still open after the update

nothing was installed by adb for that step, and no design was removed. the two android
panels in the middle of it — "update this app?" and play protect's scan — belong to the
phone, not to the app, and are described on the install page.

## the file

    BeadCraftStudio-v0.2.4.apk
    172904 bytes
    sha256 9ce7e28415f3e54a7f0a667532d247a34093f295c69df9658ddd0048d62ded39
    versionCode 9, version 0.2.4, minSdk 24, targetSdk 34
    signed with the same key as every earlier build:
    certificate 5295f944 fd1a0906 1e3acd34 acd5c408 be89437f 5b11ec89 7031d416 90caede7

permissions are unchanged and still only two: INTERNET and REQUEST_INSTALL_PACKAGES.

## the install qr

`BeadCraftStudio-v0.2.4-qr.png` in this release carries one address and nothing else:

    https://github.com/jphutching/beadcraft-studio-releases/releases/download/v0.2.4/BeadCraftStudio-v0.2.4.apk

that string was decoded back out of the published png (zbar/pyzbar, one symbol, exact
match), so the code opens this release's apk and not an older one. `SHA256SUMS.txt` covers
the apk and the png.
