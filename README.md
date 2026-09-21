# EmulatR — Documentation and Releases

**EmulatR** is a full-system emulator of the DEC Alpha AXP architecture,
modelling the Alpha 21264 / 21264A (EV6 / EV67) processor and the 21272
"Tsunami / Typhoon" core-logic chipset, targeting AlphaServer DS10 / DS20 /
DS25 / ES40 / ES45-class machines.

Copyright © 2025, 2026 Timothy Peer / eNVy Systems, Inc. — https://envysys.com

---

## 📖 Read the guide

### **https://emulatrapp.github.io/EmulatR-docs/**

The complete User and Developer Reference — installation, operation, the SRM
console, storage, networking, architecture internals, and the appendices. It
is the same guide the installer lays down as `documentation/EmulatRGuide.pdf`,
and it is republished with each release.

A few pages worth starting from:

| | |
|---|---|
| [Installing with the Windows Installer](https://emulatrapp.github.io/EmulatR-docs/index.html?installing-with-the-windows-installer.html) | what the kit puts where, and what you must supply |
| [Booting / Configure a New OpenVMS Instance from an ISO](https://emulatrapp.github.io/EmulatR-docs/index.html?booting-from-an-iso-image.html) | a full OpenVMS installation from the emulated CD, console output and all |
| [Networking (EWA0)](https://emulatrapp.github.io/EmulatR-docs/index.html?networking-ewa0.html) | bridging the emulated DE500-BA to a real host adapter |
| [Known Gaps](https://emulatrapp.github.io/EmulatR-docs/index.html?known-gaps.html) | what does not work yet, stated plainly |
| [License](https://emulatrapp.github.io/EmulatR-docs/index.html?license.html) · [Terms of Use](https://emulatrapp.github.io/EmulatR-docs/index.html?terms-of-use.html) | the terms, before you install anything |

## 💾 Download

Installers are published as **[Releases](https://github.com/EmulatRApp/EmulatR-docs/releases)**
on this repository, not as files in the tree — a kit is ~50 MB and committing
each one would grow every clone forever.

**You supply your own firmware, operating system and media.** EmulatR ships
with none of them: SRM console images, OpenVMS distributions and disk images
are licensed material and are never included. The tools to create empty disks
are in the kit; what goes on them is yours. See
[Terms of Use §6](https://emulatrapp.github.io/EmulatR-docs/index.html?terms-of-use.html).

## ⚖️ Licence

EmulatR is released under the **eNVy Systems Non-Commercial License v1.1** —
free for personal, educational and non-commercial use. Commercial use requires
a separate licence from eNVy Systems, Inc.

---

## 🙏 Acknowledgments

This documentation was created with [Help+Manual](https://www.helpandmanual.com).

Thanks to the
[Performance Validator](https://www.softwareverify.com/product/performance-validator/)
team for the use of their tools during the development of this project.

---

## About this repository

This repository holds the **published documentation and the release
downloads**. The emulator source lives elsewhere and is not mirrored here.

The two were separated deliberately: documentation should be readable by
anyone from day one, while the source has its own release timing. Keeping them
apart means neither repository has to be half public and half private.

### For maintainers

**Pages are added by exporting the guide, never by dropping HTML in here.**
The site is a Help & Manual export, and three of its files are *generated* from
the topic set:

| File | What it carries |
|---|---|
| `helpman_navigation.js` | the contents tree |
| `hmkwindex.html` | the keyword index |
| `zoom_*.js` | the full-text search database |

A hand-placed page would be absent from all three — reachable only by direct
URL, invisible to the contents tree and to search — and the next export would
not know it existed. Add a topic in Help & Manual, then export the whole guide.

**`.nojekyll` is load-bearing. Do not delete it.** GitHub Pages runs Jekyll by
default, and Jekyll silently drops any file whose name begins with an
underscore. `__tools_build_emulatr_diag_bat.html` is such a page: in the
previous location it was committed, linked from the contents tree, and returned
404 on the live site for its entire existence, with nothing in the build log to
say so. The empty `.nojekyll` file disables Jekyll and publishes the export
verbatim.

### Previous location

The guide used to be served from `docs/` in the source repository. Old links
still work — that site forwards to this one, preserving the page and its query
string, so a saved bookmark lands on the same page here.
