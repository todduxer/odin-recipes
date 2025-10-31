# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is a static HTML website project for The Odin Project curriculum, showcasing basic recipe pages. The site consists of a main index page linking to individual recipe pages with ingredients and step-by-step instructions.

## Project Structure

```
odin-recipes/
├── index.html          # Main landing page with recipe links
├── images/             # Recipe images (fries.png, pbj.jpeg, swedishmeatball.jpeg)
├── recipes/            # Individual recipe HTML pages
│   ├── frenchfries.html
│   ├── pbj.html
│   └── swedishmeatballs.html
└── readme.md           # Project documentation
```

## Development Commands

### Version Control
- **View changes**: `git --no-pager diff`
- **Stage changes**: `git add .`
- **Commit changes**: `git commit -m "your message"`
- **Push to GitHub**: `git push origin main`
- **Check status**: `git status`

### Local Development
- **Open site locally**: `open index.html` (macOS)
- **Start local server**: `python3 -m http.server 8000` then navigate to http://localhost:8000

### HTML Validation
- **Validate HTML**: Use W3C validator at https://validator.w3.org/ or install a local validator

## Code Architecture

### HTML Structure Pattern
Each recipe page follows this consistent structure:
1. DOCTYPE and HTML setup with proper meta tags
2. Page title in `<head>`
3. Main heading (`<h1>`) matching the recipe name
4. Home navigation link back to index.html
5. Ingredients section with unordered list
6. Steps section with ordered list

### Navigation
- All recipe pages link back to index using relative paths (`../index.html`)
- Index page links to recipes using relative paths (`recipes/[name].html`)

### Image Management
- Images stored in `/images/` directory
- Referenced from index.html using relative paths
- Named to match recipe files (e.g., `fries.png` for `frenchfries.html`)

## Common Tasks

### Adding a New Recipe
1. Create new HTML file in `recipes/` directory
2. Follow the existing HTML structure pattern from other recipes
3. Add corresponding image to `images/` directory
4. Update `index.html` to include link and image for new recipe

### Fixing HTML Structure Issues
- Recipe pages have `</body>` tag placement issues - body content should be inside `<body>` tags
- Consider adding CSS stylesheet for consistent styling across pages
- Images on index page should be wrapped with or placed adjacent to their corresponding links

## GitHub Repository
- **Remote**: https://github.com/todduxer/odin-recipes.git
- **Branch**: main (default)