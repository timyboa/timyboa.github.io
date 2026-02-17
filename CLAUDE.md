# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static personal portfolio/resume website for Timothée Barattin, hosted on GitHub Pages at https://timyboa.github.io/. Built with vanilla HTML, CSS, and JavaScript — no frameworks, no build tools, no package manager.

## Development

No build step. Open `index.html` directly in a browser or serve with any static file server. Deploy by pushing to the `master` branch (GitHub Pages).

## Architecture

Single-page site with three key files:

- **index.html** — All content in one file. Three-column flexbox layout (profile photo, sidebar, main content) that collapses to single column on mobile. Uses `<details>/<summary>` for expandable sections. Inline `<script>` blocks dynamically calculate age, years of experience, and role durations.
- **css/style.css** — Desktop-first styles. 900px max-width container, flexbox layout, CSS nesting syntax, print styles, expand/collapse animations. Font: Quicksand (Google Fonts).
- **css/mobile.css** — Mobile overrides at `max-width: 649px` breakpoint.
- **portfolio.js** — Handles responsive toggling of `<details>` elements (open on desktop, closed on mobile) and "See More/See Less" button behavior.

## Conventions

- **Commit messages** follow `[ACTION] Description` format (e.g., `[UPDATE] Minor skill update`).
- **Editor settings**: 2-space tabs, format on save (see `.vscode/settings.json`).
- **Images**: WebP format with multiple density variants (`_150`, `_300`, `_450`) served via `<picture>` element.
