# A to A dollar coffee — Development Guidelines

## Project Overview
A2A is an experimental framework for machine-to-machine value transfer through the HTTP 402 Payment Required protocol. The landing page showcases the vision, research, and opportunity in autonomous agent economies.

- **Repository:** https://github.com/dearkenny/a-to-a-dollar-coffee
- **Live Site:** https://dearkenny.github.io/a-to-a-dollar-coffee/
- **Tech Stack:** Static HTML, inlined CSS, no dependencies

## Design System
**READ DESIGN.md BEFORE ANY UI WORK**

All visual decisions must align with the **Elegant Monospace** design system:

### Color Palette
- **Primary dark:** `#0a0e14` (never pure black)
- **Accent:** `#d4a574` (warm gold, rare in crypto—use sparingly)
- **Text primary:** `#e5e9f0` (warm off-white)
- **Text secondary:** `#a8b5c7`
- **Borders:** `#2d3748`
- **Semantic:** Green #10b981, Amber #f59e0b, Red #f87171, Blue #3b82f6

### Typography
| Role | Font | Usage |
|------|------|-------|
| **Headlines** | Space Mono Bold (700) | `<h1>`, `<h2>`, `<h3>`, section titles, data labels |
| **Body** | Lora Regular (400/600) | Long-form text, paragraphs, explanations |
| **UI/Code** | JetBrains Mono (400/600) | Buttons, forms, labels, code snippets |

**Google Fonts Link:**
```html
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Lora:ital,wght@0,400;0,600;1,400&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
```

### Spacing
- **Base unit:** 8px (all spacing = 8px multiples)
- **Standard gaps:** sm(8px) md(16px) lg(24px) xl(32px)
- **Section margins:** 48px-64px between sections
- **Line heights:** Body 1.8, headings 1.2

### Motion
- **Hover states required** on all interactive elements
- Use `transform: translateY(-2px)` + color change for buttons
- Duration: 150ms, easing: `ease-out` (enter), `ease-in` (exit)
- **No decorative animations.** Motion aids comprehension only.

### Border Radius
- **sm:** 2px (inputs, badges)
- **md:** 4px (buttons, cards, default)
- **lg:** 6px (larger containers)
- **Never use arbitrary values** like 5px, 3px, 10px, etc.

## Code Standards

### CSS
- Use CSS custom properties (variables) for all colors
- Never hardcode hex values in the source
- No inline styles—keep styles in `<style>` tags or separate sheets
- Dark mode + Light mode support via `@media (prefers-color-scheme: light)` OR explicit `.light-mode` class

### HTML
- Always use semantic HTML: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`, `<button>` (not `<div>` with click handlers)
- Ensure focus states for all interactive elements
- Provide alt text for images
- Use proper heading hierarchy (no skipping h1 → h3)

### Accessibility
- Minimum text size: 16px (body), 14px (secondary)
- Contrast ratio: 4.5:1 (WCAG AA) minimum
- Focus states: visible, gold-colored border, never hidden
- Respect `prefers-reduced-motion`: reduce animations to instant if user has this set

## Common Tasks

### Adding a New Page
1. Create a new `.html` file
2. Import the fonts from Google Fonts (see Typography above)
3. Define CSS variables for the design system (see DESIGN.md)
4. Use only Space Mono / Lora / JetBrains Mono for all text
5. Use 8px multiples for all spacing
6. Add hover/focus states to all interactive elements
7. Test in both dark and light modes

### Updating Colors
1. **Always update the CSS variables in `:root`**
2. Check contrast with WebAIM's contrast checker
3. Ensure both dark and light mode variables are updated
4. Never hardcode colors—always use the variable name

### Adding Components
1. Use the dimensions defined in DESIGN.md (border-radius, padding, etc.)
2. Document the component in DESIGN.md under "Component Library"
3. Test hover/active/focus/disabled states
4. Ensure semantic HTML (buttons are `<button>`, not `<div class="btn">`)

### Responsive Design
- **Desktop (1200px+):** Full layout, multi-column grids
- **Tablet (768px-1199px):** 8-column grid, slightly smaller padding
- **Mobile (<768px):** Single column, 1rem padding, larger tap targets
- Use `max-width: 1200px` for content width

## Deployment

### GitHub Pages
- Deployed automatically from `main` branch root
- All changes to `index.html`, `README.md`, CSS, or assets are live within 1-2 minutes
- No build step required (static HTML only)

### Process
1. Make changes locally
2. Test in browser: `open index.html`
3. Commit with clear message: `git commit -m "Update: [change description]"`
4. Push to main: `git push origin main`
5. Changes are live at https://dearkenny.github.io/a-to-a-dollar-coffee/

## File Structure
```
a-to-a-dollar-coffee/
├── index.html              # Main landing page
├── DESIGN.md               # Design system (source of truth for all visual decisions)
├── CLAUDE.md               # This file (development guidelines)
├── README.md               # Project documentation
├── design-preview.html     # Preview page showing fonts, colors, components
└── .gitignore              # Git configuration
```

## QA Checklist Before Shipping

- [ ] All text aligns with Space Mono / Lora / JetBrains Mono fonts
- [ ] Colors use CSS variables (no hardcoded hex values)
- [ ] Spacing follows 8px multiples (checked against DESIGN.md)
- [ ] All buttons have hover states
- [ ] All form inputs have focus states (gold border + shadow)
- [ ] Tested in dark mode and light mode
- [ ] Mobile responsive (tested at 375px, 768px, 1200px widths)
- [ ] Contrast passes WCAG AA (4.5:1 for text, 3:1 for graphics)
- [ ] No animations on non-interactive elements
- [ ] All motion respects `prefers-reduced-motion`
- [ ] Semantic HTML used throughout (no divs as buttons)
- [ ] Links have visible focus states
- [ ] Page loads without errors in console
- [ ] GitHub Pages build succeeds (check commit status)

## Useful Links

- **Contrast Checker:** https://webaim.org/resources/contrastchecker/
- **Google Fonts:** https://fonts.google.com/
- **CSS Variables Guide:** https://developer.mozilla.org/en-US/docs/Web/CSS/--*
- **Responsive Design:** https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design
- **WCAG Guidelines:** https://www.w3.org/WAI/WCAG21/quickref/

## Contact & Support

- **GitHub Issues:** https://github.com/dearkenny/a-to-a-dollar-coffee/issues
- **Design Questions:** Refer to DESIGN.md or update it with new decisions
- **Deployment Issues:** Check GitHub Pages build status in repo Settings

---

**Last Updated:** March 22, 2024  
**Status:** Design system finalized. Ready for development.
