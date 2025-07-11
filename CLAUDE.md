# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML website for Block System, a creative studio specializing in audiovisual art, live performances, and installations. The site showcases various projects including VJing, art installations, and the BITCHBOY MIDI controller.

## Architecture

### Single-Page Application Structure
- **Main file**: `index.html` - Contains the complete website with embedded CSS and JavaScript
- **Architecture**: Single-page static site with no build process or package.json
- **Styling**: All CSS is embedded within `<style>` tags in the HTML head
- **JavaScript**: All functionality is contained in a single `<script>` tag at the bottom of the HTML

### Key Components
- **Video Banner**: Full-screen video background with overlay logo
- **Navigation**: Fixed header with smooth scrolling to sections
- **Visual Grid**: Responsive grid layout for showcasing projects
- **Popup System**: Interactive modal system for project details with carousel functionality
- **Collaborators Section**: Animated marquee displaying partner logos
- **Team Section**: Grid layout for team member profiles

### CSS Architecture
- **CSS Variables**: Defined in `:root` for consistent theming (primary, secondary, accent colors)
- **Responsive Design**: Mobile-first approach with media queries
- **Animation**: CSS animations for marquee scrolling and hover effects
- **Grid Layouts**: Extensive use of CSS Grid for responsive layouts

### JavaScript Functionality
- **Popup System**: Dynamic modal generation with carousel support
- **Image Carousel**: Multi-image slideshow with navigation controls
- **Event Handling**: Click, keyboard, and overlay interactions
- **Smooth Animations**: CSS transitions controlled via JavaScript classes

## Development Commands

Since this is a static HTML site, there are no build commands. Development is done by:
1. Direct editing of `index.html`
2. Preview changes by opening the file in a browser
3. Use live server extensions for hot reload during development

## Git Workflow

Based on `git commands.txt`, the workflow is:
```bash
# Check status
git status

# Stage all changes
git add .

# Commit with descriptive message
git commit -m "Your commit message"

# Push to remote
git push
```

## Asset Management

### Directory Structure
- `assets/images/` - All image assets organized by category:
  - `featured/` - Featured project images and GIFs
  - `live/` - Live performance and installation photos
  - `collaborators/` - Partner and collaborator logos
  - `team/` - Team member photos
  - `projects/` - Project-specific images
- `assets/videos/` - Video files (main banner video)

### Image Optimization
- Use appropriate formats (GIF for animations, PNG for logos, JPG for photos)
- Maintain consistent aspect ratios for grid layouts
- Consider file sizes for web performance

## Popup System Implementation

The site features a sophisticated popup system for project details:
- **Text Popups**: For project descriptions with optional images
- **Video Popups**: For video content with autoplay
- **Image Carousels**: Multi-image galleries with navigation
- **Keyboard Navigation**: Arrow keys and Escape key support

## Styling Guidelines

### Color Scheme
- Primary: `#1a1a1a` (dark background)
- Secondary: `#ffffff` (white text)
- Accent: `#ffea00` (yellow highlight)
- Accent Dark: `#b8b8b8` (muted gray)

### Typography
- Font family: 'Helvetica Neue', Arial, sans-serif
- Consistent letter-spacing and text-transform for headings
- Responsive font sizes with media queries

### Interactive Elements
- Hover effects on all clickable elements
- Smooth transitions using CSS `transition` property
- Transform effects for visual feedback

## Common Development Tasks

### Adding New Projects
1. Add images to appropriate `assets/images/` subdirectory
2. Create new `.visual-item` div in the relevant section
3. Add popup data attributes if interactive content needed
4. Update popup JavaScript if new functionality required

### Modifying Popup Content
- Use `data-popup-type`, `data-popup-title`, `data-popup-content` attributes
- For carousels: `data-popup-images` with comma-separated image paths
- For videos: `data-popup-video` with video file path

### Updating Collaborators
- Add new logos to `assets/images/collaborators/`
- Update the marquee section with new `<img>` tags
- Maintain the mirrored structure for seamless scrolling

## Performance Considerations

- Single HTML file keeps HTTP requests minimal
- CSS and JavaScript are inlined to reduce external dependencies
- Video files should be optimized for web delivery
- Images should be compressed while maintaining quality

## Browser Compatibility

- Modern CSS Grid and Flexbox usage
- CSS Custom Properties (variables) support required
- JavaScript ES6+ features used (arrow functions, const/let)
- Target: Modern browsers (Chrome, Firefox, Safari, Edge)