# Portfolio Website Specification - Ayan Nazm

## 1. Project Overview

**Project Name:** Ayan Nazm Portfolio
**Type:** Single-page personal portfolio website
**Core Functionality:** Showcase analytics professional's background, skills, and projects with an immersive dark theme
**Target Users:** Recruiters, hiring managers, potential collaborators in analytics/data science

---

## 2. UI/UX Specification

### Layout Structure

**Page Sections (vertical scroll):**
1. Hero Section - Full viewport height
2. About Section - Full viewport height
3. Skills Section - Auto height with grid
4. Projects Section - Auto height with grid
5. Contact Section - Full viewport height
6. Footer - Minimal

**Responsive Breakpoints:**
- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px

### Visual Design

**Color Palette:**
- Background Primary: `#0a0a0f` (deep black)
- Background Secondary: `#12121a` (dark charcoal)
- Background Tertiary: `#1a1a25` (slightly lighter)
- Accent Primary: `#00d4ff` (vibrant cyan)
- Accent Glow: `#00d4ff` with 0.3 opacity for glows
- Text Primary: `#ffffff`
- Text Secondary: `#a0a0b0`
- Text Muted: `#606070`
- Card Background: `rgba(26, 26, 37, 0.6)` (glassmorphism)
- Card Border: `rgba(0, 212, 255, 0.15)`

**Typography:**
- Headings: "Outfit", sans-serif (Google Font) - weights 600, 700
- Body: "DM Sans", sans-serif (Google Font) - weights 400, 500
- Hero Name: 4rem (desktop), 2.5rem (mobile)
- Section Titles: 2.5rem (desktop), 1.75rem (mobile)
- Body Text: 1rem
- Small Text: 0.875rem

**Spacing System:**
- Section Padding: 100px vertical (desktop), 60px (mobile)
- Container Max Width: 1200px
- Card Padding: 32px
- Element Gap: 24px

**Visual Effects:**
- Glassmorphism: backdrop-filter blur(12px), semi-transparent backgrounds
- Glow Effects: box-shadow with accent color, spread radius
- Gradient Overlays: Subtle radial gradients from accent color
- Noise Texture: SVG noise overlay for depth

### Components

**1. Navigation Bar**
- Fixed position, transparent initially, solid on scroll
- Logo/Name on left, nav links on right
- Mobile: hamburger menu
- Hover: accent color underline animation

**2. Hero Section**
- Full viewport height with centered content
- Animated gradient background with subtle movement
- Large name with glow effect
- Tagline with typewriter or fade-in animation
- Scroll indicator at bottom (animated chevron)
- Floating geometric shapes in background (subtle)

**3. About Section**
- Two-column layout (text + visual)
- Profile card with glassmorphism
- Key stats: Warwick MSc, 3+ years experience, location
- Animated skill tags

**4. Skills Section**
- Grid of skill cards (2-3 columns desktop, 1-2 mobile)
- Each card: icon, skill name, proficiency indicator
- Hover: lift effect with glow border
- Skills: Python, SQL, R, Tableau, Power BI, Excel, VBA

**5. Projects Section**
- Grid of project cards (2 columns desktop, 1 mobile)
- Each card: project title, description, tags
- Glassmorphism effect
- Hover: scale up with enhanced glow

**6. Contact Section**
- Centered layout
- Large heading with accent color
- Contact links with icon buttons
- Email: ayan.nazm@warwick.ac.uk
- LinkedIn: linkedin.com/in/ayannazm
- Hover effects on links

**7. Footer**
- Minimal: copyright, subtle accent line

### Animations

**Page Load:**
- Staggered fade-in for hero elements (0.1s delay between)
- Navigation slides down from top

**Scroll Animations:**
- Sections fade in and slide up on scroll (IntersectionObserver)
- Skill cards stagger in

**Hover States:**
- Buttons/links: color change + subtle glow
- Cards: translateY(-8px) + enhanced glow
- Icons: scale(1.1) + color shift

**Background:**
- Subtle animated gradient mesh (CSS only)
- Floating particles or shapes (CSS keyframes)

---

## 3. Functionality Specification

### Core Features
- Smooth scroll navigation
- Responsive design (mobile-first)
- Animated section reveals on scroll
- Interactive skill cards
- Project card hover effects
- Contact links (mailto, LinkedIn URL)

### User Interactions
- Click nav links: smooth scroll to section
- Hover cards: visual feedback
- Click contact: open email client / LinkedIn profile
- Mobile menu toggle

### Data Handling
- Static content (no backend)
- All data embedded in HTML

### Edge Cases
- Graceful degradation without JavaScript (basic functionality)
- Fallback fonts if Google Fonts fail
- Reduced motion support (@media prefers-reduced-motion)

---

## 4. Acceptance Criteria

1. Page loads without errors
2. All sections visible and properly styled
3. Dark theme with cyan accent consistently applied
4. Glassmorphism effects visible on cards
5. Animations smooth (60fps)
6. Responsive on mobile (375px), tablet (768px), desktop (1200px+)
7. All links functional (email, LinkedIn)
8. Navigation works correctly
9. Hero animation plays on load
10. Skills and Projects display correctly with descriptions