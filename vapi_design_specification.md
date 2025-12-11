# Vapi.ai Design Specification Document

> **Generated**: December 11, 2025  
> **Source**: https://vapi.ai  
> **Purpose**: Complete reverse-engineering documentation for landing page clone

---

## SECTION 1: VISUAL DESIGN & TYPOGRAPHY

### Color Palette

#### Primary Brand Colors
| Color Name | Hex Code | RGB | Usage |
|------------|----------|-----|-------|
| **Brand Primary (Mint Green)** | `#62f6b5` | `rgb(98, 246, 181)` | Primary CTAs, accents |
| **Brand Primary Hovered** | `#82f8c4` | - | Hover states |
| **Brand Purple** | `#9977ff` | `rgb(153, 119, 255)` | Accent, decorative |
| **Brand Pink** | `#de94e2` | `rgb(222, 148, 226)` | Accent, decorative |
| **Brand Yellow** | `#ffdd03` | `rgb(255, 221, 3)` | Accent, decorative |
| **Brand Blue** | `#0090ff` | `rgb(0, 144, 255)` | Links, accents |
| **Cyan Accent** | `#4dcafa` | `rgb(77, 202, 250)` | Decorative elements |

#### Background Colors
| Color Name | Hex Code | RGB | Usage |
|------------|----------|-----|-------|
| **Base Background (Main)** | `#0e0e13` | `rgb(14, 14, 19)` | Primary dark background |
| **Base Background (Alt/Light)** | `#fffaea` | `rgb(255, 250, 234)` | Light section (Enterprise) |
| **Base 950** | `#09090b` | `rgb(9, 9, 11)` | Darkest background |
| **Base 900** | `#18181b` | `rgb(24, 24, 27)` | Card backgrounds |
| **Base 700** | `#3f3f46` | `rgb(63, 63, 70)` | Borders, dividers |

#### Text Colors
| Color Name | Hex Code | RGB | Usage |
|------------|----------|-----|-------|
| **Primary Text** | `#d8d7d4` | `rgb(216, 215, 212)` | Main body text |
| **Secondary Text** | `#a1a1aa` | `rgb(161, 161, 170)` | Muted text |
| **Tertiary Text** | `#717179` | `rgb(113, 113, 122)` | Subtle text |
| **White Text** | `#fcfcfd` | `rgb(252, 252, 253)` | Headlines on dark |
| **Dark Text** | `#0e0e13` | `rgb(14, 14, 19)` | Text on light backgrounds |

#### Border Colors
| Color Name | Hex Code | Usage |
|------------|----------|-------|
| **Base Border** | `#d9d3c2` | Light mode borders |
| **Base 700** | `#3f3f46` | Dark mode borders |
| **Base 800** | - | Section dividers |

---

### Typography System

#### Font Families
| Font | CSS Variable | Usage |
|------|--------------|-------|
| **seasonSans** | `--font-sans` | Headings, body text |
| **Geist Mono** | `--font-mono` | Navigation, buttons, code |

#### Font Weights
| Weight | Value | Usage |
|--------|-------|-------|
| Light | `300` | Subtle text |
| Regular | `400` | Body text |
| Medium | `500` | Buttons, navigation |
| Semi-bold | `570` | Emphasis |
| Bold | `700` | Headlines |

#### Font Sizes (Desktop)
| Element | Size | Notes |
|---------|------|-------|
| H1 (Hero) | `68px - 96px` | Large display heading |
| H2 (Section) | `40px - 56px` | Section headings |
| H3 (Subsection) | `24px - 32px` | Card titles |
| Body Large | `18px - 20px` | Lead paragraphs |
| Body | `15px - 16px` | Standard text |
| Small/Caption | `11px - 12px` | Labels, navigation |
| XS | `10.6px` | Micro text |

---

### Spacing & Layout Grid

#### Container Max-Widths
- **Desktop**: ~1200px - 1440px
- **Tablet**: 768px
- **Mobile**: 100% with padding

#### Section Padding
| Breakpoint | Vertical Padding |
|------------|------------------|
| Desktop | `120px` top/bottom |
| Tablet | `80px` top/bottom |
| Mobile | `80px` top/bottom |

#### Border Radius
| Size | Value | Usage |
|------|-------|-------|
| Small | `0.25rem` (4px) | Small elements |
| Medium | `0.375rem` (6px) | Inputs |
| Large | `0.5rem` (8px) | Cards |
| 2XL | `1rem` (16px) | Large cards |
| Full/Pill | `9999px` | Buttons, pills |

---

## SECTION 2: NAVIGATION & HEADER

### Top Navigation Bar
```
Structure: [LOGO] [Nav Links] [CTA Button]
Position: Fixed/Sticky on scroll
Background: Semi-transparent dark with blur
```

