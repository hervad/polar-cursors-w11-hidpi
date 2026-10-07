# Polar Cursor Theme — Windows 11 HiDPI cursors

Rendered from the original vector art for every layer Windows picks at pointer sizes 1–15. Artwork by
**Eric Matthews (ECHM)** ([Polar Cursor Theme on gnome-look](https://www.gnome-look.org/p/999968)), packaged for Windows 10 1903+ / Windows 11.

![preview](docs/preview.png)

## Install
1. Download the zip for your variant from [Releases](../../releases/latest) and extract it.
2. Right-click **`install.inf`** → **Install** (accept the UAC prompt — it copies to `C:\Windows\Cursors`).
3. Mouse Properties opens → choose **Polar W11 HiDPI**, **Polar Blue W11 HiDPI** or **Polar Green W11 HiDPI** → **Apply**.

> Changing the pointer size in Settings can switch the scheme back to *Windows Default* — just re-select it.

**Uninstall:** run `uninstall.cmd`, pick another scheme, delete `C:\Windows\Cursors\<scheme>` as admin.

## What's embedded
| | Layers (px) |
|---|---|
| Static (`.cur`) | 32 48 64 72 80 96 112 120 128 144 160 168 176 192 200 208 216 224 240 256 |
| Animated (`.ani`) | 32 48 64 72 80 96 120 128 144 |

Contains every layer size Windows picks at 100–199 % display scale (measured), plus the sizes assumed for 200–300 %.
Details: [w11-cursor-toolkit docs](https://github.com/hervad/w11-cursor-toolkit).

## Why not the existing ports?
TODO: `w11cursor inspect` evidence for each existing port (layers, hotspots, roles).

## Notes
- **Variants:** orange, blue and green differ only in the colour of the busy/working spinner bar. Blue and Green
  recolour the bar by rotating the original orange's hue (+180° / +74°), measured from the upstream PNGs.
  Upstream's own recolouring script is an incomplete draft, so these colours approximate the originals
  (hue within 0.1°).
- **Location Select (Pin) and Person Select** have no Polar artwork; they use the pointing hand (Link Select)
  for now, like Windows' own Pin/Person cursors, which are hand variants. Dedicated badges may come later.
- **Shadow:** upstream's soft drop shadow isn't baked into the artwork, because Windows draws its own. For the
  closest look, turn on Settings > Accessibility > Mouse pointer and touch > **Enable mouse pointer shadow**.
- **Animation:** 18 frames per turn like upstream (60 ms each); Windows counts in 1/60 s, so frames alternate
  4/3 jiffies: 1,083 ms per turn instead of 1,080 ms.

## License
Artwork: GPL-2.0-or-later (same as upstream; author's notice in [COPYRIGHT](COPYRIGHT)). See [CREDITS.md](CREDITS.md) and [LICENSE](LICENSE).
