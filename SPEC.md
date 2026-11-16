# AIAPGET Prep - Ayurveda Study App Specification

## Project Overview

**Project Name:** AIAPGET Prep - Ayurvedic Medical Exam Preparation Platform
**Type:** Web Application (PWA)
**Core Functionality:** A comprehensive preparation platform for Ayurveda students preparing for AIAPGET (All India Ayush Postgraduate Entrance Test)
**Target Users:** BAMS graduates, Ayurveda students preparing for PG entrance exams

---

## UI/UX Specification

### Layout Structure

**Pages:**
1. **Landing/Home** - Welcome, quick stats, featured content
2. **Dashboard** - Progress tracking, study planner, recent activity
3. **Video Library** - Full-length lectures and short reels
4. **Mnemonics** - Memory aids and quick revision notes
5. **Test Series** - Mock tests, practice questions, results
6. **Guidance** - Study plan, syllabus, exam tips
7. **Profile** - User settings, progress stats

**Responsive Breakpoints:**
- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px

### Visual Design

**Color Palette:**
- Primary: `#1B4332` (Deep Ayurvedic Green)
- Primary Light: `#2D6A4F` (Forest Green)
- Secondary: `#B08968` (Saffron/Maroon accent - traditional Ayurveda)
- Accent: `#D4A373` (Gold highlights)
- Background: `#F8F9FA` (Off-white)
- Card Background: `#FFFFFF`
- Text Primary: `#212529`
- Text Secondary: `#6C757D`
- Success: `#40916C`
- Warning: `#E9C46A`
- Error: `#E76F51`

**Typography:**
- Headings: 'Playfair Display', serif (elegant, traditional feel)
- Body: 'Source Sans Pro', sans-serif (clean, readable)
- Hindi/Sanskrit text: 'Noto Sans Devanagari', sans-serif

**Spacing System:**
- Base unit: 8px
- Section padding: 48px (desktop), 24px (mobile)
- Card padding: 24px
- Component gap: 16px

**Visual Effects:**
- Card shadows: `0 4px 20px rgba(27, 67, 50, 0.08)`
- Hover lift: `transform: translateY(-4px)`
- Smooth transitions: 0.3s ease
- Subtle gradient overlays on hero sections

### Components

**Navigation:**
- Bottom navigation on mobile (5 tabs)
- Sidebar navigation on desktop
- Active state: filled icon + primary color

**Cards:**
- Video card (thumbnail, duration, title, subject tag)
- Mnemonic card (title, category, preview, save button)
- Test card (title, questions, time, status)
- Stat card (icon, value, label, trend)

**Buttons:**
- Primary: Filled with primary color
- Secondary: Outlined
- Icon buttons: Circular with hover effect

**Forms:**
- Floating labels
- Validation states
- Custom file upload with drag-drop

---

## Functionality Specification

### 1. Video Library System

**Full-Length Videos:**
- Upload functionality (drag-drop or click)
- Supported formats: MP4, MKV, WebM
- Video metadata: title, subject, chapter, duration
- Progress tracking (resume where left off)
- Playback speed controls (0.5x, 1x, 1.25x, 1.5x, 2x)
- Picture-in-picture support

**Short Reels (TikTok-style):**
- Vertical video format
- Swipe navigation
- Quick 30-60 second clips
- Category filters (Anatomy, Pharmacology, Clinical, etc.)

**Subject Categories:**
- Kayachikitsa (Medicine)
- Shalya Tantra (Surgery)
- Shalakya Tantra (ENT & Ophthalmology)
- Prasuti Tantra & Stri Roga (Gynecology)
- Kaumarbhritya (Pediatrics)
- Charaka Samhita
- Sushruta Samhita
- Ashtanga Hridayam
- Dravyaguna (Pharmacology)
- Rasa Shastra (Alchemy)
- Basic Principles (Padartha Vigyan)

### 2. Mnemonics System

**Features:**
- Create mnemonics with title, content, category
- Rich text editor for formatting
- Image upload support
- Tag-based organization
- Search and filter
- Spaced repetition reminders
- Favorite/bookmark system

**Categories:**
- Drug names & formulations
- Anatomical landmarks
- Clinical presentations
- Differential diagnoses
- Sanskrit terms & definitions

### 3. Professional Dashboard

**Stats Display:**
- Study hours today/week/month
- Videos watched count
- Tests completed
- Current streak
- Accuracy percentage

**Progress Tracking:**
- Subject-wise completion
- Weak areas identification
- Performance trends graph
- Daily/weekly goals

**Quick Actions:**
- Resume last video
- Continue test
- Quick quiz
- Add mnemonic

### 4. Guidance Section

**Study Planner:**
- Day-wise schedule
- Subject rotation
- Revision calendar
- Custom plan creation

**Content:**
- Complete syllabus (all 18 subjects)
- Important topics highlighted
- Previous year paper analysis
- Exam pattern & marking scheme
- Time management tips
- Recommended books list

### 5. Test Series

**Test Types:**
- Chapter-wise tests
- Subject-wise tests
- Full-length mock tests
- Previous year papers
- Quick practice (10 questions)

**Features:**
- Timer with auto-submit
- Bookmark questions for review
- Detailed solutions
- Performance analytics
- Comparative analysis
- Rank prediction

**Question Types:**
- Multiple choice (single answer)
- Multiple correct answers
- Match the column
- True/False

---

## Technical Specification

### Frontend
- React 18 with Vite
- React Router for navigation
- Zustand for state management
- Framer Motion for animations
- React Player for video
- Chart.js for analytics

### Data Storage
- LocalStorage for user preferences
- IndexedDB for video cache
- JSON-based mock data structure

### PWA Features
- Service worker for offline support
- Installable on mobile
- Push notifications (future)

---

## Acceptance Criteria

1. ✅ User can navigate between all 7 main sections
2. ✅ Video upload works with preview
3. ✅ Videos play with controls
4. ✅ Reels have swipe navigation
5. ✅ Mnemonics can be created, edited, deleted
6. ✅ Dashboard shows accurate stats
7. ✅ Test series has working quiz interface
8. ✅ Guidance section displays syllabus
9. ✅ Responsive on mobile and desktop
10. ✅ Smooth animations and transitions