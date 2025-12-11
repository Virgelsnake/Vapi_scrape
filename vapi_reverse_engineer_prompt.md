# Reverse-Engineering Prompt: Vapi.ai Landing Page Clone

## Objective
Analyze and document the complete design, architecture, and component structure of the Vapi.ai landing page (https://vapi.ai) to enable building an identical website with substitute content for [YOUR PRODUCT/SERVICE].

---

## SECTION 1: VISUAL DESIGN & TYPOGRAPHY AUDIT

### Color Palette
- Document the exact color scheme used throughout:
  - Primary brand colors (dominant accent colors)
  - Secondary/supporting colors
  - Neutral palette (grays, blacks, whites)
  - Button states (default, hover, active)
  - Text colors and contrast ratios
  - Background gradients (if any)
- **Deliverable**: Color swatches with hex codes for light/dark modes

### Typography System
- Identify and record all font families used (heading fonts, body text, monospace/code)
- Document font weights, sizes, and line heights for:
  - H1, H2, H3, H4, H5, H6 headings
  - Body text (paragraphs)
  - Navigation items
  - Button text
  - Small labels and captions
- Note any custom or premium fonts (Google Fonts, Typekit, etc.)
- **Deliverable**: Typography hierarchy spreadsheet with exact specifications

### Spacing & Layout Grid
- Measure and document:
  - Top/bottom padding and margins for major sections
  - Horizontal padding/margins (mobile, tablet, desktop)
  - Gap spacing between components and cards
  - Container max-widths
  - Section heights and proportions
- Identify the underlying grid system (8px, 12px, 16px, etc.)
- **Deliverable**: Spacing documentation with measurements for all breakpoints

---

## SECTION 2: NAVIGATION & HEADER

### Top Navigation Bar
- Document structure: logo placement, nav links, CTA buttons
- List all navigation items in order with their destinations:
  - Primary links (Custom Agents, Pricing, Docs, Resources, etc.)
  - Secondary links (Careers, Enterprise)
  - Dropdown menus (identify which nav items have dropdowns)
  - Primary CTA button ("Open Dashboard") styling and placement
- Note sticky/fixed behavior on scroll
- Mobile navigation pattern (hamburger menu, etc.)
- **Deliverable**: Navigation component spec with link structure and behavior

---

## SECTION 3: CORE SECTIONS & LAYOUT STRUCTURE

Document these major sections in order, for each specify:

### 1. Hero Section
- Headline text: "Voice AI agents for developers"
- Subheading/supporting copy
- Primary and secondary CTA buttons ("Sign Up" / "Read the Docs")
- Background treatment (solid color, gradient, image, video, animation)
- Layout type (centered, asymmetrical, etc.)
- Any hero image/video/animation elements

### 2. Social Proof / Logo Carousel
- Title/heading text
- Number of logos displayed (appears to show ~6 client logos)
- Logo carousel behavior (auto-scrolling, manual, etc.)
- Supporting statement below logos
- Spacing and sizing of logos

### 3. Statistics Section / Key Metrics
- The three key numbers displayed:
  - Calls: 150M+
  - Assistants Launched: 1.5M+
  - Developers: 350K+
- Layout: horizontal, cards, or list?
- Visual styling (icons, background, typography weight)

### 4. Value Proposition / "Making voice AI simple and accessible"
- Section title
- Description copy
- Call-to-action links (Github, Download ZIP, Client SDK, Server SDK)
- Visual elements (diagram, illustration, or video)
- Layout and spacing

### 5. Use Cases Section - "Feels human. Moves the needle"
- Tabs/toggle interface (Inbound Calls vs. Outbound Calls)
- Content structure for each tab:
  - Metric callouts (e.g., "powers 400,000+ daily calls")
  - Quote/testimonial with attribution
  - Screenshot/diagram
  - CTA button
- Interaction behavior on tab switching

### 6. How It Works - "Try in minutes. Deploy in days"
- Step-by-step layout (3 steps shown)
- Step card structure:
  - Step number (001, 002, 003)
  - Illustration/image
  - Title
  - Description text
- Visual progression (arrows, lines, etc.)
- Card styling and spacing

### 7. Features Section - "Flexible for engineers. Easy for business users"
- Grid layout for feature cards (appears to be 2 or 3 columns)
- Feature card anatomy:
  - Icon/illustration
  - Title
  - Description text
- Total number of features displayed (~6)
- Icon styling and size
- Background and border treatments

### 8. Enterprise Section
- Header with three pillars: "Reliable", "Scalable", "Secure"
- Feature cards with icons and metrics (99.99% uptime, forward-deployed team, etc.)
- Enterprise client logos/testimonials
- CTA or supporting text

### 9. Community / Statistics Section
- Stats display (250K+ devs, 4.2K+ config points, etc.)
- Links to docs and community
- Layout and styling

### 10. Careers Section
- Section title: "Brilliant minds. Bleeding-edge tech. Relentless drive."
- Hero image/illustration
- CTA button ("See open roles")
- Supporting copy

### 11. FAQ / Accordion Section
- FAQ titles (What is Vapi?, How is this cost-effective?, etc.)
- Accordion open/close behavior
- Typography and styling for questions/answers

### 12. Integrations Section
- Title and subtitle
- Grid display of integration logos (appears to be 40+ logos)
- Logo sizing and grid layout (rows/columns)
- Any grouping or categorization visible

### 13. Footer
- Footer layout and background color
- Links grouped by category
- Copyright/legal text
- Social media links and follower counts
- Newsletter signup (if present)
- Logo/branding placement

---

## SECTION 4: INTERACTIVE ELEMENTS & ANIMATIONS

### Buttons
- Document all button styles:
  - Primary button (color, padding, border-radius, hover state, active state)
  - Secondary button (outline/ghost style, if used)
  - Size variations (large, medium, small, if used)
  - Hover animations (color change, shadow, lift effect, etc.)
  - Focus states (for accessibility)

### Links
- Inline link styling
- Hover states
- Underline behavior

### Forms (if any)
- Input field styling
- Placeholder text
- Focus states
- Validation states

### Animations & Transitions
- Identify any scroll animations (fade-in, slide-in, parallax, etc.)
- Auto-playing carousels/sliders
- Hover effects on cards or images
- Loading states
- Page transition animations
- Smooth scroll behavior

---

## SECTION 5: RESPONSIVE DESIGN BREAKPOINTS

Document design for each breakpoint:
- **Desktop** (1920px, 1440px, 1200px)
- **Tablet** (768px, 800px)
- **Mobile** (375px, 390px, 414px)

For each breakpoint, specify:
- Navigation changes (hamburger menu trigger point)
- Column layout changes (single column vs. multi-column grids)
- Font size adjustments
- Padding/margin adjustments
- Image sizing and optimization
- CTA button placement and sizing
- Carousel/slider behavior

---

## SECTION 6: COMPONENT LIBRARY SPECIFICATION

### Reusable Components to Document:
1. **Card Component**: Used for features, testimonials, steps
   - Padding, border, shadow, background
   - Image aspect ratio
   - Text alignment

2. **Navigation Component**: Top bar, mobile menu, breadcrumbs

3. **Button Component**: All variations (primary, secondary, sizes)

4. **Badge/Pill Component**: For stats, labels (if used)

5. **Testimonial Component**: Quote layout, attribution

6. **Logo Grid Component**: For clients, integrations, investors

7. **Tab/Toggle Component**: For use case switching

8. **Section Container**: Max-width wrapper, spacing

9. **Image Lazy-Loading**: Identify how images are optimized

10. **Icon System**: Icon sources (SVG, icon font, image)

---

## SECTION 7: TECHNICAL ARCHITECTURE

### Technology Stack
- Identify the frontend framework (React, Next.js, Vue, etc.)
- Check for server-side rendering (SSR) or static generation (SSG)
- CSS approach (Tailwind, styled-components, CSS Modules, plain CSS, etc.)
- Animation library (Framer Motion, GSAP, AOS, etc.)
- Image optimization (Next.js Image, Cloudinary, etc.)

### Performance & SEO Considerations
- Meta tags (title, description, open graph)
- Structured data/schema markup
- Sitemap and robots.txt
- Image formats and lazy-loading strategy
- Font loading strategy

---

## SECTION 8: DELIVERABLE OUTPUT FORMAT

Provide a comprehensive design document including:

1. **Visual Design Specification** (PDF or Figma link)
   - Color palette with codes
   - Typography hierarchy
   - Spacing scale
   - Component library mockups

2. **Component Structure Diagram**
   - Visual hierarchy of all sections
   - Reusable component breakdown
   - Layout flow

3. **Responsive Breakpoint Documentation**
   - Screenshots/wireframes for mobile, tablet, desktop
   - Key layout changes at each breakpoint

4. **Interactive Behavior Guide**
   - List of all hover states
   - Animation specifications (duration, easing)
   - Tab/accordion behaviors

5. **Code Architecture Recommendations**
   - Suggested folder structure
   - Component organization
   - Proposed CSS/styling approach
   - State management needs (if any)

6. **Implementation Checklist**
   - Prioritized list of components to build
   - Estimated complexity per component
   - Build order recommendations

---

## ADDITIONAL CONTEXT FOR DEVELOPER

- **Goal**: Create a pixel-perfect replica using [YOUR PRODUCT] content instead of Vapi content
- **Brand Colors to Substitute**: Identify your brand's primary, secondary, and accent colors
- **Content Placeholders**: Note where product-specific copy, metrics, logos, images, and CTAs should be swapped
- **Timeline**: Clarify expected delivery date and any must-have features for launch
- **Collaboration Tools**: Specify whether Figma, Miro, or other tools should be used for documentation