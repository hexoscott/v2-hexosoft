# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

# Project

Astro-based website for Hexosoft.

# Stack

- **Framework**: Astro (minimal template)
- **Styling**: Tailwind CSS v4 (via `@tailwindcss/vite` plugin, no config file)
- **Language**: TypeScript (strict mode)
- **UI interactivity**: React (`@astrojs/react`) — ready for use, no components yet
- **Fonts**: Syne (display/headings) + JetBrains Mono (UI/body) — loaded via Google Fonts in `Layout.astro`

# Structure

```
src/
  layouts/
    Layout.astro     # Base layout — imports global.css, loads fonts, accepts title + description props
  pages/
    index.astro      # Homepage
  styles/
    global.css       # Tailwind entry point: @import "tailwindcss"
```

# Dev Commands

- `npm run dev` — start dev server
- `npm run build` — production build
- `npm run preview` — preview production build

# Conventions

- Tailwind v4: no `tailwind.config.*` file needed; utilities are auto-generated from source scans
- Custom font classes (`.font-display`, `.font-ui`) are defined in component `<style>` blocks
- React components should use the `.tsx` extension and can be dropped into `src/components/`
- Astro `<style>` is scoped by default; use `<style is:global>` for globals
