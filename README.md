# marp-tha-presentation-scheme

A complete Marp project scheme with THA Corporate Design theme for creating professional presentations from Markdown files.

## Features

- 🎨 Custom THA Corporate Design theme
- 📝 Write presentations in Markdown
- 🚀 Automatic build process
- 📤 Export to HTML, PDF, and PPTX formats
- 🔄 Live preview with watch mode
- 🎯 Professional styling out of the box

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm (v6 or higher)

### Installation

1. Clone this repository
2. Install dependencies:

```bash
npm install
```

### Usage

#### Creating a New Presentation

1. Create a new Markdown file in the `slides/` directory
2. Add the required frontmatter at the top of your file:

```markdown
---
marp: true
theme: tha-theme
paginate: true
header: 'Your Header'
footer: 'Your Footer'
---

<!-- _class: lead -->

# Your Presentation Title

## Subtitle

---

# First Slide

Your content here...
```

#### Building Presentations

Run one of the following commands:

```bash
# Build all presentations to HTML
npm run build

# Build all presentations to PDF
npm run build:pdf

# Build all presentations to PPTX
npm run build:pptx

# Watch for changes and rebuild automatically
npm run watch

# Start a development server with live preview
npm run serve
```

All output files will be generated in the `output/` directory.

## Project Structure

```
marp-tha-presentation-scheme/
├── slides/                    # Your markdown presentation files
│   └── example-presentation.md
├── themes/                    # Custom theme files
│   └── tha-theme.css
├── output/                    # Generated presentations (git-ignored)
├── package.json              # Project configuration
└── README.md                 # This file
```

## Theme Customization

The THA theme includes:

- Professional color scheme with primary and accent colors
- Clear typography optimized for presentations
- Styled code blocks, tables, and lists
- Special slide classes:
  - `<!-- _class: lead -->` for title slides
  - Two-column layouts with `.columns` class
  - Emphasis classes: `.highlight`, `.text-primary`, `.text-accent`

To customize the theme, edit `themes/tha-theme.css` and modify the CSS variables:

```css
:root {
  --color-primary: #0066cc;
  --color-secondary: #004080;
  --color-accent: #ff6600;
  --color-background: #ffffff;
  --color-foreground: #333333;
}
```

## Example Presentation

An example presentation is included in `slides/example-presentation.md` that demonstrates all the features of the theme.

## Tips and Tricks

- Use `<!-- _class: lead -->` before a slide to make it a title slide
- Images are automatically centered and responsive
- Use backticks for inline code: `` `code` ``
- Create code blocks with triple backticks and language specification
- Add page numbers with `paginate: true` in frontmatter
- Customize headers and footers per presentation in frontmatter

## Contributing

Feel free to customize the theme and add your own enhancements!

## License

ISC
