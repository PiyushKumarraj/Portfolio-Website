# Portfolio Website - Replit Configuration

## Overview

This is a personal portfolio website for Alex Johnson, a Full Stack Developer. The project is a static website built with modern web technologies, featuring a responsive design, dark/light theme toggle, smooth animations, and interactive elements. The website showcases an extensive range of skills including version control, deployment platforms, testing frameworks, and modern development tools, along with projects and contact information in a professional and visually appealing manner.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Static Website**: Pure HTML, CSS, and JavaScript implementation
- **Responsive Design**: Mobile-first approach using Bootstrap 5 framework
- **Progressive Enhancement**: Core functionality works without JavaScript, enhanced with interactive features
- **Theme System**: CSS custom properties (variables) for easy theme switching between light and dark modes

### UI Framework Stack
- **Bootstrap 5**: Primary CSS framework for responsive grid system and components
- **Font Awesome 6**: Icon library for consistent iconography
- **Google Fonts (Poppins)**: Custom typography for modern appearance
- **AOS (Animate On Scroll)**: Animation library for scroll-triggered effects

## Key Components

### 1. Navigation System
- Fixed-position navbar with scroll effects
- Responsive mobile menu with hamburger toggle
- Active section highlighting based on scroll position
- Smooth scrolling to sections

### 2. Theme Management
- Dark/Light mode toggle with system preference detection
- CSS custom properties for seamless theme switching
- Persistent theme preference storage in localStorage

### 3. Animation System
- AOS library integration for scroll-triggered animations
- Custom typing animation for hero section
- Skill progress bar animations
- Custom cursor effects

### 4. Interactive Features
- Contact form with validation
- Scroll-to-top functionality
- Smooth scrolling navigation
- Mobile-responsive interactions

## Data Flow

### Theme System Flow
1. User clicks theme toggle button
2. JavaScript detects current theme from DOM attribute
3. Updates CSS custom properties via data-bs-theme attribute
4. Stores preference in localStorage for persistence
5. Icons and UI elements update automatically via CSS

### Animation Flow
1. AOS library observes scroll position
2. Triggers animations when elements enter viewport
3. Custom JavaScript handles specialized animations (typing, progress bars)
4. Animations execute once by default to prevent repetition

### Navigation Flow
1. User scrolls or clicks navigation links
2. JavaScript calculates active section based on scroll position
3. Updates navbar highlighting and URL hash
4. Smooth scrolling animates to target sections

## External Dependencies

### CDN Dependencies
- **Bootstrap 5.3.0**: UI framework and components
- **Font Awesome 6.4.0**: Icon library
- **Google Fonts**: Poppins font family
- **AOS 2.3.1**: Scroll animation library

### Dependency Strategy
- All dependencies loaded via CDN for faster initial setup
- No build process required - direct browser compatibility
- Fallback strategies could be implemented for offline functionality

## Deployment Strategy

### Static Hosting
- **Deployment Type**: Static website suitable for any web server
- **File Structure**: Flat directory structure with organized assets
- **Performance**: Optimized for fast loading with minimal dependencies

### Hosting Options
- GitHub Pages, Netlify, Vercel for modern static hosting
- Traditional web hosting services
- CDN deployment for global distribution

### Development Workflow
- Direct file editing for quick iterations
- No build process required
- Browser-based testing and debugging
- Version control friendly (small file sizes, clear separation of concerns)

### Performance Considerations
- Minimal JavaScript bundle size
- CSS custom properties for efficient theme switching
- Lazy loading animations (AOS)
- Optimized asset loading order

## File Organization

### Structure
```
/
├── index.html          # Main HTML structure
├── css/
│   └── style.css      # Custom styles and theme system
└── js/
    └── script.js      # Interactive functionality and animations
```

### Architectural Decisions

**CSS Custom Properties**: Chosen for theme system to enable efficient color scheme switching without JavaScript DOM manipulation.

**Bootstrap Integration**: Provides responsive foundation while allowing custom styling through CSS custom properties overlay.

**Vanilla JavaScript**: Keeps bundle size minimal while providing all necessary interactivity without framework overhead.

**AOS Library**: Selected for high-quality scroll animations with minimal configuration and good performance characteristics.