# SkillBridge Mentorship Platform - Design Documentation

## 📋 Overview

This document provides comprehensive design specifications for the SkillBridge mentorship platform. All HTML prototypes have been created using Tailwind CSS for pixel-perfect reference when creating Figma designs.

## 🎨 Design System

### Color Palette

#### Primary Colors
- **Blue 600**: #2563eb (Primary buttons, active states)
- **Blue 500**: #3b82f6 (Hover states)
- **Blue 100**: #dbeafe (Light backgrounds, badges)

#### Secondary Colors
- **Indigo 600**: #4f46e5 (Secondary accent)
- **Indigo 500**: #6366f1 (Secondary hover)
- **Indigo 100**: #e0e7ff (Secondary light)

#### Status Colors
- **Green 500**: #10b981 (Success, available status)
- **Green 100**: #dcfce7 (Success backgrounds)
- **Red 500**: #ef4444 (Error, unavailable)
- **Red 100**: #fee2e2 (Error backgrounds)
- **Yellow 500**: #eab308 (Warning, busy status)
- **Yellow 100**: #fef3c7 (Warning backgrounds)
- **Yellow 400**: #facc15 (Star ratings)

#### Neutral Colors
- **Gray 900**: #111827 (Primary text)
- **Gray 800**: #1f2937 (Secondary text)
- **Gray 700**: #374151 (Tertiary text)
- **Gray 600**: #4b5563 (Muted text)
- **Gray 500**: #6b7280 (Placeholder text)
- **Gray 300**: #d1d5db (Borders)
- **Gray 200**: #e5e7eb (Light borders)
- **Gray 100**: #f3f4f6 (Light backgrounds)
- **Gray 50**: #f9fafb (Page backgrounds)

### Typography

#### Font Stack
- **Primary Font**: System fonts (Tailwind default)
- **Fallback**: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif

#### Font Sizes & Usage
- **text-4xl** (36px): Page titles, hero headings
- **text-3xl** (30px): Section headings
- **text-2xl** (24px): Card titles, subsection headings
- **text-xl** (20px): Component titles
- **text-lg** (18px): Emphasized text
- **text-base** (16px): Body text (default)
- **text-sm** (14px): Secondary text, labels
- **text-xs** (12px): Captions, metadata

#### Font Weights
- **font-bold** (700): Main headings, important text
- **font-semibold** (600): Section headings, card titles
- **font-medium** (500): Button text, emphasized content
- **font-normal** (400): Body text (default)

### Spacing System

Based on Tailwind's spacing scale (4px base unit):
- **1**: 4px
- **2**: 8px
- **3**: 12px
- **4**: 16px
- **6**: 24px
- **8**: 32px
- **12**: 48px
- **16**: 64px
- **24**: 96px

### Border Radius
- **rounded**: 4px (small elements)
- **rounded-lg**: 8px (cards, buttons)
- **rounded-full**: 50% (avatars, pills)

### Shadows
- **shadow-sm**: Subtle elevation for cards
- **shadow-md**: Hover states, dropdowns
- **shadow-lg**: Modals, overlays

## 🧩 Component Library

### Buttons

#### Primary Button
```html
<button class="bg-blue-600 hover:bg-blue-700 text-white font-medium py-2 px-4 rounded-lg transition-colors">
  Primary Button
</button>
```

#### Secondary Button
```html
<button class="bg-white hover:bg-gray-50 text-gray-700 font-medium py-2 px-4 rounded-lg border border-gray-300 transition-colors">
  Secondary Button
</button>
```

#### Ghost Button
```html
<button class="bg-gray-100 hover:bg-gray-200 text-gray-700 font-medium py-2 px-4 rounded-lg transition-colors">
  Ghost Button
</button>
```

#### Button Sizes
- **Small**: `py-1.5 px-3 text-sm`
- **Medium**: `py-2 px-4` (default)
- **Large**: `py-3 px-6`

### Form Elements

#### Input Field
```html
<input type="text" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent" placeholder="Enter text">
```

#### Select Dropdown
```html
<select class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
  <option>Choose an option</option>
</select>
```

#### Textarea
```html
<textarea class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent" rows="3"></textarea>
```

### Cards

#### Basic Card
```html
<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-6">
  <h3 class="text-lg font-semibold text-gray-900 mb-2">Card Title</h3>
  <p class="text-gray-600">Card content</p>
</div>
```

#### Feature Card with Icon
```html
<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-6 hover:shadow-md transition-shadow">
  <div class="flex items-center mb-4">
    <div class="bg-blue-100 p-2 rounded-lg">
      <i class="fas fa-star text-blue-600"></i>
    </div>
    <h3 class="text-lg font-semibold text-gray-900 ml-3">Feature Title</h3>
  </div>
  <p class="text-gray-600">Feature description</p>
</div>
```

#### Stat Card
```html
<div class="bg-gradient-to-r from-blue-500 to-indigo-600 rounded-lg shadow-sm p-6 text-white">
  <h3 class="text-2xl font-bold mb-1">$2,345</h3>
  <p class="text-blue-100">Total Earnings</p>
</div>
```

### Badges & Status Tags

