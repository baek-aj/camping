<!-- Created: 2026-05-17 07:43 -->
# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-file static web page for a camping event ("메이메이 소풍 2025"). All HTML, CSS, and JavaScript live in `index.html` — no build tools, no dependencies, no backend.

## Development

Edit `index.html` directly and open in a browser. No installation or build step needed.

To preview locally:
```bash
open index.html          # macOS
python3 -m http.server   # serve at http://localhost:8000
```

## Architecture

Everything is in `index.html`:

- **CSS variables** at the top of `<style>` define the color palette (sky blues, sunset oranges, greens)
- **5-section tab layout**: Schedule → Menu → Checklist → Roles → Notice; tab switching is handled by `switchTab(id, btn)`
- **Checklist state** is managed in a plain JS object; checkboxes update a progress bar in real-time
- **Star animation** in the hero: 28 elements injected by JS with random positions and `twinkle` keyframe delays
- **Google Fonts** (Noto Sans KR, Nanum Myeongjo) are the only external dependency — loaded via `<link>`

## Deployment

Push to GitHub — the repo is served via GitHub Pages.
