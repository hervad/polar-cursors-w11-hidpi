# Credits

**Artwork:** Polar Cursor Theme by Eric Matthews (ECHM) - https://www.gnome-look.org/p/999968
(GPL-2.0-or-later). Copyright (C) 2005 Eric Matthews.
The author's licence notice is in [COPYRIGHT](COPYRIGHT), copied byte-for-byte from the upstream tarball,
where it shipped as `COPYRIGHT~` (identical in all three variant folders; there is no file named
`COPYRIGHT` without the tilde upstream). The full GPL-2.0 text is in [LICENSE](LICENSE)
(from https://www.gnu.org/licenses/old-licenses/gpl-2.0.txt).
**Source provenance:** `upstream/27913-PolarCursorThemes.tar.bz2` is the original archive from the gnome-look page
above, committed unmodified (417,876 bytes, SHA-256 `03d77c528c89f507eb240d4efd2dfcb0b5d8245cd20c94f9cf8a87e50c16f598`).
The build verifies that hash and reads only `PolarCursorTheme/Source/Cursors.svg` from it (`w11cursor unpack theme.toml`).
**Windows 11 HiDPI port:** Vadym Herman ([@hervad](https://github.com/hervad)), built with
[w11-cursor-toolkit](https://github.com/hervad/w11-cursor-toolkit)

## Changes from upstream
- Re-rendered from the original SVG master (`Source/Cursors.svg`) at every Windows cursor size (no resampling).
  Cursors are cut from its Inkscape layers; Help = Arrow + Info, Working = Arrow + AppSpinner (as upstream's PNGs).
- Horizontal and diagonal resize cursors: the NS arrow transposed / rotated by ±45°, as in upstream's PNGs.
- Busy/Working: 18 frames made by rotating the spinner bar 10° per frame (upstream shipped pre-rendered PNGs);
  60 ms per frame approximated as alternating 4/3 jiffies (1,083 ms per turn instead of 1,080 ms).
- Blue/Green: spinner bar hue rotated +180° / +74° (measured from upstream's PNGs; upstream's recolour script
  is an incomplete draft).
- Drop shadow not reproduced in the artwork (Windows draws its own; upstream's PNGs had one baked in, the SVG master does not).
- Hotspots from upstream's `*.conf`, rescaled per size; Windows role mapping incl. Pin and Person
  (both use the Link hand for now). No files in overrides/.
