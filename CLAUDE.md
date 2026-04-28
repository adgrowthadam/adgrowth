# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev       # Start dev server (localhost:4321)
npm run build     # Build for production (outputs to dist/)
npm run preview   # Preview production build locally
```

Node.js 22.12.0+ is required.

## Architecture

This is an [Astro](https://astro.build) v6 project using TypeScript in strict mode.

**Routing:** File-based via `src/pages/`. Each `.astro` file maps directly to a URL path.

**Layouts:** `src/layouts/Layout.astro` is the base HTML shell. Pages wrap their content in this layout via `<Layout>` component.

**Components:** Reusable UI in `src/components/`. Astro components use triple-dash frontmatter for imports and logic, with scoped `<style>` blocks.

**Static assets:** `src/assets/` for imported/optimized assets (SVG, images). `public/` for files served as-is (favicon, etc.).