#### Status Badges
```html
<span class="bg-green-100 text-green-800 text-sm font-medium px-2.5 py-0.5 rounded-full">Available</span>
<span class="bg-red-100 text-red-800 text-sm font-medium px-2.5 py-0.5 rounded-full">Busy</span>
<span class="bg-yellow-100 text-yellow-800 text-sm font-medium px-2.5 py-0.5 rounded-full">Draft</span>
```

#### Skill Tags
```html
<span class="bg-gray-100 text-gray-700 text-sm font-medium px-3 py-1 rounded-lg">JavaScript</span>
<span class="bg-blue-100 text-blue-800 text-sm font-medium px-3 py-1 rounded-lg">React</span>
```

### Navigation

#### Main Navigation
```html
<nav class="hidden md:flex space-x-8">
  <a href="#" class="text-blue-600 font-medium">Active Link</a>
  <a href="#" class="text-gray-500 hover:text-gray-700">Inactive Link</a>
</nav>
```

#### Breadcrumbs
```html
<nav class="flex items-center space-x-2 text-sm">
  <a href="#" class="text-gray-500 hover:text-gray-700">Home</a>
  <i class="fas fa-chevron-right text-gray-400"></i>
  <a href="#" class="text-gray-500 hover:text-gray-700">Mentors</a>
  <i class="fas fa-chevron-right text-gray-400"></i>
  <span class="text-gray-900">Profile</span>
</nav>
```

## 📱 Responsive Design

### Breakpoints
- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

### Grid System
- **Mobile**: Single column layouts
- **Tablet**: 2-column grids
- **Desktop**: 3-4 column grids

### Key Responsive Patterns
1. **Navigation**: Hamburger menu on mobile, full nav on desktop
2. **Cards**: Stack vertically on mobile, grid on desktop
3. **Sidebars**: Full width on mobile, sidebar on desktop
4. **Tables**: Horizontal scroll on mobile, full view on desktop

## 🎯 User Experience Patterns

### Mentor Cards
- **Image**: 48px × 48px rounded profile picture
- **Status**: Green (Available), Yellow (Busy), Red (Unavailable)
- **Rating**: 5-star system with review count
- **Skills**: Max 3-4 skill tags visible
- **CTA**: "Book Session" primary button

### Session Booking Flow
1. **Calendar View**: Month view with available dates highlighted
2. **Time Slots**: Grid of available time slots
3. **Confirmation**: Summary with mentor details and pricing
4. **Payment**: Secure payment form (placeholder)

### Dashboard Widgets
- **Stats Cards**: Large numbers with trend indicators
- **Upcoming Sessions**: List with join/cancel actions
- **Recent Activity**: Timeline or feed format
- **Quick Actions**: Prominent buttons for common tasks

### Messaging Interface
- **Conversation List**: Avatar, name, last message preview
- **Chat Window**: Traditional chat bubble layout
- **Online Status**: Real-time presence indicators
- **File Sharing**: Attachment previews and download links

## 🔧 Implementation Notes

### Icons
- **Library**: Font Awesome 6
- **Style**: Filled icons (fas)
- **Usage**: Consistent sizes (text-sm, text-lg, text-xl)

### Animations
- **Transitions**: `transition-colors`, `transition-shadow`
- **Hover Effects**: Subtle scale, color, or shadow changes
- **Loading States**: Skeleton screens or spinner components

### Accessibility
- **Color Contrast**: WCAG AA compliant
- **Focus States**: Visible focus rings on interactive elements
- **Semantic HTML**: Proper heading hierarchy and landmarks
- **Alt Text**: Descriptive alt text for all images

## 📄 File Structure

```
/app/frontend/src/
├── design-system.html      # Complete design system showcase
├── mentor-dashboard.html   # Mentor dashboard prototype
├── mentee-dashboard.html   # Mentee dashboard prototype
├── browse-mentors.html     # Mentor discovery page
├── mentor-profile.html     # Detailed mentor profile
├── booking-flow.html       # Session booking interface
├── messaging.html          # Chat interface
└── DESIGN_DOCUMENTATION.md # This file
```

## 🚀 Getting Started with Figma

1. **Open each HTML file** in your browser to see the live prototypes
2. **Take screenshots** of each screen at different breakpoints
3. **Import to Figma** and trace over the designs
4. **Create components** for reusable elements (buttons, cards, etc.)
5. **Build the design system** using the specifications above
6. **Add interactions** for hover states and transitions

## 💡 Key Features to Highlight

### For Mentors
- **Dashboard**: Earnings, session stats, upcoming bookings
- **Profile Management**: Skills, availability, bio editing
- **Session Management**: Calendar view, session notes
- **Course Creation**: Upload content, set pricing
- **Messaging**: Direct communication with mentees

### For Mentees
- **Discovery**: Search, filter, browse mentors
- **Booking**: Calendar selection, session details
- **Learning**: Course progress, session history
- **Communication**: Direct messaging with mentors
- **Progress Tracking**: Goals, achievements, growth metrics

This design system provides a solid foundation for creating a professional, user-friendly mentorship platform that serves both mentors and mentees effectively.