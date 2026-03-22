# Design System — A to A dollar coffee

## Product Context
- **What this is:** A2A is an experimental framework for machine-to-machine value transfer through the HTTP 402 Payment Required protocol
- **Who it's for:** Developers, researchers, and engineers interested in autonomous agent economies, cryptography, and decentralized protocols
- **Space/industry:** Blockchain/Web3 research, agent AI, payment protocols, experimental systems
- **Project type:** Research landing page (marketing site for an experimental protocol/research project)

---

## Aesthetic Direction

**Direction:** *Elegant Monospace*

**Decoration level:** Intentional (subtle, refined, never gratuitous)

**Mood:** 
Research-grade, not startup-grade. Precise, technical, credible. Like reading a white paper that looks beautiful. Geek credibility without sacrificing elegance. Warm, confident, differentiated from the purple-blue convergence in crypto.

**Reference:** GitHub (dark mode), Stripe (typography hierarchy), research papers (whitespace), Basis/Optimism (DeFi refinement)

---

## Typography

### Display/Hero Fonts
**Primary: Space Mono (Bold)**
- Role: Headlines, section titles, data labels, strategic statements
- Why: Geometric monospace conveys precision and technical authority. Unusual in its boldness—most geek projects use thin monospace. Bold monospace signals confidence.
- Usage: `<h1>`, `<h2>`, `<h3>`, `.logo`, `.section-title`, data tables (`<thead>`)
- Loading: Google Fonts `family=Space+Mono:wght@700`
- Font scale: 2.5rem (h1) → 1.8rem (h2) → 1.2rem (h3)
- Letter-spacing: -0.02em (headings tighter), 0.05em (labels, upcase)
- Line-height: 1.2 (headings compact), 1.8 (data dense)

### Body/Long-form Fonts
**Primary: Lora (Regular + Italic)**
- Role: Body text, paragraphs, explanatory copy, long-form content
- Why: Serif elegance softens technical rigor. Warm serif + cold mono = tension that feels intentional. Serif readability at 16px is superior to sans. Italic elegantly highlights asides and quotes.
- Usage: `<p>`, `.subtitle`, narrative sections, quotes
- Loading: Google Fonts `family=Lora:ital,wght@0,400;0,600;1,400`
- Font weights: 400 (standard) and 600 (emphasis in body)
- Font scale: 1.1rem (large), 1rem (standard), 0.9rem (secondary)
- Line-height: 1.8 (body), 1.6 (secondary), 1.5 (data)

### UI/Labels/Code Fonts
**Primary: JetBrains Mono (Regular + SemiBold)**
- Role: Button labels, form inputs, labels, UI text, code snippets, inline monospace, small data
- Why: Modern code font optimized for readability at small sizes. Slightly warmer than other tech monos. Professional appearance.
- Usage: `.btn`, `.label`, `<code>`, grid labels, inline monospace, tables
- Loading: Google Fonts `family=JetBrains+Mono:wght@400;600`
- Font weights: 400 (standard), 600 (bold, emphasis)
- Font scale: 0.9rem (standard), 0.85rem (labels), 0.8rem (small)
- Letter-spacing: 0.05em (labels, uppercase)

### Font Pairing Strategy
- **Hierarchy creates anticipation:** Bold mono gives you power. Serif lets you breathe. Mono in UI feels efficient.
- **Cognitive load:** Three fonts might seem like a lot, but they occupy different visual zones:
  - Mono = scan quickly (headlines, labels, data)
  - Serif = read slowly (prose, explanations)
  - Mono (small) = interface scaffolding (forms, buttons)
- **The discord is intentional:** Most design systems use interchangeable fonts (all sans, or all serif). You're using deliberate contrast. It says "we thought about this."

---

## Color Palette

### Approach
**Balanced-Expressive:** Primary + secondary + semantic. Gold accent is the hero; it's rare in crypto/DeFi (which converges on purple, blue, green). Gold signals scarcity and precision. Not warm like amber, not cold like bronze—a refined mid-tone that works in both light and dark.

### Core Palette

