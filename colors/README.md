# Colors

The Faytuks Network color palette from Brand System v2.0: six brand colors, semantic tokens for light and dark mode, and a scale of text tones.

These values are copied from the "Foundations / Color" page of the Figma branding file, with one change: **Gold is the logo yellow `#FED506`**, not the `#FFD700` shown in Figma. That way the palette matches `logos/faytuks-mark-white-yellow.svg`.

| File | Use |
|---|---|
| `colors.css` | CSS variables, with light mode as the default and dark mode built in |
| `colors.tokens.json` | The same tokens in the W3C Design Tokens format, for Tailwind, Style Dictionary or Figma plugins |
| `color-palette-swatches.png` | Visual preview, rendered from `colors.css` |

## Brand palette

| Name | Hex | CSS variable |
|---|---|---|
| Blue Primary | `#1D4ED8` | `--color-blue-primary` |
| Blue Secondary | `#1B43B6` | `--color-blue-secondary` |
| Blue Light | `#759BFF` | `--color-blue-light` |
| Gold | `#FED506` | `--color-gold` |
| White | `#FCFDFF` | `--color-white` |
| Navy | `#00113E` | `--color-navy` |

`text/on-brand` uses pure white `#FFFFFF` (`--color-pure-white`). Everywhere else, "White" means the off-white `#FCFDFF`.

## Semantic tokens

Use these in components rather than the raw brand colors, so dark mode works automatically.

| Token | CSS variable | Light | Dark | Usage |
|---|---|---|---|---|
| bg/default | `--color-bg-default` | `#FCFDFF` | `#00113E` | Canvas, page backgrounds |
| bg/brand | `--color-bg-brand` | `#1D4ED8` | `#1D4ED8` | Primary CTA, active states |
| bg/accent | `--color-bg-accent` | `#FED506` | `#FED506` | Gold highlights, accent badges |
| text/default | `--color-text-default` | `#00113E` | `#FCFDFF` | Body copy, primary labels |
| text/muted | `--color-text-muted` | `#1B43B6` | `#759BFF` | Secondary labels, captions |
| text/brand | `--color-text-brand` | `#1D4ED8` | `#1B43B6` ⚠️ | Links, brand text emphasis |
| text/on-brand | `--color-text-on-brand` | `#FFFFFF` | `#FFFFFF` | Text on blue backgrounds |
| text/on-accent | `--color-text-on-accent` | `#00113E` | `#00113E` | Text on gold/accent backgrounds |
| border/default | `--color-border-default` | `#759BFF` | `#1B43B6` | Dividers, card outlines |
| border/brand | `--color-border-brand` | `#1D4ED8` | `#1D4ED8` | Focus rings, active borders |

## Text tones (light mode)

Ordered from dark to light, for ranking text by importance.

| Tone | Hex | Contrast on `#FCFDFF` |
|---|---|---|
| text/default | `#00113E` | 17.9 : 1 |
| text/secondary | `#14336B` | 12.0 : 1 |
| text/muted | `#1B43B6` | 8.2 : 1 |
| text/subtle | `#4B6FA8` | 5.0 : 1 |
| text/brand | `#1D4ED8` | 6.6 : 1 |
| text/disabled | `#9BAFC9` | 2.2 : 1 (disabled text is exempt from contrast rules) |

The brand system defines no text tones for dark mode yet.

## Dark mode

`colors.css` switches to dark mode:

- **automatically** when the visitor's system is set to dark, unless the page opts out with `<html data-theme="light">`
- **always** when the page sets `<html data-theme="dark">`

So a site with a theme toggle only needs to set `data-theme` on `<html>`.

## Accessibility check

These are WCAG 2.1 contrast ratios. Normal text needs at least 4.5 : 1, and large text and UI elements need 3 : 1.

| Pairing | Light | Dark |
|---|---|---|
| text/default on bg/default | 17.9 ✅ | 17.9 ✅ |
| text/muted on bg/default | 8.2 ✅ | 6.9 ✅ |
| text/brand on bg/default | 6.6 ✅ | **2.2 ❌** |
| text/on-brand on bg/brand | 6.7 ✅ | 6.7 ✅ |
| text/on-accent on bg/accent | 12.8 ✅ | 12.8 ✅ |
| border/default on bg/default | 2.6 | 2.2 |

⚠️ **In dark mode, `text/brand` (`#1B43B6` on navy) fails at 2.2 : 1**, so links and emphasized brand text would be hard to read. The value is copied unchanged from Figma. Suggested fix for the Graphics Team: use Blue Light `#759BFF` for dark `text/brand` (6.9 : 1).

The borders fall below 3 : 1. That's acceptable for decorative dividers and card outlines, but don't rely on `border/default` alone to show where a form field or button is.
