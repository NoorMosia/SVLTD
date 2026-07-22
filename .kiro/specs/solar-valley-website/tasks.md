# Implementation Plan: Solar Valley Energy Website

## Overview

Build the Solar Valley Energy marketing website as a single `index.html` file using Tailwind CSS CDN, Google Fonts (Hanken Grotesk, Manrope, JetBrains Mono), Material Symbols Outlined icons, and vanilla JavaScript for interactivity. The implementation follows an incremental approach: HTML skeleton with Tailwind config first, then each section top-to-bottom, then interactive behaviors.

## Tasks

- [x] 1. Set up HTML skeleton and Tailwind configuration
  - [x] 1.1 Create the base index.html with document structure, meta tags, and external resources
    - Create `index.html` in the project root (`c:/code/SVLTD/Inspiration/`)
    - Add `<!DOCTYPE html>`, `<html class="dark" lang="en">`, viewport meta, charset
    - Link Google Fonts: Hanken Grotesk (300–800), Manrope (400, 500), JetBrains Mono (500)
    - Link Material Symbols Outlined icon font
    - Add Tailwind CSS CDN script (`https://cdn.tailwindcss.com?plugins=forms,container-queries`)
    - Add inline `<script>` block with `tailwind.config` containing Solar Kinetic design tokens (colors, fontFamily, fontSize, spacing, borderRadius) matching the design system YAML
    - Add custom `<style>` block for hero-gradient, nav-blur backdrop-filter, and text-shadow utility
    - Set `<body>` with `class="bg-background text-on-background font-body-md antialiased"`
    - _Requirements: 10.1, 10.2, 10.3, 10.4, 10.5, 10.6, 10.7, 10.8, 12.1_

- [x] 2. Implement the Navigation Bar
  - [x] 2.1 Build the fixed navigation header with logo, links, theme toggle, and CTA button
    - Create `<header>` with fixed positioning, h-16 (64px), z-50, border-b in outline-variant
    - Add logo.png (height 40–48px, wrapped in anchor to `#`) with alt text "Solar Valley Energy"
    - Add nav links: Home, About Us, Solar Solutions, Products, Projects, Care Plan, Contact Us using Manrope body-md
    - Add theme toggle button (sun/moon icon from Material Symbols) with accessible label and keyboard operability
    - Add "GET A QUOTE" ghost button with 1px primary border, 4px border-radius, hover fill effect
    - Style hover transitions on links (color → primary, 200ms ease) and button (fill primary-container, 200ms)
    - Add `transition-all duration-300` for backdrop-blur animation on scroll
    - _Requirements: 1.1, 1.2, 1.3, 1.4, 1.5, 1.6, 1.8, 1.9, 2.2, 2.10, 13.1, 13.3, 13.4_

  - [x] 2.2 Implement the mobile responsive navigation (hamburger menu)
    - Add hamburger icon button visible only below md (768px) with `md:hidden`
    - Hide desktop nav links below md with `hidden md:flex`
    - Create full-width dropdown panel (hidden by default) with vertical nav links, 48px min touch targets
    - Reduce logo height to 32–40px on mobile
    - _Requirements: 1.10, 1.11, 1.12, 12.7, 13.5_

- [x] 3. Implement the Hero Section
  - [x] 3.1 Build the hero section with background image, gradient overlay, and content
    - Create `<section id="home">` with min-h-[90vh], flex items-center, pt-20
    - Apply background image with inline style gradient overlay (40% → 80% opacity)
    - Add tagline label "POWERING TOMORROW" in JetBrains Mono label-caps, primary yellow, with decorative line
    - Add primary headline (Hanken Grotesk, display size 72px/800 weight desktop, 32px mobile) with "RELIABLE ENERGY." and "SUSTAINABLE FUTURE." in primary color
    - Add subtext paragraph (Manrope, body-lg, max 200 chars, text-secondary)
    - Add "Our Solutions" primary filled button and "Watch Video" ghost button with play icon
    - Apply 4px border radius on all buttons
    - Left-align content, stack vertically: tagline → headline → subtext → buttons
    - Ensure responsive: 80vh min-height and 32px headline on mobile
    - _Requirements: 3.1, 3.2, 3.3, 3.4, 3.5, 3.6, 3.7, 3.8, 3.9_

