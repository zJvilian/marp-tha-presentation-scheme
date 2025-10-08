# Quick Start Guide

Get started with your THA presentation in 3 simple steps!

## Step 1: Install Dependencies

```bash
npm install
```

## Step 2: Create Your Presentation

Create a new file in the `slides/` directory, for example `slides/my-presentation.md`:

```markdown
---
marp: true
theme: tha-theme
paginate: true
header: 'My Company'
footer: 'Confidential'
---

<!-- _class: lead -->

# My Amazing Presentation

## Subtitle Goes Here

---

# First Topic

- Point one
- Point two
- Point three

---

# Next Topic

More content here...

```

## Step 3: Build Your Presentation

```bash
npm run build
```

Your presentation will be in `output/my-presentation.html`! 🎉

## Need PDF or PowerPoint?

```bash
# Export to PDF
npm run build:pdf

# Export to PowerPoint
npm run build:pptx
```

## Live Preview While You Work

```bash
# Watch mode - rebuilds on save
npm run watch

# Or start a development server
npm run serve
```

## Tips

- Use `---` to separate slides
- Add `<!-- _class: lead -->` before a slide to make it a title slide
- Use standard Markdown: **bold**, *italic*, `code`, etc.
- Add images with `![alt text](image.png)`
- Create code blocks with triple backticks
- Check `slides/example-presentation.md` for more examples

## Need Help?

See the full [README.md](README.md) for detailed documentation.
