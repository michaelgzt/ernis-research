---
title: "Markdown Feature Showcase"
date: 2026-02-28
authors:
  - ERNIS Team
tags:
  - markdown
  - gfm
  - testing
summary: "A single post to test how Markdown renders across headings, lists, code, tables, links, images, and more."
---

# Heading Level 1

This post is a visual test page for Markdown rendering.  
The line above ends with two spaces to force a hard line break.

## Heading Level 2

### Heading Level 3

#### Heading Level 4

##### Heading Level 5

###### Heading Level 6

## Text Styling

- *Italic text*
- **Bold text**
- ***Bold + italic***
- ~~Strikethrough~~
- `inline code`
- Escaped characters: \*not italic\*, \#not heading

## Links

- Inline link: [Maastricht University](https://www.maastrichtuniversity.nl/)
- Autolink URL: https://github.com/
- Reference link: [GitHub Docs][gh-docs]

[gh-docs]: https://docs.github.com/

## Images

![Placeholder image for markdown testing](/assets/images/blog/ood-placeholder.svg "Markdown test image")

## Blockquotes

> This is a blockquote.
>
> It supports multiple paragraphs.
>
> > Nested blockquote level 2.

## Lists

### Unordered

- First item
- Second item
  - Nested item A
  - Nested item B
- Third item

### Ordered

1. Step one
2. Step two
3. Step three
   1. Sub-step three-A
   2. Sub-step three-B

### Task List (GFM)

- [x] Completed task
- [ ] Open task
- [x] Another completed task

## Horizontal Rule

---

## Code Blocks

```bash
bundle exec jekyll serve --livereload
```

```python
def greet(name: str) -> str:
    return f"Hello, {name}!"
```

```json
{
  "project": "ernis-research",
  "feature": "markdown-showcase",
  "enabled": true
}
```

## Table (GFM)

| Feature | Syntax Example | Status |
| :------ | :------------- | -----: |
| Bold | `**text**` | ✅ |
| Task list | `- [x] item` | ✅ |
| Table | `\| a \| b \|` | ✅ |

## Footnotes (kramdown/common support)

You can place a footnote marker like this.[^1]

[^1]: This is the footnote content.

## Inline HTML (allowed in Markdown)

<details>
  <summary>Click to expand</summary>
  <p>This block uses inline HTML inside Markdown.</p>
</details>

## Mixed Content Test

1. A list item with a paragraph.

   Continued paragraph text under the same list item.

2. A list item with code:

   ```text
   nested fenced block under ordered list item
   ```

3. A list item with quote:

   > Quoted text inside a list item.