- [x] 4. Implement the Quick Stats Features Row
  - [x] 4.1 Build the four-item features row below the hero
    - Create `<section>` with border-t and border-b in outline-variant, py-12
    - Add 4-column grid (`grid-cols-1 md:grid-cols-4`) with 24px gap
    - Add four feature items: "Residential Solar", "Commercial Solutions", "Battery Backup", "Maintenance & Support"
    - Each item: Material Symbols icon in primary-container color, bold uppercase title (label-caps), description (max 80 chars) in secondary text
    - _Requirements: 4.1, 4.2, 4.3, 4.4, 4.5_

- [x] 5. Implement the About Us Section
  - [x] 5.1 Build the About Us two-column layout with text and imagery
    - Create `<section id="about">` with py-[80px] to py-[120px] (section spacing)
    - Two-column grid: `grid-cols-1 lg:grid-cols-2` with 64px gap
    - Left column: "ABOUT US" label (JetBrains Mono, label-caps, primary), "WHO WE ARE" headline (Hanken Grotesk, headline-md, bold, uppercase), descriptive paragraphs (Manrope, body-md, text-secondary), "Learn More" primary filled button
    - Right column: 2-4 images in grid layout (max 2 cols), 8px border-radius
    - Stack to single column below 1024px (text above images)
    - _Requirements: 5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8_

- [x] 6. Implement the Solar Solutions Grid
  - [x] 6.1 Build the solutions section with four service cards
    - Create `<section id="solutions">` with section spacing, centered header
    - Add section label and headline following the same pattern as About Us
    - Create responsive grid: `grid-cols-1 md:grid-cols-2 lg:grid-cols-4` with 24px gap
    - Four cards: Residential Solar, Commercial Solar, Backup Power Systems, Maintenance & Care
    - Each card: top image (16:9), category icon, bold uppercase title (max 40 chars), description (max 120 chars)
    - Card styling: surface-container background, 1px outline-variant border, 8px border-radius, overflow-hidden
    - Add hover transition: border-color from outline-variant to primary within 200ms
    - _Requirements: 6.1, 6.2, 6.3, 6.4, 6.5, 6.6, 6.7_

- [x] 7. Checkpoint - Verify core sections render correctly
  - Ensure all tests pass, ask the user if questions arise.

- [x] 8. Implement the Projects Showcase Section
  - [x] 8.1 Build the projects section with grid and navigation arrows
    - Create `<section id="projects">` with section spacing, surface-container-lowest background
    - Add centered section label and headline
    - Create project grid: `grid-cols-1 md:grid-cols-4` with 16px gap
    - Add minimum four project items: image (8px border-radius) + category label (JetBrains Mono uppercase 12px)
    - Add previous/next arrow navigation controls with 1px primary border, circular styling
    - Add image hover: `scale(1.05)` transform over 700ms ease-out with overflow-hidden on container
    - _Requirements: 7.1, 7.2, 7.3, 7.4, 7.5, 11.2_

- [x] 9. Implement the CTA Section
  - [x] 9.1 Build the call-to-action section with headline and buttons
    - Create `<section>` with surface-container-low background, centered text
    - Add headline (headline-md, max 60 chars) and body paragraph (body-lg, max 200 chars)
    - Add "Request a Custom Quote" primary filled button and "Download Portfolio" ghost button, 16px gap
    - 4px border radius on buttons
    - Stack buttons vertically at full width on mobile (<768px)
    - Add hover/focus state transitions within 100ms
    - _Requirements: 8.1, 8.2, 8.3, 8.4, 8.5, 8.6_

- [x] 10. Implement the Footer
  - [x] 10.1 Build the four-column footer with brand, links, contact, and social
    - Create `<footer>` with surface-container-lowest background, border-t in outline-variant
    - Four-column grid: `grid-cols-1 md:grid-cols-4` with gap-12
    - Brand column: logo.png (56–64px height), descriptor text (max 150 chars)
    - Quick links column: same links as nav bar, same order, scrolling to corresponding sections
    - Contact column: phone, email, location, website with Material Symbols icons
    - Social/CTA column: Facebook, Instagram, LinkedIn icons (open in new tab), "GET A QUOTE" ghost button
    - Add social icon hover: fill primary background, change icon to dark, 200ms
    - Add copyright bar at bottom separated by 1px border
    - Stack to single column on mobile
    - _Requirements: 9.1, 9.2, 9.3, 9.4, 9.5, 9.6, 9.7, 9.8, 13.2, 13.3, 13.4_

- [x] 11. Checkpoint - Verify all sections are rendered and responsive
  - Ensure all tests pass, ask the user if questions arise.

