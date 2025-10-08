# Contributing to THA Presentation Scheme

Thank you for your interest in contributing! This guide will help you customize and extend the project.

## Customizing the Theme

### Colors

Edit `themes/tha-theme.css` and modify the CSS variables at the top:

```css
:root {
  --color-primary: #0066cc;      /* Main brand color */
  --color-secondary: #004080;    /* Secondary brand color */
  --color-accent: #ff6600;       /* Accent/highlight color */
  --color-background: #ffffff;   /* Slide background */
  --color-foreground: #333333;   /* Text color */
  --color-light-gray: #f5f5f5;   /* Code blocks, tables */
  --color-gray: #cccccc;         /* Borders, dividers */
}
```

### Typography

Change the font family in the same file:

```css
:root {
  font-family: 'Your Font', 'Fallback Font', sans-serif;
}
```

### Slide Layout

Modify the section dimensions in `themes/tha-theme.css`:

```css
section {
  width: 1280px;   /* Default: 1280px */
  height: 720px;   /* Default: 720px (16:9) */
  padding: 60px 80px;
}
```

Common aspect ratios:
- 16:9 - 1280x720 (default, most common)
- 16:10 - 1280x800
- 4:3 - 1024x768

## Adding New Features

### Custom Slide Classes

Add new classes to `themes/tha-theme.css`:

```css
/* Two-column layout */
section.two-columns {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
}
```

Use in your markdown:

```markdown
<!-- _class: two-columns -->

# Slide Title

Left column content

Right column content
```

### Custom Styling for Specific Elements

Add styles for specific Markdown elements:

```css
/* Style for important callouts */
blockquote.important {
  border-left-color: red;
  background-color: #fff5f5;
}
```

## Testing Your Changes

1. Make changes to the theme CSS
2. Rebuild presentations: `npm run build`
3. Open the HTML in your browser to preview
4. Use live preview: `npm run serve`

## Project Structure

```
marp-tha-presentation-scheme/
├── slides/           # Markdown source files
├── themes/           # Theme CSS files
│   └── tha-theme.css # Main theme
├── output/           # Generated presentations
├── .marprc.yml       # Marp configuration
└── package.json      # Dependencies and scripts
```

## Tips

- Always test your theme with multiple slides
- Check that code blocks, tables, and images look good
- Test in different browsers
- Keep the theme accessible (good contrast, readable fonts)
- Document any new features you add

## Resources

- [Marp Documentation](https://marpit.marp.app/)
- [Marp CLI Documentation](https://github.com/marp-team/marp-cli)
- [Marpit Framework](https://marpit.marp.app/markdown)
- [CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)

## Questions?

If you have questions or need help, please open an issue on GitHub.
