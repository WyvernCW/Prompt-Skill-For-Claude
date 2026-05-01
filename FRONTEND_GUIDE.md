# Frontend Design Guide: No AI Slop

## The Problem
AI-generated frontend defaults to safe, generic, forgettable design:
- Inter font + purple gradient + white background
- Centered card + hero section + 3 features + footer
- Fade-in on scroll + hover lift + generic shadows
- No conceptual reason for any choice

## The Solution
Every frontend prompt must enforce DISTINCTIVE, INTENTIONAL, MEMORABLE design.

---

## Typography Rules

### NEVER Use
- Inter
- Roboto
- Arial
- Helvetica
- System fonts
- Space Grotesk
- Any font that ships with a framework by default

### ALWAYS Use
- Distinctive display fonts: Playfair Display, Cormorant Garamond, Fraunces, Clash Display, Cabinet Grotesk, General Sans
- Refined body fonts: Source Serif 4, Crimson Text, Literata, Newsreader, ET Book
- Characterful monospace: JetBrains Mono, Berkeley Mono, Cartograph CF, Dank Mono
- Unexpected pairings: Serif display + Sans body, or vice versa
- Variable fonts for weight/width animation

### Selection Criteria
- Font must have personality
- Font must match the aesthetic direction
- Font must not appear in top 100 Google Fonts
- Font must feel chosen, not defaulted

---

## Color Rules

### NEVER Use
- Purple gradient on white background
- Generic dark mode (pure black #000 + pure white #fff)
- Blue primary + gray secondary + green success + red error
- Gradients without conceptual reason
- Colors that look like every other SaaS dashboard

### ALWAYS Use
- Dominant color + sharp accent (70/20/10 rule)
- Colors with semantic meaning tied to the brand/context
- CSS custom properties for consistency
- Subtle variations (tints, shades, tones) rather than new hues
- Background colors with texture/depth

### Examples
- Coffee brand: Espresso #1a1208, Amber #d4a574, Cream #f5f0e8
- Cyberpunk: Void #050505, Neon Cyan #00f0ff, Acid Magenta #ff00a0
- Luxury: Onyx #0f0f0f, Champagne #f7e7ce, Deep Burgundy #800020
- Organic: Moss #3d5a3d, Clay #c67c5c, Parchment #f4ecd8

---

## Motion Rules

### NEVER Use
- Generic fade-in on scroll (IntersectionObserver default)
- Hover lift with box-shadow
- Loading spinner without brand treatment
- Parallax without depth layering
- Animation that does not serve a purpose

### ALWAYS Use
- CSS-first animations (transform, opacity) for 60fps
- Staggered reveals with animation-delay orchestration
- Scroll-triggered effects with scrubbing
- Micro-interactions that surprise (magnetic buttons, morphing icons)
- Physics-based motion (spring, damping, mass)
- One high-impact page load sequence vs scattered micro-interactions

### Motion Libraries (React)
- Framer Motion for component animation
- GSAP for complex timelines
- Lenis for smooth scroll
- React Spring for physics

---

## Spatial Rules

### NEVER Use
- Centered card on white background
- Hero + features + footer pattern
- Even margins, predictable rhythm
- Symmetrical layouts without tension
- Grid that looks like Bootstrap

### ALWAYS Use
- Asymmetry with intentional imbalance
- Overlapping elements (text over image, image over card)
- Diagonal flow or broken grid
- Generous negative space OR controlled density (not both timidly)
- Elements that bleed to viewport edge
- Z-depth layering (parallax, sticky sections, floating elements)

---

## Background Rules

### NEVER Use
- Solid flat color
- Generic gradient (especially purple/blue)
- Default white or light gray
- No background treatment

### ALWAYS Use
- Subtle textures (grain, noise, paper, fabric)
- Gradient meshes with multiple color stops
- Geometric patterns (low opacity)
- Layered transparencies
- Dramatic shadows (not generic box-shadow)
- Custom cursors
- Ambient effects (particles, floating elements, subtle motion)

### Techniques
- CSS noise overlay: `background-image: url("data:image/svg+xml,...")`
- Gradient mesh: multiple radial gradients layered
- Pattern: SVG pattern at 5-10% opacity
- Shadow: colored, layered, directional shadows

---

## Component Rules

### NEVER Use
- Rounded-lg cards with shadow-md
- Generic button (rounded, gradient, hover lift)
- Default form inputs
- Standard toggle switch
- Cookie-cutter navigation

### ALWAYS Use
- Custom-shaped buttons (pill, organic, sharp angles)
- Inputs with character (underline only, floating labels, custom focus)
- Navigation that breaks convention (sidebar, floating, hidden, gesture-based)
- Cards with unique treatments (notched corners, angled edges, glassmorphism with purpose)
- Custom cursors
- Decorative borders (not just 1px solid)

---

## AI Slop Detection Checklist

Before finalizing any frontend prompt, verify ZERO of these appear:
- [ ] Font = Inter, Roboto, Arial, system-ui, Space Grotesk
- [ ] Background = white/light gray with purple/blue gradient accent
- [ ] Layout = centered card, hero section, 3-column features, footer
- [ ] Animation = generic fade-in on scroll, hover lift shadow
- [ ] Icons = generic Lucide/FontAwesome without stylistic treatment
- [ ] Buttons = rounded-lg, gradient background, generic hover
- [ ] Spacing = even margins, predictable rhythm, no tension
- [ ] Theme = generic dark mode toggle with no conceptual reason
- [ ] Components = look like they came from a UI kit
- [ ] Overall = could be any SaaS from 2020-2024

If any checked, REJECT and redesign.

---

## Complexity Matching

| Aesthetic | Code Complexity | Key Focus |
|---|---|---|
| Brutal minimal | Medium | Precision spacing, typography, single accent color |
| Maximalist chaos | Very high | Extensive animations, layered effects, controlled noise |
| Retro-futuristic | High | CRT effects, scanlines, pixel fonts, analog UI |
| Organic/natural | Medium | SVG animations, flowing shapes, earth tones |
| Luxury/refined | Medium | Subtle animations, premium materials, restrained palette |
| Playful/toy-like | High | Physics-based motion, bright colors, unexpected interactions |
| Editorial/magazine | Medium | Typography hierarchy, asymmetric grids, dramatic imagery |
| Cyberpunk | Very high | Neon glows, glitch effects, HUD elements, grid overlays |

---

## Remember
Claude is capable of extraordinary creative work. Don't hold back. Show what can truly be created when thinking outside the box and committing fully to a distinctive vision. Every design should feel like it could only exist for THIS specific context. No two prompts should produce the same aesthetic.
