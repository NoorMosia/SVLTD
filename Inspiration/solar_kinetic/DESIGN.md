---
name: Solar Kinetic
colors:
  surface: '#121414'
  surface-dim: '#121414'
  surface-bright: '#37393a'
  surface-container-lowest: '#0c0f0f'
  surface-container-low: '#1a1c1c'
  surface-container: '#1e2020'
  surface-container-high: '#282a2b'
  surface-container-highest: '#333535'
  on-surface: '#e2e2e2'
  on-surface-variant: '#d4c4af'
  inverse-surface: '#e2e2e2'
  inverse-on-surface: '#2f3131'
  outline: '#9d8f7b'
  outline-variant: '#504535'
  surface-tint: '#fabc44'
  primary: '#ffd795'
  on-primary: '#422c00'
  primary-container: '#f4b63f'
  on-primary-container: '#694900'
  inverse-primary: '#7d5700'
  secondary: '#c8c6c5'
  on-secondary: '#313030'
  secondary-container: '#4a4949'
  on-secondary-container: '#bab8b7'
  tertiary: '#dedcdb'
  on-tertiary: '#303030'
  tertiary-container: '#c2c0c0'
  on-tertiary-container: '#4f4e4e'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#ffdeaa'
  primary-fixed-dim: '#fabc44'
  on-primary-fixed: '#271900'
  on-primary-fixed-variant: '#5f4100'
  secondary-fixed: '#e5e2e1'
  secondary-fixed-dim: '#c8c6c5'
  on-secondary-fixed: '#1c1b1b'
  on-secondary-fixed-variant: '#474646'
  tertiary-fixed: '#e5e2e1'
  tertiary-fixed-dim: '#c8c6c5'
  on-tertiary-fixed: '#1b1b1c'
  on-tertiary-fixed-variant: '#474746'
  background: '#121414'
  on-background: '#e2e2e2'
  surface-variant: '#333535'
typography:
  display:
    fontFamily: Hanken Grotesk
    fontSize: 72px
    fontWeight: '800'
    lineHeight: 80px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Hanken Grotesk
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Hanken Grotesk
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
  headline-md:
    fontFamily: Hanken Grotesk
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
  body-lg:
    fontFamily: Manrope
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Manrope
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-caps:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.1em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 8px
  container-max: 1280px
  gutter: 24px
  margin-mobile: 16px
  section-gap-lg: 120px
  section-gap-md: 80px
---

## Brand & Style

This design system is engineered to evoke a sense of high-tech reliability, environmental stewardship, and the limitless potential of renewable energy. It targets homeowners and enterprise-level stakeholders who value precision, engineering excellence, and aesthetic sophistication.

The visual style is **Corporate Modern with a High-Contrast edge**. It utilizes deep, "infinite" backgrounds to represent stability and the vast sky, punctuated by vibrant yellow accents that symbolize captured sunlight. The interface should feel premium and intentional, using expansive imagery and surgical precision in its alignment to reflect the technical nature of solar hardware.

## Colors

The palette is anchored by high-density blacks and charcoals to create a cinematic backdrop that allows hardware and iconography to "glow." 

- **Primary:** A vibrant, sun-soaked yellow (#F4B63F) used exclusively for high-priority calls to action, active states, and technical iconography.
- **Surface Tiers:** The primary background is #121212, while secondary containers and card elements utilize #1E1E1E to create subtle depth without relying on heavy shadows.
- **Typography:** Pure white (#FFFFFF) is reserved for headers to ensure maximum contrast, while a slightly muted white (#E0E0E0) is used for body text to reduce eye strain on dark backgrounds.

## Typography

Typography in this design system prioritizes a technical, engineered aesthetic. 

- **Headers:** Hanken Grotesk provides a sharp, contemporary sans-serif look with tight kerning for a commanding presence. Large headers should be set in Bold or ExtraBold.
- **Body:** Manrope offers excellent legibility at smaller scales, ensuring that complex technical data and descriptions are easily digestible.
- **Utility:** JetBrains Mono is used for overlines, labels, and technical specs (e.g., "KWH", "VOLTAGE") to reinforce the high-tech, data-driven nature of the brand.

## Layout & Spacing

This design system employs a **Fluid-Fixed hybrid grid**. The layout remains fluid for tablet and mobile devices to maximize screen real estate, but snaps to a 1280px fixed-width container on desktop to ensure optimal line lengths for technical reading.

- **Grid:** A 12-column system is used for desktop, 8 columns for tablet, and 4 columns for mobile. 
- **Rhythm:** An 8px linear scale governs all spacing. Section heights are generous (80px–120px) to allow the "dark" aesthetic to feel airy rather than cramped.
- **Alignment:** Content is generally center-aligned for marketing sections and left-aligned for data-heavy product grids.

## Elevation & Depth

In a dark-mode-first system, depth is achieved through **Tonal Layering** rather than traditional shadows. 

- **Base Layer:** #121212 for the main viewport background.
- **Mid Layer:** #1E1E1E for cards, content blocks, and navigation bars.
- **Top Layer:** #2A2A2A for hover states and interactive pop-overs.
- **Outlines:** Use 1px borders in #333333 to define card boundaries. This creates a "precision-milled" look that mirrors the aluminum frames of solar panels. Shadows, if used, should be extremely subtle (black with 40% opacity) and only applied to high-level floating elements like modals.

## Shapes

The shape language is primarily **Soft (0.25rem)**. 

While the brand is modern, overly rounded or pill-shaped elements are avoided to maintain a serious, industrial-tech feel. Buttons and input fields use a consistent 4px radius. 

Large-scale containers, such as hero images or feature cards, may use a slightly more pronounced 8px (rounded-lg) radius to feel more approachable in consumer-facing contexts, but core UI components remain sharp and disciplined.

## Components

- **Buttons:** 
    - *Primary:* Filled with sun-yellow (#F4B63F), black text, bold weight. Use sharp 4px corners.
    - *Secondary:* Ghost style with 1px white or yellow border and white text.
- **Icons:** Use thin-stroke (1.5pt) monolinear icons. When possible, accent key icons with a yellow circular background or a small yellow "plus" indicator.
- **Cards:** Use the mid-layer background (#1E1E1E) with a subtle 1px border (#333333). Media should be top-aligned with no internal padding on the container edges.
- **Inputs:** Dark background (#0A0A0A) with a light gray border. On focus, the border transitions to sun-yellow.
- **Chips:** Small, rectangular labels with the JetBrains Mono typeface, used for categories like "Residential" or "Off-Grid."
- **Progress/Data Visuals:** Use the primary yellow for data visualizations (charts, energy meters) against the dark background to create high-visibility "energy signatures."