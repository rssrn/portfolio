# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a portfolio website showcasing personal projects. The content is written in markdown and designed to be published via Quartz static site generator.

**Two-repository structure:**
- **portfolio** (this repo): Content source - markdown files and images
- **portfolio-quartz**: Quartz v4 static site generator setup, deploys to Cloudflare Pages

The portfolio-quartz repo includes the portfolio repo as a git submodule at `content/`.

## Content Structure

- **index.md**: Main portfolio page with project descriptions
- **Images**: PNG files named `index-N.png` (where N is a number) are screenshots/samples for projects
- **Project documentation**: Additional markdown files like `birdbird - Human Contribution Summary.md` and `NewsChart - Human Contribution Summary.md` provide supplementary context per project

## Markdown Conventions

This portfolio uses **Obsidian-flavored markdown** with specific syntax:

- **Image embedding**: `![[image-name.png]]` (double brackets, no path)
- **Image with alt text**: `![[image.png|Alt text description]]`
- **Clickable images**: `[![[image.png]]](image.png)` to make images link to themselves
- **Callouts**: Uses `> [!aside-left]` for image galleries positioned to the left
- **WikiLinks**: `[[Page Name]]` for internal links between markdown files

## Image Management

- Images should be in the root directory alongside markdown files
- Use descriptive alt text for accessibility (format: `![[image.png|Description]]`)
- When adding project screenshots, use sequential naming: `index-1.png`, `index-2.png`, etc.
- All images in project sections should be clickable links to the full-size version

## Publishing with Quartz (portfolio-quartz repo)

### Build Commands

In the portfolio-quartz directory:
- `npx quartz build` - Build the static site (output to `public/`)
- `npx quartz build --serve` - Build and serve locally for preview
- `npx quartz check` - TypeScript checking and code formatting validation
- `npx quartz format` - Auto-format code with Prettier

### Deployment

Deployed to Cloudflare Pages via `wrangler.jsonc`:
- Push to the portfolio-quartz repo triggers automatic deployment
- The `public/` directory is deployed as static assets
- Config in `wrangler.jsonc` specifies `compatibility_date` and assets directory

### Key Customizations from Vanilla Quartz

**quartz.config.ts:**
- Custom page title: "Ross Arnold - Portfolio"
- Popovers disabled (commented out `enablePopovers`)
- Ignore patterns: `["private", "templates", ".obsidian"]`
- Custom theme colors (lightMode and darkMode with specific hex values)
- Custom fonts: Schibsted Grotesk (header), Source Sans Pro (body), IBM Plex Mono (code)

**quartz.layout.ts:**
- Breadcrumbs conditionally hidden on index page only
- TableOfContents in desktop right sidebar
- Minimal footer with empty links object

**quartz/components/Head.tsx:**
- Umami analytics script injected manually (data-website-id: 51d20a9d-7594-47f7-a2bb-014ab9c4b61b)

**quartz/styles/custom.scss:**
- Custom responsive layout for `aside-left` callout (image galleries)
- Mobile: Full-width vertical stack
- Laptop (1100px+): Float left, 240px width, pulled into left margin
- Large desktop (1450px+): Increased to 340px width
- Custom ToC width adjustments per breakpoint (160px laptop, 250px desktop)

**static/ directory:**
- Currently empty but available for static HTML files (e.g., credits.html was added per git history)

### Content Update Workflow

When updating content in the portfolio repo:
1. Make changes to markdown/images in this portfolio repo
2. Commit and push changes here
3. In portfolio-quartz repo, update the content submodule:
   ```bash
   cd portfolio-quartz
   git submodule update --remote content
   git add content
   git commit -m "Content submodule: <describe changes>"
   git push
   ```
4. Cloudflare Pages automatically rebuilds and deploys

### Requirements

- Node.js >= 22
- npm >= 10.9.2

## Git Workflow

This is a simple documentation repository with straightforward commits for content updates. Common commit patterns:
- Adding new project sections
- Updating descriptions or technical details
- Adding/updating project screenshots
- Improving accessibility (alt text)

In portfolio-quartz, commits referencing content updates follow the pattern: `"Content submodule: <description>"`
