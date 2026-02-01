# Pandoc Template with Image Lightbox

This directory contains a standalone Pandoc HTML5 template with a Notion/Medium-style image lightbox feature.

## Files

- `template.html` - Standalone Pandoc HTML5 template with embedded CSS and JavaScript

## Usage

### Basic Usage

```bash
pandoc your-document.md -o output.html --template=template.html --standalone
```

### With Metadata

If your Markdown has a YAML front matter:

```yaml
---
title: "My Document Title"
author: "Your Name"
date: "2024-01-01"
lang: fr
---
```

Then use:

```bash
pandoc your-document.md -o output.html --template=template.html --standalone
```

### With Table of Contents

To generate a table of contents, use the `--toc` flag:

```bash
pandoc your-document.md -o output.html --template=template.html --standalone --toc
```

The TOC will appear right after the document title. You can customize the TOC title using:

```bash
pandoc your-document.md -o output.html --template=template.html --standalone --toc --toc-depth=3
```

### Features

- **Standalone**: All CSS and JavaScript are embedded in the template
- **Table of Contents**: Generate a TOC with `--toc` flag (appears after the title)
- **Image Lightbox**: Click any image to view it in a full-screen modal
  - Click × button to close
  - Click outside image to close
  - Press Escape key to close
- **Syntax Highlighting**: Code blocks are styled with a dark theme
- **Responsive**: Works on mobile and desktop
- **Clean Design**: Simple, readable typography

## Customization

The template uses Pandoc variables:
- `$title$` - Document title
- `$body$` - Main content
- `$lang$` - Language code
- `$author$` - Author name(s)
- `$date$` - Publication date
- And more standard Pandoc variables

To customize styles, edit the `<style>` section in `template.html`.
