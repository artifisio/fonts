# Artifisio Fonts Registry

This repository is the **open-source font registry** for [Artifisio](https://artifisio.com) — typefaces released under the [SIL Open Font License 1.1](LICENSE), distributed as plain `woff2` / `otf` files with a ready-made `@font-face` stylesheet per family.

> **Auto-generated.** Maintained by Artifisio's sync pipeline. Do not send pull requests — [open an issue](../../issues) instead.

---

## Install via CLI

```bash
# Find a family
npx artifisio search "<vibe>" --kind font

# Add a family to your project (writes the font files, <slug>.css and ATTRIBUTION.md)
npx artifisio add <set-slug> --kind font

# Only the web format
npx artifisio add <set-slug> --kind font --format woff2
```

Then link the stylesheet and use the family name:

```html
<link rel="stylesheet" href="/fonts/multi-sans/multi-sans.css" />
<style>body { font-family: 'Multi Sans', sans-serif; }</style>
```

---

## Direct CDN usage (jsDelivr)

Every set ships a stylesheet whose `src` URLs are relative, so linking it from the CDN just works:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/artifisio/fonts@main/sets/multi-sans/multi-sans.css" />
```

Pin to a registry release for reproducible builds: `https://cdn.jsdelivr.net/gh/artifisio/fonts@v2026.10.04-1405-0aa34af/sets/<set-slug>/<file>`.

---

## Available families (1)

| Name | Slug | Styles | Scripts | Formats | Tags |
| ---- | ---- | ------ | ------- | ------- | ---- |
| [Multi Sans](sets/multi-sans) | `multi-sans` | Regular (400) | latin | otf, woff2 | sans, condensed, grotesque, display, headline |

Each set directory holds `meta.json` (family, styles, metrics, `@font-face` snippet, sha256 per file) next to the binaries.

---

## License

All fonts here are licensed under the [SIL Open Font License 1.1](LICENSE) with no Reserved Font Names: use, embed, bundle, modify and redistribute them freely, keep the license text with the font files, and do not sell the fonts by themselves. Attribution text lives in every set's `license.attribution`; `npx artifisio add` writes it to `ATTRIBUTION.md` for you.

---

## Registry details

| Field | Value |
| --- | --- |
| Registry version | `2026.10.04-1405-0aa34af` |
| CLI | [`artifisio`](https://www.npmjs.com/package/artifisio) |
| License | [OFL 1.1](LICENSE) |
| Other kinds | [`index.json`](index.json) lists every per-kind registry (illustrations, icons) |
| For agents | [`llms.txt`](llms.txt) |

Fonts are generated and curated at [artifisio.com](https://artifisio.com).
