# Requirements Document

## Introduction

Solar Valley Energy (Pty) Ltd requires a modern, responsive marketing website that showcases the company's renewable energy services, builds brand credibility, and generates leads through quote requests. The website follows the "Solar Kinetic" design system — a dark-mode-first, high-contrast aesthetic with sun-yellow accents that evokes industrial-tech precision and environmental stewardship. The site must support both dark and light mode, feature subtle animations, and deliver a premium user experience across all devices.

## Glossary

- **Website**: The Solar Valley Energy marketing website, a single-page application with multiple sections
- **Navigation_Bar**: The fixed top navigation component with logo, links, and call-to-action button
- **Hero_Section**: The full-viewport introductory section with background imagery, headline, and primary calls-to-action
- **Solutions_Grid**: The section displaying solar service offerings as a grid of cards
- **Projects_Section**: The section showcasing completed solar installations
- **Footer**: The bottom section containing links, contact information, and social media
- **Theme_Toggle**: The interactive control that switches between dark mode and light mode
- **CTA_Button**: A call-to-action button designed to prompt user engagement (e.g., "Get a Quote")
- **Design_System**: The "Solar Kinetic" design system defining colors, typography, spacing, and component styles
- **Visitor**: Any person browsing the website

## Requirements

### Requirement 1: Fixed Navigation Bar

**User Story:** As a Visitor, I want a persistent navigation bar at the top of the page, so that I can access any section of the website at all times.

#### Acceptance Criteria

