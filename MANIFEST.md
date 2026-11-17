# Asset Manifest

Every file in this repository, where it came from, and what it is. Update this file in the same pull request whenever assets are added, renamed or removed.

## Uploaded

| Path | Original filename | Dimensions | Format | Description |
|---|---|---|---|---|
| `logos/faytuks-mark-white-yellow.svg` | `faytukslogo.svg` | 1080 × 380 (viewBox) | SVG | FN mark: white "FN" letters with the eye, plus three yellow (`#FED506`) signal arcs. No wordmark. Intended for dark backgrounds. Inkscape metadata removed, size changed from mm to unitless, optimized with SVGO 3.3.2 (8.6 KB → 3.9 KB). The before and after renders look identical. |
| `misc/brand-guide/brand-system-v2-typography-4320x6477.png` | `Typography - FN.png` | 4320 × 6477 | PNG | Branding System v2.0, typography sheet: Object Sans / JetBrains Mono / Inter, type scale with 13 styles shown (the header says 17) across Display, Heading, Label and Body, plus "In context" UI examples. |
| `misc/brand-guide/brand-system-v2-in-context-4320x1827.png` | `In Context.png` | 4320 × 1827 | PNG | Branding System v2.0, "In context" examples: article card with a LIVE badge, stats card, "On air now" schedule card. The same content as the bottom of the typography sheet, as a separate file. |
| `fonts/README.md` | (new) | | Markdown | Typography spec: font roles, type-scale table, web usage, licences and sources. |
| `fonts/typography.css` | (new) | | CSS | `@font-face` rules, font-stack and type-scale CSS variables, one class per style. |
| `fonts/type-scale-specimen.png` | (new) | 2640 × 2158 | PNG | Preview of all 13 styles, rendered from `typography.css`. |
| `fonts/onest/Onest-Variable.woff2` / `.ttf` | `Onest[wght].ttf` (Google Fonts) | variable, wght 100–900 | WOFF2 / TTF | Display and heading font, v2.001. Free stand-in for Object Sans. |
| `fonts/onest/OFL.txt` | `OFL.txt` | | Text | SIL Open Font License 1.1 for Onest. |
| `fonts/inter/InterVariable.woff2`, `InterVariable-Italic.woff2`, `.ttf` | `Inter-4.1.zip` (official release) | variable, wght 100–900, opsz 14–32 | WOFF2 / TTF | Body font, v4.1. |
| `fonts/inter/OFL.txt` | `LICENSE.txt` | | Text | SIL Open Font License 1.1 for Inter. |
| `fonts/jetbrains-mono/JetBrainsMono-Variable.woff2`, `-Variable-Italic.woff2`, `.ttf` | `JetBrainsMono-2.304.zip` (official release) | variable, wght 100–800 | WOFF2 / TTF | Label and data font, v2.304. |
| `fonts/jetbrains-mono/OFL.txt` | `OFL.txt` | | Text | SIL Open Font License 1.1 for JetBrains Mono. |
| `colors/README.md` | (new) | | Markdown | Palette, semantic light/dark tokens, text tones, dark-mode usage, WCAG contrast check. |
| `colors/colors.css` | (new) | | CSS | Brand, text-tone and semantic CSS variables. Light is the default; dark applies via `prefers-color-scheme` or `data-theme="dark"`. |
| `colors/colors.tokens.json` | (new) | | JSON | The same tokens in the W3C Design Tokens format. |
| `colors/color-palette-swatches.png` | (new) | 2992 × 1858 | PNG | Swatches plus light and dark example cards, rendered from `colors.css`. |

## Excluded

None of the files in this batch were excluded.

The main graphics archive (`Faytuks_Graphics-2.zip`, ~170 files) is **not part of this batch**. It will come in a separate pull request, with its own entries and exclusions added here.

## Known gaps

- **Only one vector file exists.** `faytuks-mark-white-yellow.svg` is the only SVG. Every other logo is raster.
- **Missing logo variants:** no navy/dark-on-light logo, no single-color (mono) version, and no favicon or app icons (`/icons` is empty).
- **No full-logo or wordmark vector.** The SVG is the mark only, without "FAYTUKS NETWORK".
- **Gold differs from Figma.** Gold is the logo yellow `#FED506` in `/colors`, but the Figma branding file still shows `#FFD700`. Figma should be updated to match.
- **Two versions of the mark exist.** In the raster "Dark" logo the N's diagonal runs unbroken behind the eye. In the SVG the diagonal is cut where the eye sits. Someone needs to decide which is official.
- **Dark-mode `text/brand` fails contrast.** `#1B43B6` on navy is 2.2 : 1 (WCAG AA needs 4.5 : 1). Suggested fix: `#759BFF`. Dark-mode text tones are also not defined yet.
- **Headline font differs from the guide sheets.** Object Sans (paid web licence) has been replaced by the free font Onest in `/fonts`, but the v2.0 guide sheets still show Object Sans. Weights and letter-spacing in the type scale were matched by eye.
- **Type scale is incomplete.** The typography sheet says "17 styles" but shows only 13.
- **No web BREAKING badge style.** The brand guide shows LIVE and ON AIR badges, but not BREAKING.
