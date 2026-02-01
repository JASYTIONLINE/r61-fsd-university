# FSD University Content

This repository contains the course content for FSD University, published using [Quartz](https://quartz.jzhao.xyz/) and hosted on GitHub Pages.

## Setup

### Prerequisites

- Node.js 20 or higher
- Git
- GitHub account

### Initial Setup

**Important**: Quartz requires its core files to be present. You have two options:

#### Option 1: Initialize with Quartz CLI (Recommended)
1. Run the Quartz initialization:
   ```bash
   npx quartz create
   ```
   This will set up the necessary Quartz files and structure.

2. Move your existing content into the appropriate location (usually the root or `content/` folder depending on Quartz version).

#### Option 2: Clone Quartz Template
1. Clone the official Quartz repository:
   ```bash
   git clone https://github.com/jackyzha0/quartz.git
   cd quartz
   ```

2. Copy your content files into the repository.

3. Update `quartz.config.ts` with your settings.

### After Setup

1. Install dependencies (if needed):
   ```bash
   npm install
   ```

2. Preview locally:
   ```bash
   npm run preview
   ```

3. Build for production:
   ```bash
   npm run build
   ```

## Editing in Obsidian

1. Open this folder as a vault in Obsidian
2. Edit your markdown files directly
3. Use the Git plugin (recommended) to commit and push changes
4. Changes will automatically deploy to GitHub Pages via GitHub Actions

## Configuration

- **Content**: All markdown files in the root and subdirectories
- **Configuration**: `quartz.config.ts`
- **Deployment**: Automatic via GitHub Actions (`.github/workflows/deploy.yml`)
- **Repository**: https://github.com/JASYTIONLINE/r61-fsd-university

## Important Notes

- The `baseUrl` in `quartz.config.ts` is configured for this repository
- Obsidian-specific files (`.obsidian/`) are ignored by git
- The site will be available at `https://jasytionline.github.io/r61-fsd-university`

## Publishing

1. Make changes to your markdown files
2. Commit and push to the `main` branch
3. GitHub Actions will automatically build and deploy to GitHub Pages
4. Your site will be live in a few minutes

## Local Development

- `npm run preview` - Start local development server
- `npm run build` - Build static site
- `npm run sync` - Sync with remote repository
