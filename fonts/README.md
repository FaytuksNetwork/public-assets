# Fonts

The typefaces of Brand System v2.0, as free, open-licensed font files you can use on the web and in design tools.

| Role | Font | Files | Version | Licence |
|---|---|---|---|---|
| Display and headings | **Onest** | `onest/Onest-Variable.woff2`, `.ttf` | 2.001 | SIL OFL 1.1 |
| Body text | **Inter** | `inter/InterVariable.woff2`, `-Italic.woff2`, `.ttf` | 4.1 | SIL OFL 1.1 |
| Labels, data, timestamps | **JetBrains Mono** | `jetbrains-mono/JetBrainsMono-Variable.woff2`, `-Italic.woff2`, `.ttf` | 2.304 | SIL OFL 1.1 |

All of these are **variable fonts**: one file covers every weight (Onest and Inter 100–900, JetBrains Mono 100–800). Inter also has an optical-size axis.

- **`.woff2`** files are for websites.
- **`.ttf`** files are for installing on a computer (Figma, Photoshop, Premiere, OBS and so on).

Each folder includes the font's `OFL.txt` licence, which must stay next to the files. The OFL lets you use, embed and redistribute the fonts for free, including commercially. You may not sell the font files on their own.

### Why Onest and not Object Sans

The v2.0 guide sheets in `misc/brand-guide/` show **Object Sans** (Pangram Pangram foundry) for headlines. Object Sans needs a paid licence for web use, and its files can't be published in a public repository. So the brand now uses **Onest** for display and headings. It's a free font that is close in shape (wide round bowls, flat stroke ends, single-storey `g`) and weight. The guide sheets still show Object Sans, so expect small differences between them and the live site.

## Using it on the web

Copy this whole folder, keep its layout, and load the stylesheet:

```html
<link rel="stylesheet" href="/brand/fonts/typography.css">
```

`typography.css` sets up the fonts with `@font-face`, defines CSS variables for the three font stacks and the type scale, and provides one class per style (for example `.text-h1` or `.text-label-sm`).

```css
--font-display: "Onest", "Inter", ui-sans-serif, system-ui, sans-serif;
--font-body:    "Inter", ui-sans-serif, system-ui, sans-serif;
--font-mono:    "JetBrains Mono", ui-monospace, "SFMono-Regular", Menlo, monospace;
```

## Type scale

The sizes and line-heights below come straight from the v2.0 typography sheet. Weights and letter-spacing aren't written on the sheet; they were matched by eye.

| Style | Class | Font | Size / line-height | Weight | Letter-spacing | Case |
|---|---|---|---|---|---|---|
| Display / Hero | `.text-display-hero` | Onest | 72 / 76 px | 700 | −0.03em | |
| Display / XL | `.text-display-xl` | Onest | 56 / 60 px | 700 | −0.03em | |
| Heading / H1 | `.text-h1` | Onest | 48 / 50 px | 700 | −0.025em | |
| Heading / H2 | `.text-h2` | Onest | 40 / 42 px | 700 | −0.02em | |
| Heading / H3 | `.text-h3` | Onest | 32 / 32 px | 500 | −0.015em | |
| Heading / H4 | `.text-h4` | Onest | 24 / 24 px | 500 | −0.015em | |
| Label / XL | `.text-label-xl` | JetBrains Mono | 20 / 28 px | 700 | 0.1em | UPPER |
| Label / LG | `.text-label-lg` | JetBrains Mono | 16 / 24 px | 600 | 0.1em | UPPER |
| Label / MD | `.text-label-md` | JetBrains Mono | 14 / 20 px | 500 | 0.06em | UPPER |
| Label / SM | `.text-label-sm` | JetBrains Mono | 12 / 16 px | 500 | 0.04em | UPPER |
| Body / XL | `.text-body-xl` | Inter | 18 / 28 px | 400 | 0 | |
| Body / Large | `.text-body-lg` | Inter | 16 / 20 px | 400 | 0 | |
| Body / Medium | `.text-body-md` | Inter | 14 / 16 px | 400 | 0 | |

The sheet's header says "17 styles", but it only shows the 13 above. If the other four styles exist, the Graphics Team should add them here.

## Sources

| Font | Downloaded from |
|---|---|
| Inter 4.1 | Official release `Inter-4.1.zip` (github.com/rsms/inter) |
| JetBrains Mono 2.304 | Official release `JetBrainsMono-2.304.zip` (github.com/JetBrains/JetBrainsMono) |
| Onest 2.001 | Google Fonts repository (`ofl/onest`) |

The JetBrains Mono and Onest `.woff2` files were converted from the original `.ttf` files with fontTools. The glyphs were not modified. Inter's `.woff2` files are the official ones from its release.