#### Navigation Items (Left to Right)
1. **VAPI** (Logo) → `/`
2. **Custom Agents** → `/custom-agents`
3. **Pricing** → `/pricing`
4. **Docs** → `https://docs.vapi.ai/quickstart/introduction` (external link icon)
5. **Resources** (dropdown)
   - Blog → `/blog`
   - Video Library → `/library`
   - Community → `/community`
   - Events → `https://lu.ma/vapi_events`
6. **Careers** → `/careers`
7. **Enterprise** → `/enterprise`
8. **[Open Dashboard]** (Primary CTA button) → `https://dashboard.vapi.ai/`

#### Navigation Styling
- **Font**: Geist Mono, 11px, weight 500
- **Text Transform**: Uppercase
- **Letter Spacing**: 0.05rem
- **Padding**: 22px 24px per item
- **CTA Button**: Mint green background, dark text, pill shape

---

## SECTION 3: CORE SECTIONS & LAYOUT

### 1. Hero Section
```
Layout: Centered, full-width
Background: Dark (#0e0e13)
Padding-top: 80px (accounts for fixed nav)
```

**Content:**
- **Headline**: "Voice AI agents for developers"
  - Font: seasonSans, 68-96px, weight 700
  - Color: White/off-white
- **CTA Buttons**:
  1. "SIGN UP" → Primary mint green, pill shape
  2. "READ THE DOCS" → Outline/ghost style
- **Interactive Element**: "TALK TO VAPI" button with audio waveform visualization
- **Visual**: Animated colorful dot grid pattern (equalizer style)

### 2. Logo Carousel / Social Proof
```
Layout: Full-width horizontal scroll
Background: Transparent (inherits dark)
Border: Top and bottom border (#3f3f46)
```

**Client Logos:**
- Unity AI, NY Life, Intuit, Instawork, Housecall Pro, Cherry

### 3. Statistics Section
```
Layout: Three-column horizontal
Background: Dark
```

**Metrics** (not visible in initial scan, but referenced):
- Calls: 150M+
- Assistants Launched: 1.5M+
- Developers: 350K+

### 4. Code Sample Section - "Making voice AI simple and accessible"
```
Layout: Two-column (text left, code right)
Background: Dark (#0e0e13)
```

**Features:**
- Language tabs: TypeScript, Python, cURL, React (web SDK)
- Code block with syntax highlighting
- Copy button

### 5. Use Cases - "Feels human. Moves the needle."
```
Layout: Tabbed interface
Background: Dark
```

**Tabs:**
1. **Inbound calls** (default active)
2. **Outbound calls**

**Tab Styling:**
- Active: Background highlight, dark text
- Inactive: Transparent, light text
- Shape: Pill/rounded

### 6. Integrations - "Integrate with more than 40+ apps"
```
Layout: Logo grid
Background: Dark with dotted pattern overlay
```

**Integration Partners (30+):**
OpenAI, Anthropic, 11 Labs, Deepgram, Cartesia, Assembly AI, PlayHT, Azure, Gemini, Groq, Perplexity, Gladia, Langfuse, Twilio, AWS S3, GCP, Google Calendar, Zendesk, Notion, Zapier, Apollo.io, Google Sheets, Salesforce

### 7. How It Works - "Try in minutes. Deploy in days."
```
Layout: Three-step horizontal flow
Background: Dark
```

**Steps:**
1. **001** - "Choose your workflow"
2. **002** - "Plug it in"
3. **003** - "Done"

### 8. Features - "Flexible for engineers. Easy for business users."
```
Layout: Feature card grid (2-3 columns)
Background: Dark
```

**Features:**
- Multilingual
- API-native
- Automated testing
- Bring your own models

### 9. Enterprise Section
```
Layout: Full-width with alternating content
Background: Light cream (#fffaea)
Text: Dark
```

**Headlines:**
- "Reliable." "Scalable." "Secure."

**Metrics:**
- 99.99% uptime
- Forward-deployed team

### 10. Community - "250,000+ devs are already here"
```
Layout: Stats + link cards
Background: Dark
```

**Stats:**
- 4.2K+ (GitHub stars or similar)
- 13K+ (Discord members or similar)
- 9.6K+ (Twitter followers or similar)

**Link Cards:**
- Docs
- Community
- LinkedIn

### 11. Careers - "Brilliant minds. Bleeding-edge tech. Relentless drive."
```
Layout: Full-width hero style
Background: Dark
```

### 12. FAQ - "Your questions, answered."
```
Layout: Accordion list
Background: Dark
```

**Questions:**
1. What is Vapi?
2. How is this more cost-effective for my organisation?
3. What is the difference from other AI voice competitors?
4. I need holistic customization, what types of support does your platform offer?
5. Is it difficult to set up?

### 13. CTA Section - "Get started today"
```
Layout: Centered
Background: Dark with top border
```

### 14. Footer
```
Layout: Multi-column links
Background: Dark
```

**Columns:**
- **Product**: Docs, Pricing, Features, Security
- **Company**: Blog, Careers, Community, Contact
- **Legal**: Privacy Policy, Terms

