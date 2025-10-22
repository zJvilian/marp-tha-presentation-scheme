# Marp THA Presentation Scheme

Starter kit for authoring slide decks with [Marp](https://marp.app/) using a Thai corporate-inspired theme. The repo includes a ready-made folder structure, a reusable custom theme, and helper scripts for exporting decks.

## Structure

```
.
├── assets/              # Images and other media used across decks
├── slides/
│   ├── decks/           # Entry-point decks (main.md ships as an example)
│   └── partials/        # Reusable slide snippets such as the title slide
├── themes/
│   └── tha-corporate.css  # Custom Marp theme definition
├── marp.config.js       # CLI configuration (input/output, theme registration)
├── package.json         # Marp CLI dependency and helper scripts
└── .gitignore           # Ignores build artefacts and dependencies
```

## Prerequisites

- Node.js ≥ 18 (for `npm` and the Marp CLI)
- Run `npm install` once Node.js is available to install dependencies

> **Heads-up:** The current environment does not expose `npm`. Install Node.js or open the project in a Node-enabled terminal before running the scripts below.

## Working with decks

1. Create new decks inside `slides/decks/` using the front matter template from `slides/decks/main.md`.
2. Reuse snippets from `slides/partials/` by copying them into your deck or creating additional partial files.
3. Place shared illustrations in `assets/` and reference them with relative paths.

Each deck should include the following front matter to activate the custom theme:

```yaml
---
marp: true
theme: tha-corporate
---
```

## CLI commands

```powershell
npm run watch        # Live preview with automatic rebuilds (requires Node.js)
npm run build        # Export all decks to the dist/ folder
npm run export:pdf   # Produce a PDF version of slides/decks/main.md
npm run export:pptx  # Produce a PowerPoint version of slides/decks/main.md
```

Generated files land in `dist/`. Remember to add the folder to `.gitignore` (already handled).

## Customizing the theme

- Update colors, fonts, and layout tokens in `themes/tha-corporate.css`.
- Add additional selectors (e.g., `.title-slide`) to tailor specific slide types.
- Register new themes by cloning the CSS file, updating the `/* @theme ... */` header, and adding the file to the `themeSet` array in `marp.config.js`.

## Next steps

- Install Node.js and the Marp CLI dependencies (`npm install`).
- Duplicate `slides/decks/main.md` for each presentation and adapt the contents.
- Add more partials under `slides/partials/` to streamline repeated slide patterns.
