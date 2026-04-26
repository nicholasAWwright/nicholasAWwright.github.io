# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Single-page portfolio site for `nicholasAWwright.github.io`, built with Jekyll and the `jekyll-theme-hacker` theme. Deployed automatically by GitHub Pages on every push to `main`.

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

Site available at `http://localhost:4000`.

## Adding or Editing Projects

All projects are managed in [`_data/projects.yml`](_data/projects.yml). Each entry renders as a card on the page — no HTML editing needed. Supported fields:

```yaml
- title: "Project Name"
  description: "Short description shown on the card."
  image: "assets/images/your-image.jpg"   # optional thumbnail
  links:                                   # optional, any number of buttons
    - label: "GitHub"
      url: "https://github.com/..."
    - label: "PDF"
      url: "assets/pdfs/file.pdf"
    - label: "Video"
      url: "https://youtube.com/..."
```

Place media files in `assets/images/`, `assets/pdfs/`, or `assets/videos/`.

## Key Files

| File | Purpose |
|---|---|
| `index.html` | Page structure — bio section + project grid |
| `_data/projects.yml` | Project data (the only file to edit for new projects) |
| `_includes/project-card.html` | Card template used for every project |
| `assets/css/style.scss` | Custom styles layered on top of the hacker theme |
| `_config.yml` | Site title, description, theme |

## Styling

`assets/css/style.scss` imports the hacker theme then adds portfolio-specific styles. Key colors from the hacker theme: background `#151515`, text `#cacaca`, accent green `#b5e853`. The `.btn` class is shared between bio links and project card links.