- [x] 12. Implement JavaScript interactivity
  - [x] 12.1 Implement the theme toggle with localStorage persistence
    - Add `DOMContentLoaded` listener
    - On load: read `localStorage.getItem('sv-theme')`; if `'light'` remove `dark` class from `<html>`, else ensure `dark` class present
    - Toggle button click: flip `dark` class on `<html>`, persist new value to localStorage
    - Wrap localStorage access in try/catch for private browsing fallback
    - Validate stored value is 'dark' or 'light', default to 'dark' if invalid
    - Transition all colors within 300ms (use `transition-colors duration-300` on body/main containers)
    - Update toggle icon state (sun ↔ moon)
    - _Requirements: 2.1, 2.3, 2.4, 2.5, 2.6, 2.7, 2.8, 2.9_

  - [x] 12.2 Implement mobile menu toggle functionality
    - Toggle dropdown panel visibility on hamburger button click
    - Close menu on nav link click
    - Ensure open/close transitions within 200ms
    - _Requirements: 1.11, 1.12, 1.13_

  - [x] 12.3 Implement smooth scroll navigation and active link highlighting
    - Add `scroll-behavior: smooth` to `<html>` or use JS `scrollIntoView({ behavior: 'smooth' })`
    - Set up IntersectionObserver on all section elements with `rootMargin: '-80px 0px 0px 0px'`
    - When a section enters the viewport top 80px zone, add 2px bottom border (primary-container) to corresponding nav link, remove from others
    - On nav link click: smooth-scroll to target section, close mobile menu if open
    - _Requirements: 1.7, 1.13_

  - [x] 12.4 Implement scroll-triggered navigation blur effect
    - Add scroll event listener (debounced or passive)
    - When scrollY > 50px: add backdrop-blur-[12px] and semi-transparent background to header
    - When scrollY <= 50px: remove blur (backdrop-blur-0)
    - Transition between states within 200–400ms
    - _Requirements: 1.5, 11.5_

  - [x] 12.5 Implement project carousel arrow navigation
    - Add click handlers to previous/next arrow buttons
    - Scroll the project grid by one item width in the corresponding direction
    - Visually disable previous arrow at first item, next arrow at last item
    - _Requirements: 7.4, 7.5_

- [x] 13. Implement light mode styles
  - [x] 13.1 Add Tailwind dark-mode variant classes for light mode support
    - Ensure all sections use `dark:` prefixed classes for dark-mode colors and non-prefixed for light
    - Light mode base: bg-white, text-[#121414]
    - Maintain primary yellow (#F4B63F) for accents in both modes
    - Update Solutions Grid section to use white/light-gray background in light mode
    - Verify all text has sufficient contrast in both modes
    - _Requirements: 2.4, 2.5, 2.6_

- [x] 14. Apply animations and transitions polish
  - [x] 14.1 Add CSS transitions and micro-interactions across all interactive elements
    - Ensure all interactive elements (links, buttons, icons) have `transition-colors duration-200 ease-out`
    - Add card image hover: `group-hover:scale-105 transition-transform duration-700 ease-out`
    - Add button active/press state: `active:scale-95` with 50–100ms transition
    - Avoid box-shadow elevation on hover
    - Use ease-out for hover/scroll transitions, ease-in for active/press
    - _Requirements: 11.1, 11.2, 11.3, 11.4, 11.5, 11.6_

- [x] 15. Final checkpoint - Verify complete site functionality
  - Ensure all tests pass, ask the user if questions arise.

## Notes

- All implementation is in a single `index.html` file with no build step required
- Images can use placeholder URLs from the inspiration files or external sources initially
- The `logo.png` file already exists in the project directory
- The inspiration files (`solar_valley_home/code.html`, `our_projects_solar_valley/code.html`) serve as reference for Tailwind class patterns and component structure
- Tailwind config uses the Solar Kinetic design system tokens directly
- No property-based tests apply to this static marketing site (per design document)
- Each task references specific requirements for traceability
- Checkpoints ensure incremental validation

## Task Dependency Graph

```json
{
  "waves": [
    { "id": 0, "tasks": ["1.1"] },
    { "id": 1, "tasks": ["2.1", "3.1"] },
    { "id": 2, "tasks": ["2.2", "4.1", "5.1"] },
    { "id": 3, "tasks": ["6.1", "8.1"] },
    { "id": 4, "tasks": ["9.1", "10.1"] },
    { "id": 5, "tasks": ["12.1", "12.2", "13.1"] },
    { "id": 6, "tasks": ["12.3", "12.4", "12.5"] },
    { "id": 7, "tasks": ["14.1"] }
  ]
}
```