#### Dark Mode (Primary)
```
Primary dark:    #0a0e14  (warm black—softer than GitHub's #0d1117)
Secondary dark:  #151b24  (raised surface)
Tertiary dark:   #1f2937  (higher surface for hover/active)
Text primary:    #e5e9f0  (warm off-white, not pure #fff)
Text secondary:  #a8b5c7  (warm gray for secondary text)
Border:          #2d3748  (subtle, warm gray)
Accent:          #d4a574  (warm gold—the hero)
Accent hover:    #e8c4a0  (slightly lighter for hover states)
```

#### Light Mode (Secondary)
```
Primary light:   #fafbfc  (off-white, not pure white)
Secondary light: #f0f3f9  (warm gray surface)
Tertiary light:  #e6ecf5  (slightly darker hover)
Text primary:    #1a1f2e  (near-black, warm)
Text secondary:  #5a6b7a  (warm medium gray)
Border:          #d1dce6  (light warm gray)
Accent:          #d4a574  (same gold, works in both modes)
```

#### Semantic Colors
```
Success:  #10b981  (emerald, active/confirmed)
Warning:  #f59e0b  (amber, caution/attention)
Error:    #f87171  (red, failure/destructive)
Info:     #3b82f6  (blue, informational)
```

### Color Psychology in This Context
- **#0a0e14 (Primary dark):** Warmer than GitHub's pure black. Less harsh on the eye at night. Adds personality.
- **#d4a574 (Gold accent):** Rare in crypto. Most projects use purple (#58a6ff), blue (#3b82f6), or neon green. Gold = precision, scarcity, value. Differentiates A2A from the crowd.
- **Warm grays (#a8b5c7, #5a6b7a):** Not cool grays. Warm grays echo the gold accent subtly. Cohesive.
- **Semantic colors:** Conservative, proven. Green (success/go), amber (caution), red (error), blue (info). No surprises.

### Usage Guidelines
- **Text:** Always `--text-primary` for body, `--text-secondary` for labels/captions
- **Backgrounds:** Dark mode = `--bg-primary` → `--bg-secondary` → `--bg-tertiary` (hierarchy)
- **Accent:** Gold for CTAs, highlights, "look here" moments. Sparingly.
- **Semantic:** Use for status, validation, output. Never decorative.
- **Borders:** Always `--border`. Never black (#000) or pure white (#fff).
- **Hover/Active:** Darken in dark mode, lighten in light mode. Use `--accent-hover` for accent buttons.

---

## Spacing

### Base Unit
**8px**

All spacing derives from 8px. This is comfortable for digital UI without feeling squeaky.

### Spacing Scale
```
2xs:   2px  (hairlines, minimal gaps)
xs:    4px  (tight spacing)
sm:    8px  (standard spacing, base unit)
md:   16px  (comfortable spacing)
lg:   24px  (generous spacing)
xl:   32px  (large, breathing room)
2xl:  48px  (section separator)
3xl:  64px  (major section gap)
```

### Density
**Comfortable:** Not packed, not loose. Geek projects often go too tight. Not here. Whitespace is part of the design.

### Application
- **Padding within cards/boxes:** md (16px)
- **Margin between sections:** 2xl → 3xl (48-64px)
- **Line-height body:** 1.8 (relaxed reading)
- **Line-height headings:** 1.2 (compact drama)
- **Gap in grids:** lg → xl (24-32px)
- **Button padding:** sm md (8px 16px)
- **Form input padding:** md (16px)

---

## Layout

### Approach
**Editorial/Asymmetric Hybrid**

Not strict grid. Not freeform chaos. Editorial (like a magazine) with deliberate asymmetry. Grids are boring when applied with zero variation. Use a 12-column grid on desktop, but break it strategically. The geek projects that feel timeless (Stripe, GitHub, Cloudflare docs) have grid discipline *with* personality.

### Grid System
- **Desktop (1200px+):** 12 columns, 24px gap
- **Tablet (768px-1199px):** 8 columns, 20px gap
- **Mobile (<768px):** 4 columns, 16px gap
- **Max content width:** 1200px
- **Margins:** 2rem on desktop, 1.5rem on tablet, 1rem on mobile

### Border Radius
**Subtle, sharp, geek:**
```
sm:    2px   (form inputs, small interactive elements)
md:    4px   (cards, buttons, default)
lg:    6px   (larger cards, hero sections)
full: 9999px (only for pills/badges)
```

Not rounded. Not circular. Just enough curve to feel modern, not soft. This preserves the minimal, sharp aesthetic.

### Breathing Room
- Hero section: 4rem top padding, 3rem bottom
- Section margins: 2xl between sections (48px)
- Container max-width: 1200px, centered with auto margins
- Never let text touch the viewport edge: always 2rem+ padding

---

## Motion & Interaction

### Approach
**Minimal-Functional**

No decorative animation. Every motion must aid comprehension.

### Timing
- **Micro transitions:** 50-100ms (hover states, quick feedback)
- **Short transitions:** 150-250ms (button clicks, state changes)
- **Medium transitions:** 250-400ms (page transitions, modal enters)
- **Long animations:** 400-700ms (only for product onboarding, not UI chrome)

### Easing
- **Enter animation:** `ease-out` (fast start, slow end—feels natural)
- **Exit animation:** `ease-in` (slow start, fast end—feels decisive)
- **Move**: `ease-in-out` (balanced, used for hovers, state changes)

### Specific Interactions
- **Button hover:** `transform: translateY(-2px)` + `background-color` change. 150ms ease-out.
- **Form input focus:** `border-color` → accent + subtle `box-shadow`. 100ms ease-out.
- **Card hover on desktop:** slight elevation + border color change, no scale (feels lighter and more refined).
- **Disabled state:** `opacity: 0.5` + `cursor: not-allowed`. No animation.

### Anti-patterns
- No fade-in on page load (feels slow)
- No spinning loaders (use progress bars instead)
- No parallax scrolling (geek projects avoid this)
- No micro-interactions on non-interactive elements
- No gradient animations (feels cheap)

---

## Component Library (Semantic)

### Buttons
```
Primary:   gold (#d4a574) background, dark text, border same as background
Secondary: transparent background, gold text, gold border
Ghost:     transparent, secondary text, secondary border
Disabled:  opacity 0.5, cursor not-allowed

Padding: md lg (16px 24px)
Border-radius: md (4px)
Font: JetBrains Mono 600
Transition: all 150ms ease-out
Hover: translateY(-2px) for primary, lighter background for secondary/ghost
```

### Form Inputs
```
Background: --bg-tertiary
Border: --border, 1px
Text: --text-primary
Label: JetBrains Mono 600, uppercase, --text-secondary
Padding: md (16px)
Border-radius: md (4px)
Focus: border-color → accent, box-shadow 0 0 0 2px rgba(accent, 0.1)
Font: Lora 400 (body-like, not monospace)
```

### Cards / Containers
```
Background: --bg-secondary
Border: 1px --border
Border-radius: md-lg (4-6px)
Padding: 2rem
Hover (desktop): bg → --bg-tertiary, border → accent, translateY(-4px), subtle shadow
```

### Alerts / Status
```
Success: bg rgba(success, 0.1), border-left 4px success, text success
Warning: bg rgba(warning, 0.1), border-left 4px warning, text warning
Error:   bg rgba(error, 0.1), border-left 4px error, text error
Info:    bg rgba(info, 0.1), border-left 4px info, text info
Font: JetBrains Mono or Lora 400
Padding: md (16px)
Border-radius: sm (2px)
```

### Data Tables
```
Header background: --bg-tertiary
Header text: --text-secondary, uppercase, Space Mono 700
Body font: JetBrains Mono 400
Row borders: 1px --border
Row hover: background → --bg-secondary
Padding: sm md (8px 16px)
Alignment: left for text, right for numbers
```

---

## Design Decisions Log

| Date | Decision | Rationale |
|------|----------|-----------|
| 2024-03-22 | Warm dark (#0a0e14) instead of pure black | Soften GitHub-standard black, add personality. Still high contrast. |
| 2024-03-22 | Gold (#d4a574) instead of blue/purple accent | Differentiate from crypto's color consensus. Gold = scarcity, precision, value. |
| 2024-03-22 | Serif + mono hybrid (Lora + Space Mono + JetBrains) | Discord is intentional. Mono for scan, serif for read, mono for UI. Works together. |
| 2024-03-22 | Minimal-functional motion only | Geek projects don't need dancing UI. Motion aids comprehension, not decoration. |
| 2024-03-22 | Sharp but subtle border radius (2-6px, no circles) | Preserve minimal aesthetic without harshness. Modern, not soft. |
| 2024-03-22 | Comfortable spacing (8px base), not compressed | Whitespace is design. Readability > density. |
| 2024-03-22 | Editorial grid with asymmetry | Grid discipline + personality. Boring grids feel generic. |

---

## Implementation Notes

### CSS Variables (always use, never hardcode colors)
```css
:root {
    --bg-primary: #0a0e14;
    --bg-secondary: #151b24;
    --bg-tertiary: #1f2937;
    --text-primary: #e5e9f0;
    --text-secondary: #a8b5c7;
    --accent: #d4a574;
    --accent-hover: #e8c4a0;
    --border: #2d3748;
    --success: #10b981;
    --warning: #f59e0b;
    --error: #f87171;
    --info: #3b82f6;
}

/* Light mode override */
body.light-mode {
    --bg-primary: #fafbfc;
    --bg-secondary: #f0f3f9;
    --text-primary: #1a1f2e;
    --text-secondary: #5a6b7a;
    --border: #d1dce6;
}
```

### Font Loading
```html
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Lora:ital,wght@0,400;0,600;1,400&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
```

### System Font Stack (if Google Fonts unavailable)
```css
/* Display */
font-family: 'Space Mono', 'Courier New', monospace;

/* Body */
font-family: 'Lora', Georgia, serif;

/* UI/Code */
font-family: 'JetBrains Mono', 'SF Mono', Monaco, monospace;
```

### Dark/Light Mode
Use CSS `:prefers-color-scheme` + `@media (prefers-color-scheme: light)` for system preference detection. Offer explicit toggle button that overrides system preference.

---

## Accessibility Checklist

- ✅ Color contrast: All text meets WCAG AA (4.5:1 minimum). Gold accent is decorative primarily; verify semantic colors are sufficient contrast.
- ✅ Font sizes: 16px minimum for body, 14px for secondary text.
- ✅ Line-height: 1.8 for body, 1.5 for data. Never less than 1.4.
- ✅ Focus states: Always visible. Gold border + subtle shadow for inputs.
- ✅ Motion: Respects `prefers-reduced-motion`. If set, animations reduce to 0ms (instant state change).
- ✅ Semantic HTML: Use `<button>` not `<div>` for buttons, `<header>` for nav, `<main>` for content.

---

## Usage Rules (MUSTS)

1. **All colors must be CSS variables.** Never hardcode hex values. `-—bg-primary`, not `#0a0e14`.
2. **Spacing must use the scale.** 8px multiples. Never arbitrary spacing like `11px`.
3. **Fonts must be one of the three.** No Random Sans, no System UI. Space Mono, Lora, or JetBrains Mono.
4. **Motion is intentional, never decorative.** No spinning icons, no fade-ins on load, no parallax.
5. **Never invent new border-radius values.** Use: 2px, 4px, 6px, or 9999px only.
6. **Button hover states are required.** At minimum, `transform: translateY(-2px)` or background change.
7. **All interactive elements must have focus states.** Visible, gold-colored, never removed.
8. **Light mode is a first-class citizen.** Not an afterthought. `@media (prefers-color-scheme: light)` applies to all components.

---

## Future Considerations

- **Icons:** If needed, use Feather Icons (simple, monospace-compatible) or custom SVG with 2px stroke weight.
- **Illustrations:** Minimize. Use diagrams, charts, and simple forms. No stock photos or AI-generated imagery.
- **Animations:** Consider Framer Motion for complex state transitions, but keep the philosophy: minimal-functional.
- **Dark/Light Mode:** Start with dark mode as primary. Light mode is a CSS override using `prefers-color-scheme` and explicit toggle.
- **Responsive Tables:** On mobile, consider stacking as cards or horizontal scroll within a container (preserve monospace data readability).

---

## References

- **Space Mono fonts:** https://github.com/adobe-fonts/space-mono
- **Lora font:** https://fonts.google.com/specimen/Lora
- **JetBrains Mono:** https://fonts.google.com/specimen/JetBrains+Mono
- **WCAG Contrast:** https://webaim.org/articles/contrast/
- **CSS Variables:** https://developer.mozilla.org/en-US/docs/Web/CSS/--*
- **Design Inspiration:** Stripe (typography), Cloudflare (layout), GitHub (dark mode), Anthropic (geek + elegant)

---

**DESIGN.md Created:** March 22, 2024  
**System Name:** Elegant Monospace — Refined Geek Aesthetic  
**Last Updated:** March 22, 2024  
**Status:** Ready for Development
