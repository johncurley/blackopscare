# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo-based static website for Black Ops Support Services, an aged care and support services company. The site is deployed on Netlify and uses a modern, responsive design without any external themes.

## Development Commands

### Local Development
```bash
npm run dev          # Start Hugo development server with drafts
hugo server -D       # Alternative command (same as above)
```

### Production Build
```bash
npm run build        # Build optimized production site
hugo --gc --minify   # Alternative command (same as above)
```

### Preview Production Build
```bash
npm run preview      # Run server with production environment
```

### Manual Hugo Commands
```bash
hugo new site . --force                    # Initialize Hugo site structure
hugo server --environment production       # Production preview server
hugo --gc --minify --buildFuture          # Build with future content
```

## Architecture

### Site Structure
- **Hugo Configuration**: `hugo.yaml` - Main site configuration with params, menu, and markup settings
- **Netlify Config**: `netlify.toml` - Deployment settings, build commands, and security headers
- **Content**: `content/_index.md` - Homepage markdown content
- **Templates**: 
  - `layouts/index.html` - Homepage template with all sections
  - `layouts/_default/baseof.html` - Base template with common HTML structure
- **Styles**: `assets/css/main.css` - Single CSS file with modern styling using CSS Grid and Flexbox
- **Generated**: `public/` - Hugo-generated static files (not tracked in git)

### Template Architecture
The site uses a single-page design with all content sections in the homepage template:
- Hero section with company branding
- Services grid (6 main service categories)
- About section with company values
- Reviews/testimonials section
- Contact form with Netlify integration

### CSS Architecture
- CSS Custom Properties (variables) for theming
- Mobile-first responsive design
- Modern layout techniques (CSS Grid, Flexbox)
- Component-based styling approach
- No external CSS frameworks or dependencies

## Key Configuration

### Site Parameters (hugo.yaml)
```yaml
params:
  phone: '0498 052 843'
  email: 'info@blackopssupportservices.com.au'
```

### Hugo Version Requirements
- Hugo Extended v0.121.0 or later (specified in netlify.toml and package.json)
- Node.js v16.0.0 or later

### Deployment
- Primary deployment: Netlify (automated from git)
- Build command: `hugo --gc --minify`
- Publish directory: `public`
- Security headers configured in netlify.toml
- Caching policies for static assets (CSS, JS, images)

## Development Notes

### Content Management
- Homepage content is in markdown format (`content/_index.md`)
- Site configuration and parameters in `hugo.yaml`
- No CMS integration - content edited directly in files

### Form Handling
- Contact form uses Netlify Forms (serverless form processing)
- Form submissions appear in Netlify dashboard
- No additional backend required

### Performance Optimizations
- Asset minification via Hugo pipes
- Aggressive caching headers for static assets
- Optimized CSS with minimal dependencies
- Single-page application approach reduces navigation overhead

### Customization Areas
- Colors and branding: CSS custom properties in `assets/css/main.css`
- Contact information: `hugo.yaml` params section
- Services: Currently hardcoded in template, could be moved to data files
- Reviews: Static in template, could be made dynamic with data files