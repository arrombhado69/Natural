# Design Guidelines - Aura Natural Website

## Design Approach
**Reference-Based Approach** inspired by premium wellness brands (Aesop, Herbivore Botanicals) combined with your specific brand identity. Focus on organic elegance, soft animations, and natural beauty.

## Core Design Elements

### A. Color Palette
**Brand Colors (from provided assets):**
- Primary Turquoise: 174 48% 60% (headers, CTAs, accents)
- Secondary Purple: 270 36% 39% (text highlights, sections)
- Soft Aqua: 175 52% 75% (backgrounds, cards)
- Natural Beige: 110 67% 95% (sections, subtle backgrounds)
- Pure White: 0 0% 100% (main backgrounds, text)

**Usage:**
- Hero: Gradient from Beige to Soft Aqua
- Sections: Alternate between White and Beige backgrounds
- CTAs: Turquoise with Purple hover states
- Text: Purple for headings, dark gray (0 0% 20%) for body

### B. Typography
**Font Families:**
- Headings: 'Playfair Display' (serif, elegant)
- Body: 'Poppins' (sans-serif, clean, 300-400 weight)
- Accent: 'Dancing Script' (cursive, for taglines)

**Scales:**
- H1: text-5xl md:text-6xl lg:text-7xl (hero)
- H2: text-3xl md:text-4xl lg:text-5xl (sections)
- H3: text-2xl md:text-3xl (cards, team)
- Body: text-base md:text-lg
- Small: text-sm

### C. Layout System
**Spacing Primitives:** Tailwind units of 4, 8, 12, 16, 20, 24 (p-4, m-8, gap-12, py-16, etc.)

**Grid Structure:**
- Container: max-w-7xl mx-auto px-4 md:px-8
- Hero: Full viewport height with centered content
- Sections: py-16 md:py-24 lg:py-32
- Team Grid: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8

### D. Component Library

**Hero Section:**
- Full viewport animated background with floating floral SVG elements
- Centered logo with gentle scale-in animation
- Tagline with fade-up effect (delay 0.3s)
- CTA button with pulse animation

**About Section:**
- Two-column layout (text + decorative floral illustration)
- Fade-in on scroll trigger
- Soft divider with flower icon

**Products Gallery:**
- Masonry-style grid with hover lift effects
- Image overlay with gradient on hover
- Quick-view modal with smooth transitions

**Team Section ("Nossa Equipe"):**
- Card-based grid layout
- Profile photos with circular frames and subtle shadow
- Names in Playfair Display, roles in Poppins
- Stagger animation on scroll (0.1s delay between cards)
- Hover: gentle scale (1.05) + shadow increase

**Footer:**
- Multi-column layout (about, links, contact, social)
- Floral decorative element in background
- Soft border-top with Turquoise accent

### E. Animations
**Entrance Animations:**
- Hero elements: fade-in + slide-up (0.8s ease-out)
- Section content: fade-in on scroll intersection
- Team cards: stagger fade-up (100ms delays)

**Continuous Animations:**
- Floating petals: gentle vertical movement (4s infinite)
- Logo glow: subtle pulse (3s infinite)
- CTA buttons: gentle scale pulse

**Hover States:**
- Product cards: transform scale-105 + shadow-xl (0.3s)
- Team photos: brightness increase + rotate(2deg)
- Buttons: translate-y(-2px) + shadow enhancement

**Implementation:**
- Use Intersection Observer for scroll-triggered animations
- CSS custom properties for animation timing
- Framer Motion or CSS @keyframes for complex animations

## Images

**Hero Background:**
- Large, soft-focus image of natural flowers or botanical elements
- Light overlay (rgba white 0.3 opacity) for text readability
- Position: center, cover

**Product Images:**
- High-quality product photography on white/beige backgrounds
- Minimum 800x800px, optimized WebP format
- Alt text describing each product

**Team Photos:**
- Professional headshots with natural lighting
- Consistent aspect ratio (1:1 square)
- Soft vignette effect for polish

**Decorative Elements:**
- Use provided floral SVG icons as floating elements
- Scattered throughout sections with rotation variants
- Opacity 0.1-0.3 for subtle presence

## Responsive Behavior
- Mobile: Single column, stacked sections, larger touch targets (min 48px)
- Tablet: Two-column grids, reduced animation complexity
- Desktop: Full multi-column layouts, enhanced animations
- Breakpoints: sm(640px), md(768px), lg(1024px), xl(1280px)