**Social Links**: Twitter/X, LinkedIn, Discord, GitHub

---

## SECTION 4: INTERACTIVE ELEMENTS & ANIMATIONS

### Button Styles

#### Primary Button (Mint Green)
```css
background-color: #62f6b5;
color: #09090b;
border-radius: 9999px; /* pill */
padding: 8px 20px;
font-family: "Geist Mono";
font-size: 12-20px;
font-weight: 500;
text-transform: uppercase;
letter-spacing: 0.05rem;
transition: all 0.3s;
```

#### Secondary Button (Outline/Ghost)
```css
background-color: transparent;
color: #d8d7d4;
border: 1px solid #3f3f46;
border-radius: 9999px;
padding: 8px 20px;
```

#### Tab Button
```css
background-color: transparent; /* or highlighted when active */
border-radius: 9999px;
padding: 16px 20px;
font-family: seasonSans;
font-size: 15px;
```

### Animations
- **Scroll animations**: Fade-in on scroll (likely using Intersection Observer)
- **Audio waveform**: Animated equalizer visualization in hero
- **Hover effects**: Color transitions, scale (active:scale-95)
- **Transition duration**: 300ms standard

---

## SECTION 5: RESPONSIVE BREAKPOINTS

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | 375px - 767px | Single column, hamburger nav |
| Tablet | 768px - 1023px | 2-column grids |
| Desktop | 1024px+ | Full layout |
| Large Desktop | 1440px+ | Max-width containers |

### Mobile Adaptations
- Navigation collapses to hamburger menu
- Hero text size reduces significantly
- Feature grids become single column
- Reduced padding (pt-14 vs pt-24)

---

## SECTION 6: COMPONENT LIBRARY

### Reusable Components

1. **Section Container**
   - Max-width wrapper
   - Responsive padding
   - Border-top/bottom options

2. **Card Component**
   - Dark background (#18181b or #24242a)
   - Border: 1px solid #3f3f46
   - Border-radius: 8-16px
   - Padding: 24-32px

3. **Button Component**
   - Variants: primary, secondary, ghost
   - Sizes: sm, md, lg
   - States: default, hover, active, disabled

4. **Tab Component**
   - Pill-shaped tabs
   - Active state highlighting
   - Smooth transitions

5. **Accordion/FAQ Component**
   - Question as trigger
   - Expand/collapse animation
   - Icon rotation on toggle

6. **Logo Grid Component**
   - Auto-fit grid
   - Grayscale to color on hover (optional)
   - Consistent sizing

7. **Stats Counter Component**
   - Large number display
   - Label below
   - Animated counting (optional)

---

## SECTION 7: TECHNICAL ARCHITECTURE

### Tech Stack
- **Framework**: Next.js (SSR/SSG)
- **Styling**: Tailwind CSS (evident from class naming)
- **Fonts**: 
  - seasonSans (custom/premium)
  - Geist Mono (Vercel's monospace font)
- **Analytics**: PostHog, HubSpot, LinkedIn Insight, Facebook Pixel, Reddit Pixel, Twitter Ads

### Meta/SEO
```html
<title>Vapi - Build Advanced Voice AI Agents</title>
<meta name="description" content="Build, test, and deploy advanced voice AI agents in minutes with Vapi. The platform for developers creating conversational voice AI.">
<meta name="keywords" content="Voice AI,AI Agents,Voice Agents,Conversational AI,Voice AI Platform,AI Development">
<meta name="theme-color" content="#0E0E13">
<meta property="og:image" content="https://vapi.ai/vapi_social_preview.png">
```

---

## SECTION 8: IMPLEMENTATION CHECKLIST

### Priority Order
1. ☐ Set up Next.js project with Tailwind CSS
2. ☐ Configure fonts (seasonSans alternative, Geist Mono)
3. ☐ Establish color palette CSS variables
4. ☐ Build navigation component
5. ☐ Create button component variants
6. ☐ Build hero section with CTA
7. ☐ Logo carousel component
8. ☐ Stats section
9. ☐ Code sample section with tabs
10. ☐ Use cases tabbed section
11. ☐ Integrations logo grid
12. ☐ How it works 3-step section
13. ☐ Features grid
14. ☐ Enterprise section (light theme)
15. ☐ Community stats section
16. ☐ Careers CTA section
17. ☐ FAQ accordion
18. ☐ Final CTA section
19. ☐ Footer
20. ☐ Mobile responsive adjustments
21. ☐ Animations and transitions

### Font Alternatives
- **seasonSans**: Consider Inter, DM Sans, or Satoshi as alternatives
- **Geist Mono**: Available from Vercel, or use JetBrains Mono

---

## Screenshots Reference
- `vapi-homepage-hero-*.png` - Desktop hero view
- `vapi-fullpage-*.png` - Full page desktop
- `vapi-mobile-*.png` - Mobile full page
- `vapi-tablet-*.png` - Tablet view

All screenshots saved to: `/Users/steveshearman/Downloads/`
