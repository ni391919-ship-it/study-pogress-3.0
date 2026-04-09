# StudyFlow - Personal Study Tracker

## Concept & Vision

StudyFlow is a vibrant, motivating study companion that transforms mundane academic tracking into an engaging daily ritual. It combines the satisfaction of progress tracking with the organization of a class schedule and the creativity of note-taking—all wrapped in a dynamic, animated interface that responds to your every interaction with delightful micro-animations. The app feels alive, encouraging you to return and continue your learning journey.

## Design Language

**Aesthetic Direction:** Neo-brutalist meets soft gradients—bold geometric shapes with playful rounded corners, layered depth with soft shadows, and vibrant accent colors that shift based on study sessions.

**Color Palette:**
- Primary: `#6366F1` (Indigo) - Main actions, headers
- Secondary: `#EC4899` (Pink) - Accents, highlights
- Accent: `#10B981` (Emerald) - Success states, completed items
- Background: `#0F172A` (Dark slate) - Base background
- Surface: `#1E293B` (Slate) - Cards and elevated surfaces
- Text Primary: `#F8FAFC` (Light)
- Text Secondary: `#94A3B8` (Muted)
- Gradient 1: `linear-gradient(135deg, #6366F1, #EC4899)`
- Gradient 2: `linear-gradient(135deg, #10B981, #34D399)`

**Typography:**
- Headings: "Plus Jakarta Sans" (Google Fonts) - Bold, modern
- Body: "Inter" (Google Fonts) - Clean, readable
- Sizes: Display 48px, H1 32px, H2 24px, Body 16px, Small 14px

**Spatial System:**
- Base unit: 4px
- Card padding: 24px
- Section gaps: 32px
- Border radius: 16px (cards), 12px (buttons), 8px (inputs)

**Motion Philosophy:**
- Entrance: Elements fade-slide in from bottom with stagger (300ms, 100ms delay between items)
- Interactions: Scale on hover (1.02), press effect on click (0.98), spring-based easing
- Progress: Animated fills with glow pulse on completion
- Transitions: 200ms for micro-interactions, 400ms for larger state changes
- Floating elements: Subtle continuous float animation on decorative elements

**Visual Assets:**
- Icons: Lucide React icons
- Decorative: Animated gradient orbs floating in background
- Progress indicators: Custom animated circular progress bars

## Layout & Structure

**Page Structure:**
- Single-page app with tab navigation at bottom (mobile) / sidebar (desktop)
- Three main sections: Dashboard, Schedule, Notes
- Floating action button for quick note capture
- Animated background with floating gradient orbs

**Visual Pacing:**
- Hero section on Dashboard with motivational greeting and daily progress ring
- Card-based content below with staggered entrance
- Schedule presented as a timeline with visual day indicators
- Notes as a masonry-style card grid

**Responsive Strategy:**
- Mobile-first with bottom tab navigation
- Tablet: 2-column grid for notes
- Desktop: Sidebar navigation + 3-column content area

## Features & Interactions

### Dashboard
- Daily greeting with animated text reveal
- Circular progress ring showing daily study goal completion
- Quick stats cards: Today's study time, Classes remaining, Notes count
- Current streak display with flame animation
- Quick add study session button

### Schedule
- Weekly calendar view with animated day transitions
- Add/edit/delete class items with smooth animations
- Color-coded class cards with subject icons
- Time slot visualization
- Empty state: Illustrated prompt to add first class

### Notes
- Grid of note cards with preview text
- Create note modal with rich text area
- Edit/delete notes with confirmation
- Search/filter notes
- Tags for categorization
- Animated card entrance on creation

### Study Progress
- Add study sessions with subject, duration, date
- Progress history with animated charts
- Subject-wise breakdown
- Goals setting (daily/weekly study hours)

## Component Inventory

### Navigation
- Desktop: Fixed sidebar with icons and labels
- Mobile: Fixed bottom bar with icons
- States: Default (muted), Active (gradient background with glow)

### Cards
- Base: Surface color, rounded corners, soft shadow
- Hover: Lift effect (translateY -4px), enhanced shadow
- Interactive: Scale 1.02 on hover, 0.98 on press

### Progress Ring
- Animated SVG circle with gradient stroke
- Glow effect on completion
- Percentage text in center with count-up animation

### Buttons
- Primary: Gradient background, white text, hover glow
- Secondary: Surface background, border, hover fill
- Icon buttons: Circular, hover scale

### Input Fields
- Floating label animation
- Focus ring with gradient border
- Error state with shake animation

### Modal
- Backdrop blur with fade-in
- Content slides up from bottom with spring animation
- Close button with rotate on hover

### Note Cards
- Title, preview, timestamp, tags
- Hover: Lift and subtle glow
- Delete: Confirm modal with slide-out animation

## Technical Approach

- **Framework:** React 18 + TypeScript + Vite
- **Styling:** Tailwind CSS with custom animations
- **State:** React useState/useReducer for local state
- **Icons:** Lucide React
- **Animations:** CSS animations + Tailwind animate utilities
- **Data:** LocalStorage for persistence
- **Unique IDs:** Date.now() for simplicity
