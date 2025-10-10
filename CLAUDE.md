# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal website for Jędrzej Tabaczyński (jedrzej.com) - an ultra-minimal, zero-dependency single-page site deployed on Vercel.

## Architecture

**Single-file static site**: The entire website is contained in `index.html` with embedded CSS. No build process, bundler, or framework is used.

**Key design principles**:
- Zero JavaScript dependencies (analytics is external script)
- Pure HTML/CSS with inline styles
- Mobile-first responsive design with breakpoints at 768px and 480px
- WCAG 2.1 AA accessibility compliance
- Bold typography using Inter font family

**Assets**:
- `jed-tabaczynski-headshot.webp` - Profile photo (referenced in index.html)
- Vercel Analytics injected via external script tag

## Development

**Local testing**: Open `index.html` directly in a browser - no server or build step required.

**Deployment**: Automatic deployment to jedrzej.com via Vercel on push to `main` branch. Configuration in `vercel.json` specifies no build/install/dev commands.

## Styling Architecture

All CSS is embedded in `<style>` tag within `index.html`:
- Uses CSS custom properties for animations (fadeIn)
- Responsive breakpoints: 768px (tablet), 480px (mobile)
- Key sections: `.photo-section`, `.name-section`, `.bio-section`, `.links-section`
- LinkedIn link styled as primary CTA button (`.link-item.linkedin`)
- Location is non-interactive (`.link-item.location`)

## Making Changes

When modifying the site:
1. Edit `index.html` directly
2. Test by opening file in browser
3. Commit changes - Vercel auto-deploys from main branch
4. Verify deployment at jedrzej.com

**Important**: There is no package.json, no dependencies, and no build tooling. Keep it simple.
