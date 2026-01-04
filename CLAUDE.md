# CLAUDE.md

This file provides guidance to Claude Code when working with code in this repository.

## Project Overview

This is a static single-page website for the children's picture book "I Carried You in my Heart" by Dr. Rori Martello. The book is a lyrical celebration of adoption, featuring beautiful illustrations and storytelling for adoptive families.

**Live Site:** https://www.rorimartello.com
**GitHub Pages URL:** https://mjamiv.github.io/rorimartello/

## Tech Stack

- **HTML5** - Single-page structure with semantic markup
- **Tailwind CSS** - Utility-first CSS framework (loaded via CDN from browser bundle)
- **Vanilla JavaScript** - For interactive features (theme toggle, mobile menu, scroll effects)
- **Custom CSS** - Extensive custom styling with CSS variables for theming
- **Google Fonts** - Nunito (body text) and Special Elite (headlines)

## File Structure

```
rorimartello/
├── index.html              # Main landing page (all HTML, CSS, and JS)
├── book_cover.png          # Book cover image
├── CNAME                   # Custom domain configuration
├── README.md              # Basic repository information
└── IMG/                   # Image assets
    ├── 1_purplecard.png   # Watercolor card images
    ├── 2_bluecard.png
    ├── 3_greencard.png
    ├── 4_yellowcard.png
    ├── 5_redcard.png
    ├── headshot.PNG       # Author photo
    └── whythisbook_background.png
```

## Architecture

### Single-File Structure
All code is contained in `index.html`:
- Lines 1-2054: Styles and scripts (embedded in `<head>` and `<style>` tags)
- Lines 2055+: HTML content and structure

### Page Sections
The website consists of these main sections (in order):
1. **Hero** (`#hero`) - Book introduction with cover image
2. **About** (`#about`) - Book description and key features
3. **Why This Book** (`#why`) - Benefits and target audience
4. **Reviews** (`#reviews`) - Testimonials and ratings
5. **Author** (`#author`) - Dr. Rori Martello biography
6. **Details** (`#details`) - Book specifications and purchase options
7. **Educators** (`#educators`) - Resources for teachers and librarians
8. **Contact** (`#contact`) - Contact form and information

## Design System

### Color Palette
The site uses a warm, watercolor-inspired palette with CSS custom properties:

**Watercolor Colors:**
- Orange: `#FBC7C0` (`--wc-orange`)
- Yellow: `#FEF0CD` (`--wc-yellow`)
- Green: `#D9ECC8` (`--wc-green`)
- Blue: `#C8E2EF` (`--wc-blue`)
- Purple: `#DDD0E8` (`--wc-purple`)
- Pink: `#F3D9E9` (`--wc-pink`)

**Theme Colors:**
- Primary accent: `#D4887D`
- Backgrounds: White, off-white variations
- Text: Dark brown tones (`#2D1B17`, `#4A322C`)

### Typography
- **Headlines:** 'Special Elite' (monospace, typewriter-style)
- **Body:** 'Nunito' (rounded, friendly sans-serif)
- Responsive font sizing using `clamp()`

### Dark Mode
Full dark mode support via `[data-theme="dark"]` attribute. Theme preference is stored in localStorage and applied on page load.

## Key Features

### Interactive Elements
1. **Fixed Navigation Bar**
   - Transparent blur effect
   - Shrinks on scroll
   - Active link highlighting
   - Mobile hamburger menu

2. **Theme Toggle**
   - Sun/moon icon
   - Persists preference to localStorage
   - Smooth transitions between themes

3. **Scroll Progress Bar**
   - Fixed at top of viewport
   - Rainbow gradient indicator

4. **Loading Screen**
   - Animated heart on page load
   - Fades out when content is ready

5. **Responsive Design**
   - Mobile-first approach
   - Breakpoints at 900px, 768px, 640px, 480px
   - Touch-friendly mobile menu

## Development Workflow

### Making Changes

**To modify content:**
- Edit `index.html` directly
- Content sections are clearly marked with comments
- Use semantic HTML and maintain accessibility attributes

**To update styles:**
- Modify CSS custom properties in `:root` for theme changes
- Follow existing naming conventions
- Test both light and dark modes
- Ensure responsive behavior at all breakpoints

**To add images:**
- Place in `IMG/` directory
- Use descriptive filenames
- Update `index.html` references
- Optimize images before committing (keep file sizes reasonable)

### Testing

Since this is a static site, testing is straightforward:
1. Open `index.html` in a browser
2. Test responsive breakpoints using browser dev tools
3. Verify dark mode toggle functionality
4. Test mobile menu on smaller viewports
5. Check all anchor links navigate correctly
6. Ensure images load properly
7. Test on multiple browsers (Chrome, Firefox, Safari)

### No Build Process
This project has no build step or dependencies to install. Changes to `index.html` are immediately reflected when the file is loaded in a browser.

## Deployment

### GitHub Pages
The site is automatically deployed via GitHub Pages:
- Branch: `main`
- Source: root directory
- Custom domain configured via `CNAME` file

### Publishing Changes
1. Make edits to `index.html` or assets
2. Commit changes to the repository
3. Push to `main` branch
4. GitHub Pages will automatically deploy (usually within 1-2 minutes)
5. Verify changes at https://www.rorimartello.com

## Important Conventions

### Code Style
- **Indentation:** 4 spaces (in HTML sections)
- **CSS:** Use CSS custom properties for themeable values
- **JavaScript:** Embedded in `<script>` tags at end of `<body>`
- **Comments:** Use HTML comments to mark section boundaries

### Accessibility
- Maintain semantic HTML structure
- Include `alt` text for all images
- Ensure proper heading hierarchy (h1 → h2 → h3)
- Keep color contrast ratios WCAG AA compliant
- Support keyboard navigation

### Performance
- Lazy load images where appropriate
- Minimize layout shifts during load
- Use CDN for external resources (fonts, Tailwind)
- Optimize images before committing

## Common Tasks

### Update Book Information
Edit the relevant section in `index.html`:
- Book description: `#about` section
- Purchase links: `#details` section
- Reviews: `#reviews` section

### Add New Review
1. Locate the reviews section (`#reviews`)
2. Duplicate an existing review card structure
3. Update content, star rating, and reviewer info
4. Maintain consistent styling

### Modify Color Scheme
1. Update CSS custom properties in `:root`
2. Update dark mode properties in `[data-theme="dark"]`
3. Test all sections for visual consistency
4. Verify text contrast ratios

### Update Author Information
1. Edit the `#author` section
2. Update headshot image if needed (in `IMG/` directory)
3. Modify bio text and credentials

## Browser Support

Target browsers:
- Chrome/Edge (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)
- iOS Safari (last 2 versions)
- Chrome Android (last 2 versions)

## Contact & Support

For questions about the book or website content, use the contact form at `#contact` section or reach out through the provided contact methods on the live site.
