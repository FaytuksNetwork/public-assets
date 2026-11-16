# Asset Manifest

Every file in this repository, where it came from, and what it is. Update this file in the same pull request whenever assets are added, renamed or removed.

## Uploaded

| Path | Original filename | Dimensions | Format | Description |
|---|---|---|---|---|
| `logos/faytuks-mark-white-yellow.svg` | `faytukslogo.svg` | 1080 × 380 (viewBox) | SVG | FN mark: white "FN" letters with the eye, plus three yellow (`#FED506`) signal arcs. No wordmark. Intended for dark backgrounds. Inkscape metadata removed, size changed from mm to unitless, optimized with SVGO 3.3.2 (8.6 KB → 3.9 KB). The before and after renders look identical. |
| `misc/brand-guide/brand-system-v2-typography-4320x6477.png` | `Typography - FN.png` | 4320 × 6477 | PNG | Branding System v2.0, typography sheet: Object Sans / JetBrains Mono / Inter, full 17-style type scale (Display, Heading, Label, Body), plus "In context" UI examples. |
| `misc/brand-guide/brand-system-v2-in-context-4320x1827.png` | `In Context.png` | 4320 × 1827 | PNG | Branding System v2.0, "In context" examples: article card with a LIVE badge, stats card, "On air now" schedule card. The same content as the bottom of the typography sheet, as a separate file. |

## Excluded

None of the files in this batch were excluded.

The main graphics archive (`Faytuks_Graphics-2.zip`, ~170 files) is **not part of this batch**. It will come in a separate pull request, with its own entries and exclusions added here.

## Known gaps

- **Only one vector file exists.** `faytuks-mark-white-yellow.svg` is the only SVG. Every other logo is raster.
- **Missing logo variants:** no navy/dark-on-light logo, no single-color (mono) version, and no favicon or app icons (`/icons` is empty).
- **No full-logo or wordmark vector.** The SVG is the mark only, without "FAYTUKS NETWORK".
- **Yellow conflict:** the logo uses `#FED506`, but the brand color is specified as `#FFD700`. Undecided, so the file has not been changed.
- **Two versions of the mark exist.** In the raster "Dark" logo the N's diagonal runs unbroken behind the eye. In the SVG the diagonal is cut where the eye sits. Someone needs to decide which is official.
- **No dark-mode color tokens** in the brand system.
- **No font files.** Object Sans needs a paid web licence. Inter and JetBrains Mono are under the SIL Open Font License, so they could be added.
- **No web BREAKING badge style.** The brand guide shows LIVE and ON AIR badges, but not BREAKING.
