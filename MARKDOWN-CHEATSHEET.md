# Marp Markdown Cheat Sheet

Quick reference for creating presentations with Marp.

## Frontmatter (Required at top of file)

```markdown
---
marp: true
theme: tha-theme
paginate: true
header: 'Your Header Text'
footer: 'Your Footer Text'
---
```

## Slide Separator

Use `---` to create a new slide:

```markdown
# First Slide

Content here

---

# Second Slide

More content
```

## Special Slide Classes

### Title Slide (with gradient background)

```markdown
<!-- _class: lead -->

# Main Title

## Subtitle

Regular text
```

## Text Formatting

```markdown
**Bold text**
*Italic text*
***Bold and italic***
~~Strikethrough~~
`Inline code`
```

## Headers

```markdown
# H1 - Large header (blue, with orange underline)
## H2 - Medium header (blue, with orange left border)
### H3 - Small header
```

## Lists

### Unordered Lists
```markdown
- Item one
- Item two
  - Sub-item
  - Another sub-item
- Item three
```

### Ordered Lists
```markdown
1. First item
2. Second item
3. Third item
```

## Links

```markdown
[Link text](https://example.com)
```

## Images

```markdown
![Alt text](image.png)
![width:500px](image.png)  <!-- Specify width -->
![width:500px height:300px](image.png)  <!-- Width and height -->
```

## Code Blocks

### With Syntax Highlighting
````markdown
```javascript
function hello(name) {
  return `Hello, ${name}!`;
}
```
````

### Available Languages
- `javascript`, `python`, `java`, `css`, `html`, `bash`, `json`, etc.

## Tables

```markdown
| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |
```

## Blockquotes

```markdown
> This is a blockquote
> It can span multiple lines
```

## HTML (if needed)

You can use HTML for advanced formatting:

```markdown
<div style="text-align: center;">
  Centered text
</div>
```

## Custom Classes

The THA theme includes these utility classes:

```markdown
<!-- Apply to single slide -->
<!-- _class: lead -->

<!-- Text alignment -->
<div class="center">Centered content</div>

<!-- Text size -->
<span class="large">Large text</span>
<span class="small">Small text</span>

<!-- Colors -->
<span class="text-primary">Blue text</span>
<span class="text-accent">Orange text</span>
<span class="highlight">Highlighted text</span>
```

## Layout Tips

### Two Columns (use HTML)

```markdown
<div class="columns">
<div>

Left column content

</div>
<div>

Right column content

</div>
</div>
```

### Three Columns

```markdown
<div class="columns-3">
<div>

Column 1

</div>
<div>

Column 2

</div>
<div>

Column 3

</div>
</div>
```

## Comments (not shown in presentation)

```markdown
<!-- This is a comment -->
```

## Special Directives

```markdown
<!-- _paginate: false -->    <!-- Disable page numbers for this slide -->
<!-- _header: "" -->          <!-- Disable header for this slide -->
<!-- _footer: "" -->          <!-- Disable footer for this slide -->
```

## Example Slide

```markdown
---
marp: true
theme: tha-theme
paginate: true
---

<!-- _class: lead -->

# My Presentation

## By Your Name

---

# Introduction

This is my first slide with:

- Point one
- Point two
- Point three

---

## Code Example

Here's some code:

\```javascript
console.log("Hello, World!");
\```

---

# Thank You!

Questions?
```

## Resources

- See `slides/example-presentation.md` for more examples
- Check `QUICKSTART.md` for getting started
- Read `README.md` for full documentation
