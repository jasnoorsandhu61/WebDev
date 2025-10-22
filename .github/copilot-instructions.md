# Copilot Instructions - Wheel of Misfortune Slot Machine
(JAVASCript is not allowed in this project)
## Project Overview
This is an HTML-based slot machine game called "Wheel of Misfortune" built as a team project. The application consists of two main pages: an introduction/landing page and the main game interface.

## Architecture & File Structure

### Key Files
- `introduction.html` - Landing page with game info, team details, and navigation
- `index.html` - Main game page (currently minimal, awaiting slot machine implementation)
- `style.css` - Empty global styles file (styles are currently inline)
- `src/` - Assets directory containing game images and backgrounds

### Navigation Pattern
The project uses simple client-side navigation via `document.location` redirects:
```javascript
onclick="document.location='index.html'"
```

## Styling Conventions

### CSS Organization
- **Inline styles preferred**: All styles in `introduction.html` are embedded in `<style>` tags
- **Empty global CSS**: `style.css` exists but is unused (linked as `styles.css` in `index.html`)
- **Viewport units**: Uses modern `100dvw`/`100dvh` for full viewport coverage

### Animation Patterns
Animations use composition for multiple simultaneous effects:
```css
.move {
    animation: move 5s infinite ease-in-out, rotate 3s infinite ease-in-out;
    animation-composition: add;
}
```

### Interactive Elements
- **Button styling**: Semi-transparent backgrounds with hover transforms
- **Info panels**: Positioned absolutely with opacity-based visibility
- **Trigger pattern**: Uses CSS sibling selector for info display: `.info-btn:active ~ .info`

## Asset Management

### Image Resources
All images stored in `src/` directory with WebP format for optimization:
- `introBackground.webp` - Fullscreen background
- `slotMachineClipart.webp` - Animated game logo
- Slot-related images: `blankslot1.webp`, `blankslot2.webp`

### Asset Referencing
Use relative paths from HTML root: `src/imagename.webp`

## Development Notes

### Current State
- Introduction page is fully implemented with animations and info panels
- Main game page (`index.html`) is a shell awaiting slot machine functionality
- CSS file structure suggests intended separation but currently uses inline styles

### Team Context
Project by Max, Matthew, and Jasnoor - consider this collaborative context when making changes.

## Implementation Patterns

### Layout Strategy
- **Flexbox-centric**: Heavy use of flexbox for centering and layout
- **Full viewport**: Uses viewport units and `overflow: hidden` for immersive experience
- **Component-based**: Logical grouping with `.window`, `.title`, `.content` structure

### When Adding Features
- Follow the inline CSS pattern established in `introduction.html`
- Use the existing button styling conventions for consistency
- Maintain the fullscreen, immersive design approach
- Keep the semi-transparent overlay aesthetic for UI elements