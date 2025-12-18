# Fuwari Project Context

## Project Overview
**Fuwari** is a static blog template built with **Astro**, **Svelte**, and **Tailwind CSS**. It is designed to be highly customizable, performant, and visually appealing with features like smooth page transitions, light/dark mode, and rich content integrations.

**Key Features:**
*   **Framework:** Astro 5.x
*   **Styling:** Tailwind CSS 3.x with extensive customization.
*   **Interactivity:** Svelte 5.x for interactive components.
*   **Content:** Markdown-based content management with type-safe frontmatter (Astro Content Collections).
*   **Features:** Search, Table of Contents, Image Fallback, Anti-Leech protection, Analytics (Umami, GA).

## Architecture & Structure

### Key Directories
*   `src/content/posts/`: Stores the blog posts (Markdown/MDX).
*   `src/config.ts`: **Primary configuration file** for site settings, navigation, profile info, and feature toggles.
*   `src/components/`: Reusable UI components (Astro and Svelte).
*   `src/layouts/`: Page layouts (e.g., `MainGridLayout.astro`).
*   `src/pages/`: Astro file-based routing. Includes API routes like `rss.xml.ts`.
*   `src/plugins/`: Custom Rehype/Remark plugins for content processing.
*   `public/`: Static assets (favicons, images, `robots.txt` generation).
*   `scripts/`: Utility scripts for migration and other tasks.

### Key Configuration Files
*   `astro.config.mjs`: Astro project configuration, integration setup (Tailwind, Svelte, Sitemap, Expressive Code).
*   `src/config.ts`: User-facing configuration. Edit this to change site title, author, links, etc.
*   `src/content/config.ts`: Schema definitions for content collections (`posts`, `spec`, `assets`).
*   `tailwind.config.cjs`: Tailwind CSS configuration.

## Development Workflow

### Prerequisites
*   Node.js (LTS recommended)
*   pnpm (Project uses `pnpm-lock.yaml`)

### Common Commands
Run these commands from the project root:

| Command | Description |
| :--- | :--- |
| `pnpm install` | Install dependencies (also run `pnpm add sharp` if needed). |
| `pnpm dev` | Start the local development server at `localhost:4321`. |
| `pnpm build` | Build the site for production output to `./dist/`. |
| `pnpm preview` | Preview the production build locally. |
| `pnpm new-post <filename>` | Create a new blog post template in `src/content/posts/`. |
| `pnpm lint` | Run Biome to lint the codebase. |
| `pnpm format` | Run Biome to format the codebase. |

### Creating Content
Posts are located in `src/content/posts`.
Frontmatter schema includes:
```yaml
---
title: "Post Title"
published: 2023-01-01
description: "Short description"
image: "./cover.jpg"
tags: ["Tag1", "Tag2"]
category: "Category"
draft: false
---
```

## Conventions
*   **Styling:** Use Tailwind CSS utility classes. Custom styles are in `src/styles/`.
*   **Components:** Prefer Astro components for static content and Svelte for interactive elements.
*   **Type Safety:** Strict TypeScript mode is enabled. Use defined types in `src/types/`.
*   **Formatting:** The project uses Biome for formatting and linting (`biome.json`).

## Integrations & Plugins
*   **Expressive Code:** Used for syntax highlighting with custom themes.
*   **Remark/Rehype:** Extensive chain for processing Markdown, including math (Katex), directives, and custom components (Admonitions, Github Cards).
*   **Swup:** Used for smooth page transitions (configured in `astro.config.mjs`).
