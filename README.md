# Spiral Tower Ludogenics

Static site built with [Eleventy](https://www.11ty.dev/), hosted on GitHub Pages.

## Local development

```bash
npm install
npm run dev
```

Opens a local server at `http://localhost:8080`.

## Adding content

### Blog post

Create a Markdown file in `src/blog/`:

```
src/blog/2026-06-15-my-post.md
```

```yaml
---
title: "My Post Title"
date: 2026-06-15
description: "A short description."
---

Post content goes here.
```

### Essay

Same format, in `src/essays/`:

```
src/essays/my-essay-slug.md
```

### Game project

Create a Markdown file in `src/projects/`:

```yaml
---
title: "Game Name"
description: "One-line description for the card."
status: "In Development"  # or "Released", "Prototype"
links:
  - label: "Itch.io"
    url: "https://example.itch.io/game"
  - label: "Steam"
    url: "https://store.steampowered.com/app/..."
---

Longer description and details here.
```

## Deployment

Pushes to `main` trigger a GitHub Actions workflow that builds and deploys to GitHub Pages.

**One-time setup:** In your GitHub repo settings, go to **Settings > Pages** and set the source to **GitHub Actions**.

## Build commands

| Command | Description |
|---|---|
| `npm run dev` | Local dev server with hot reload |
| `npm run build` | Build to `_site/` |
| `npm run build:gh` | Build with `/spiral-tower-ludogenics/` path prefix (used by CI) |