1. THE Navigation_Bar SHALL remain fixed at the top of the viewport during scrolling with a height of 64px and a z-index ensuring it remains above all page content
2. THE Navigation_Bar SHALL display the company logo (logo.png) aligned to the left with a maximum height of 40px
3. THE Navigation_Bar SHALL display navigation links (Home, About Us, Solar Solutions, Products, Projects, Care Plan, Contact Us) centered horizontally using the body-md typography style (Manrope, 16px, weight 400)
4. THE Navigation_Bar SHALL display a "GET A QUOTE" ghost-style button aligned to the right with a 1px border in primary color, no background fill, and 4px border-radius
5. THE Navigation_Bar SHALL apply a backdrop blur effect (8px minimum) to the background with a semi-transparent surface-container background color
6. THE Navigation_Bar SHALL use a 1px bottom border in the outline-variant color (#504535) for definition
7. WHEN a Visitor scrolls such that a section's top edge is within 80px of the viewport top, THE Navigation_Bar SHALL indicate the corresponding navigation link as active with a 2px bottom border in the primary-container color (#F4B63F)
8. WHEN a Visitor hovers over a navigation link, THE Navigation_Bar SHALL transition the link text color to the primary color (#ffd795) within 200ms using an ease timing function
9. WHEN a Visitor hovers over the "GET A QUOTE" button, THE CTA_Button SHALL fill with the primary-container color (#F4B63F) and change text to on-primary-container color (#694900) within 200ms
10. WHEN the viewport width is below 768px, THE Navigation_Bar SHALL replace navigation links with a hamburger menu icon (three horizontal lines) aligned to the right
11. WHEN a Visitor taps the hamburger menu icon, THE Navigation_Bar SHALL reveal a full-width dropdown panel below the navigation bar displaying all navigation links stacked vertically with 48px minimum touch-target height per link
12. WHEN a Visitor taps the hamburger menu icon while the mobile menu is open, THE Navigation_Bar SHALL close the dropdown panel within 200ms
13. IF the Visitor clicks a navigation link, THEN THE Navigation_Bar SHALL smooth-scroll the viewport to the corresponding page section and close the mobile menu if open

### Requirement 2: Dark Mode and Light Mode Support

**User Story:** As a Visitor, I want to toggle between dark mode and light mode, so that I can view the website in my preferred visual style.

#### Acceptance Criteria

1. IF no theme preference exists in local storage, THEN THE Website SHALL default to dark mode on initial load
2. THE Theme_Toggle SHALL be visible within the Navigation_Bar and SHALL indicate the currently active theme (dark or light) via its icon or label state
3. WHEN a Visitor activates the Theme_Toggle, THE Website SHALL switch all page background, text, and component colors to the corresponding theme palette within 300ms
4. WHEN dark mode is active, THE Website SHALL use #121414 as the base background color and #E2E2E2 as the primary text color
5. WHEN light mode is active, THE Website SHALL use #FFFFFF as the base background color and #121414 as the primary text color
6. WHILE light mode is active, THE Website SHALL maintain the primary yellow (#F4B63F) for accent elements and call-to-action components
7. WHEN a Visitor activates the Theme_Toggle, THE Website SHALL persist the selected theme preference in local storage
8. WHEN a Visitor returns to the Website and a valid theme preference exists in local storage, THE Theme_Toggle SHALL restore the previously selected theme
9. IF local storage is unavailable or the stored theme preference is not a recognized value (dark or light), THEN THE Website SHALL default to dark mode and allow toggling without persistence
10. THE Theme_Toggle SHALL be keyboard-operable and include an accessible label indicating its purpose and current state

### Requirement 3: Hero Section

**User Story:** As a Visitor, I want an impactful hero section when I first arrive, so that I immediately understand what Solar Valley Energy offers.

#### Acceptance Criteria

1. THE Hero_Section SHALL occupy a minimum of 90vh (90% of the viewport height)
2. THE Hero_Section SHALL display a viewport-width background image with a vertical gradient overlay transitioning from 40% opacity at the top to 80% opacity at the bottom using the surface color (#121414)
3. THE Hero_Section SHALL display the tagline label "POWERING TOMORROW" in JetBrains Mono at the label-caps size (12px, font-weight 500, letter-spacing 0.1em), uppercase, with the primary yellow color (#F4B63F)
4. THE Hero_Section SHALL display a primary headline using Hanken Grotesk at the display size (72px desktop / 32px mobile, font-weight 800, line-height 80px desktop / 40px mobile) with a maximum length of 80 characters
5. THE Hero_Section SHALL display a subtext paragraph of no more than 200 characters using Manrope at body-lg size (18px, font-weight 400, line-height 28px) summarising the company's solar energy services and value proposition
6. THE Hero_Section SHALL display a primary filled CTA button ("Our Solutions") with sun-yellow (#F4B63F) background and black text, and a secondary ghost CTA button ("Watch Video") with a 1px white border and white text
7. THE Hero_Section SHALL use a 4px border radius on all buttons
8. THE Hero_Section SHALL left-align all text content and stack elements vertically in the order: tagline label, headline, subtext, buttons
9. IF the viewport width is less than 768px, THEN THE Hero_Section SHALL display the headline at 32px and reduce the section minimum height to 80vh

### Requirement 4: Quick Stats Features Row

**User Story:** As a Visitor, I want to see key service highlights at a glance, so that I can quickly understand the company's core capabilities.

#### Acceptance Criteria

1. THE Website SHALL display a features row immediately below the Hero_Section with no visible gap between sections
2. THE Website SHALL display exactly four feature items in a horizontal grid on viewports 768px and wider, and in a single column layout on viewports below 768px
3. EACH feature item SHALL include a Material Symbols Outlined icon in primary-container color (#F4B63F), a bold title in uppercase using label-caps typography, and a description of no more than 80 characters in secondary text color
4. THE Website SHALL separate the features row from adjacent sections using a 1px horizontal border on both top and bottom edges in outline-variant color
5. THE Website SHALL display the following four feature items in order: "Residential Solar", "Commercial Solutions", "Battery Backup", and "Maintenance & Support", each with a relevant icon and description summarizing that capability

### Requirement 5: About Us Section

**User Story:** As a Visitor, I want to learn about Solar Valley Energy's identity and values, so that I can determine if the company aligns with my needs.

#### Acceptance Criteria

1. WHILE the viewport width is 1024px or greater, THE Website SHALL display the About Us section in a two-column layout with textual content on the left and imagery on the right
2. WHILE the viewport width is below 1024px, THE Website SHALL stack the About Us section into a single-column layout with textual content above imagery
3. THE Website SHALL display the section label "ABOUT US" in JetBrains Mono, label-caps style (12px, 500 weight, 0.1em letter-spacing), uppercase, in the primary yellow color (#F4B63F)
4. THE Website SHALL display a section headline "WHO WE ARE" in Hanken Grotesk, bold (700 weight), uppercase, at headline-md size (32px)
5. THE Website SHALL display descriptive paragraphs about the company identity and values in Manrope at body-md size (16px/24px line-height) with secondary text color (#E0E0E0)
6. THE Website SHALL display a "Learn More" primary filled button (background #F4B63F, dark text, bold weight) with 4px border radius that navigates the user to the full About Us page or section
7. THE Website SHALL display 2 to 4 supporting images in a grid layout with a maximum 8px border radius and no more than 2 columns on desktop
8. WHEN a visitor activates the "Learn More" button, THE Website SHALL navigate to a dedicated view presenting the company's full mission, vision, and values content

### Requirement 6: Solar Solutions Grid

**User Story:** As a Visitor, I want to browse available solar services, so that I can find the solution relevant to my property type.

#### Acceptance Criteria

1. THE Solutions_Grid SHALL display service cards for Residential Solar, Commercial Solar, Backup Power Systems, and Maintenance and Care
2. THE Solutions_Grid SHALL use a four-column layout on viewports wider than 1024px, a two-column layout on viewports between 600px and 1024px, and a single-column layout on viewports narrower than 600px
3. EACH service card SHALL include a top-aligned image with a 16:9 aspect ratio, a category icon, a bold uppercase title (maximum 40 characters), and a description paragraph (maximum 120 characters)
4. EACH service card SHALL use the surface-container background (#1E2020 in dark mode) with a 1px border in outline-variant color
5. EACH service card SHALL use a maximum 8px border radius on the card container
6. WHEN a Visitor hovers over a service card, THE Solutions_Grid SHALL transition the card border color from outline-variant to primary color within 200ms
7. THE Solutions_Grid SHALL separate cards with a 24px gap in both row and column directions

### Requirement 7: Projects Showcase Section

**User Story:** As a Visitor, I want to see examples of completed installations, so that I can evaluate the quality and scope of Solar Valley Energy's work.

#### Acceptance Criteria

1. THE Projects_Section SHALL display a grid of project items where each item contains a project image and a category label, arranged in a 12-column grid layout on viewports 768px and above, and a single-column stacked layout on viewports below 768px
2. THE Projects_Section SHALL display a minimum of four project items visible simultaneously on desktop viewports (768px and above) in a horizontal grid row
3. EACH project item SHALL include a project image with a maximum 8px border radius and a category label displayed in uppercase JetBrains Mono at 12px font size with 0.1em letter spacing
4. THE Projects_Section SHALL include previous and next arrow navigation controls styled with a 1px primary color border, where activating a control scrolls the project grid by one item in the corresponding direction
5. IF the project grid is scrolled to the first item, THEN THE Projects_Section SHALL visually disable the previous arrow control, and IF scrolled to the last item, THEN THE Projects_Section SHALL visually disable the next arrow control

### Requirement 8: Call-to-Action Section

**User Story:** As a Visitor, I want a clear prompt to take the next step, so that I can easily request a quote or learn more about Solar Valley Energy's services.

#### Acceptance Criteria

1. THE Website SHALL display a CTA section with a centered headline using the headline-md typography style (max 60 characters), a supporting body-lg paragraph (max 200 characters) describing the next step or value proposition, and action buttons arranged horizontally below the text with 16px gap between buttons
2. THE CTA section SHALL include a primary filled button labelled "Request a Custom Quote" and a secondary ghost button labelled "Download Portfolio", where the primary button navigates the user to the quote request form and the secondary button initiates a portfolio file download
3. THE CTA section SHALL use the surface-container-low background to create visual separation from adjacent sections
4. ALL buttons in the CTA section SHALL use a 4px border radius
5. WHEN the viewport width is less than 768px, THE CTA section SHALL stack the action buttons vertically at full width while maintaining the centered text alignment
6. WHEN a user hovers over or focuses on a CTA button, THE Website SHALL display a visible state change within 100ms to indicate interactivity

### Requirement 9: Footer

**User Story:** As a Visitor, I want structured access to company information, links, and contact details, so that I can navigate or reach out to Solar Valley Energy.

#### Acceptance Criteria

1. THE Footer SHALL display a four-column layout on desktop (brand, quick links, contact info, social/CTA) and SHALL stack into a single-column layout on viewports below 768px wide
2. THE Footer SHALL display the company logo and a descriptor text of no more than 150 characters summarizing the company purpose
3. THE Footer SHALL display quick links matching the Navigation_Bar links in the same order, and each link SHALL scroll the page to the corresponding section
4. THE Footer SHALL display contact information including phone number, email address, physical location, and website URL
5. THE Footer SHALL display social media icon links (Facebook, Instagram, LinkedIn) that open in a new browser tab
6. WHEN a Visitor clicks the "GET A QUOTE" ghost button, THE Footer SHALL navigate the Visitor to the Quote_Request section
7. THE Footer SHALL display a copyright bar at the bottom separated by a 1px border in outline-variant color
8. WHEN a Visitor hovers over a social media icon, THE Footer SHALL fill the icon background with primary yellow and change the icon color to dark within 200ms

### Requirement 10: Typography and Design System Compliance

**User Story:** As a Visitor, I want consistent, readable typography throughout the website, so that I experience a polished and professional brand.

#### Acceptance Criteria

1. THE Website SHALL use Hanken Grotesk for all headings and display text, with display set at 800 weight and headlines at 600–700 weight as defined in the typography scale
2. THE Website SHALL use Manrope at 400 weight for all body text and paragraphs
3. THE Website SHALL use JetBrains Mono at 500 weight for all labels, overlines, and utility text
4. THE Website SHALL load all fonts from Google Fonts with system sans-serif declared as the fallback font-family for headings and body, and system monospace as the fallback for utility text
5. THE Website SHALL use spacing values that are multiples of 8px for all padding, margins, and gaps
6. THE Website SHALL restrict border radius to 4px for interactive components (buttons, inputs, chips) and permit up to 8px for large content containers (hero sections, feature cards)
7. THE Website SHALL achieve depth through tonal layering using at least three surface color tiers (base, mid, top) rather than box shadows, except that subtle box shadows may be applied to floating elements such as modals and pop-overs
8. THE Website SHALL use 1px borders in outline-variant color to define card boundaries and component edges where visual separation from the background is needed

### Requirement 11: Subtle Animations and Transitions

**User Story:** As a Visitor, I want subtle visual feedback during interactions, so that the website feels responsive and modern without being distracting.

#### Acceptance Criteria

1. THE Website SHALL apply CSS transition on background-color, color, and border-color properties of all interactive elements (links, buttons, icons) with a duration between 150ms and 300ms and an ease-out timing function
2. WHEN a Visitor hovers over a card image, THE Website SHALL apply a scale transform (maximum 1.05 scale) with a duration of 700ms and an ease-out timing function
3. THE Website SHALL avoid box-shadow-based elevation changes on hover
4. WHEN a Visitor presses a primary button, THE Website SHALL apply a scale reduction to 0.95 with a transition duration between 50ms and 100ms
5. WHEN a Visitor scrolls past 50px from the top of the page, THE Navigation_Bar SHALL transition from a backdrop blur of 0px to a backdrop blur of 12px with a transition duration between 200ms and 400ms
6. THE Website SHALL use ease-out as the default timing function for all hover and scroll-triggered transitions, and ease-in for all active-state (press) transitions

### Requirement 12: Responsive Layout

**User Story:** As a Visitor, I want the website to adapt to my device screen size, so that I have a usable experience on mobile, tablet, and desktop.

#### Acceptance Criteria

1. THE Website SHALL use a maximum container width of 1280px centered horizontally with auto left and right margins
2. THE Website SHALL use a 12-column grid on desktop (viewport width above 1024px), an 8-column grid on tablet (viewport width between 768px and 1024px), and a 4-column grid on mobile (viewport width below 768px)
3. WHEN the viewport width is below 768px, THE Website SHALL stack all multi-column layouts into a single column with elements appearing in source order
4. THE Website SHALL use 24px horizontal padding on viewports at or above 768px and 16px horizontal padding on viewports below 768px
5. THE Website SHALL maintain section vertical spacing between 80px and 120px on viewports at or above 768px, and between 48px and 80px on viewports below 768px
6. WHEN the viewport is resized or the device orientation changes, THE Website SHALL reflow content without requiring horizontal scrolling and without content overflow beyond the viewport width
7. THE Website SHALL render all interactive elements (buttons, links, form inputs) with a minimum touch-target size of 44×44 CSS pixels on viewports below 768px

### Requirement 13: Logo Integration

**User Story:** As a Visitor, I want to see the Solar Valley Energy branding clearly, so that I can identify the company and build brand recognition.

#### Acceptance Criteria

1. THE Navigation_Bar SHALL display logo.png at a height of 40-48px with auto width, maintaining aspect ratio, and the logo SHALL be wrapped in a link that navigates to the homepage
2. THE Footer SHALL display logo.png at a height of 56-64px with auto width, maintaining aspect ratio
3. THE Website SHALL use the logo.png file provided in the project assets without cropping, recoloring, or distorting the image
4. THE Website SHALL render the logo with an alt attribute containing the text "Solar Valley Energy" for accessibility
5. WHEN the viewport width is less than 768px, THE Navigation_Bar SHALL display logo.png at a height of 32-40px with auto width, maintaining aspect ratio
