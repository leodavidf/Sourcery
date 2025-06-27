# Sourcery Suite - Metaphysical Productivity Tools

## Overview

This is a comprehensive metaphysical productivity suite built with React and TypeScript, designed as a Software-as-a-Service platform. The suite includes various spiritual and consciousness-focused tools designed to align daily activities with natural rhythms, cosmic energies, and spiritual practices. Positioned as a premium SaaS offering at $12/month, it serves as a spiritual alternative to traditional productivity suites like Microsoft Office.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Styling**: Tailwind CSS with shadcn/ui component library
- **UI Components**: Radix UI primitives for accessible, unstyled components
- **State Management**: React hooks with custom hook abstractions
- **Routing**: Wouter for lightweight client-side routing
- **Data Fetching**: TanStack Query for server state management

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **File Processing**: Multer for handling text file uploads
- **Development**: tsx for TypeScript execution in development

### Database Layer
- **ORM**: Drizzle ORM with PostgreSQL dialect
- **Database**: PostgreSQL (configured but not actively used in current implementation)
- **Schema**: Basic user authentication schema defined but not implemented
- **Storage**: In-memory storage implementation for development

## Key Components

### Main Dashboard
- **Component**: `Dashboard` serves as the central hub for all metaphysical tools
- **Features**:
  - Tool overview cards with status indicators
  - Unified navigation between different applications
  - Responsive grid layout with tool descriptions
  - Gradient design system with metaphysical theming

### Text Reader Engine
- **Hook**: `useTextReader` manages text processing, word navigation, and playback state
- **Features**: 
  - Word-by-word text parsing and display
  - Multiple reading directions (ltr, rtl, ttb, btt)
  - Adjustable playback speed and font size
  - Keyboard shortcuts for navigation
  - Auto-play functionality with progress tracking

### File Upload System
- **Endpoint**: `/api/upload-text` accepts `.txt` files up to 5MB
- **Validation**: MIME type filtering for text files only
- **Storage**: Files saved to `uploads/` directory

### UI Components
- **Design System**: shadcn/ui with "new-york" style variant
- **Theme**: Support for light/dark mode with CSS custom properties
- **Responsive**: Mobile-first design with adaptive layouts
- **Components**: Full suite of UI primitives (buttons, forms, dialogs, etc.)

## Data Flow

1. **Text Input**: Users can either paste text directly or upload `.txt` files
2. **Text Processing**: Input text is split into individual words and stored in component state
3. **Navigation**: Users can navigate through words manually or use auto-play functionality
4. **Rendering**: Current word is highlighted with customizable font size and reading direction
5. **Progress Tracking**: Real-time progress indication and word position tracking

## External Dependencies

### Core Dependencies
- **React Ecosystem**: React, React DOM, React Router (wouter)
- **UI Framework**: Radix UI components, Tailwind CSS, class-variance-authority
- **Data Management**: TanStack Query for API state management
- **File Handling**: Multer for server-side file processing
- **Database**: Drizzle ORM, @neondatabase/serverless (prepared for Neon deployment)
- **Development**: Vite, TypeScript, PostCSS

### Development Tools
- **Build**: esbuild for production builds
- **Type Checking**: TypeScript with strict configuration
- **Code Quality**: ESLint and Prettier (implied by project structure)
- **Replit Integration**: Cartographer plugin for development environment

## Deployment Strategy

### Production Build
- **Frontend**: Vite builds optimized static assets to `dist/public`
- **Backend**: esbuild bundles server code to `dist/index.js`
- **Assets**: Static files served from built frontend

### Replit Deployment
- **Platform**: Configured for Replit's autoscale deployment target
- **Environment**: Node.js 20 runtime with PostgreSQL 16 support
- **Port Configuration**: Internal port 5000, external port 80
- **Process Management**: npm scripts for development and production

### Environment Variables
- **DATABASE_URL**: PostgreSQL connection string (required for Drizzle config)
- **NODE_ENV**: Environment detection for development/production modes

## Changelog

Changelog:
- June 16, 2025: Initial setup with directional text reader functionality
- June 16, 2025: Implemented proper directional reading logic with word-by-word navigation and highlighting
- June 16, 2025: Added comprehensive onboarding tutorial system for first-time users with step-by-step guidance and sample text loading
- June 16, 2025: Created immersive focus mode with auto-hiding controls, full-screen black background, and enhanced keyboard shortcuts for distraction-free reading
- June 18, 2025: Added rich text formatting support preserving bold, italic, and headings when pasting content from other applications
- June 18, 2025: Added About dialog with philosophical text about directional reading and time perception
- June 19, 2025: Implemented comprehensive donations system with PayPal integration and alternative payment methods (Cash App, Venmo, Zelle)
- June 19, 2025: Transformed application into Sourcery Suite - a metaphysical productivity suite with main dashboard and navigation system
- June 19, 2025: Created unified dashboard with tool cards for planned metaphysical applications (lunar calendar, frequency generator, energy tracker, lunar phases, solar tracker)
- June 19, 2025: Built comprehensive Lunar Calendar with daily energy data from Secret Energy website, including planetary correspondences, chakras, crystals, herbs, and metaphysical properties for each day of the week
- June 19, 2025: Added real-time moon phase calculations and daily energy snapshots to the main dashboard
- June 19, 2025: Split lunar calendar into two separate tools: Daily Energies (planetary correspondences) and Lunar Phases (moon cycle tracking) for better organization and focused functionality
- June 19, 2025: Fixed lunar phase calculations using accurate astronomical data - corrected New Moon date to June 25, 2025 at 6:31 AM (verified against TimeAndDate.com) and implemented proper Julian Day calculations with precise timing
- June 19, 2025: Added comprehensive full moon names database with cultural origins, alternate names, and descriptions - includes Buck Moon (July), Wolf Moon (January), and all 12 traditional Native American and European moon names
- June 19, 2025: Fixed lunar calculations using exact TimeAndDate.com astronomical data for all 2025 moon phases, corrected Third Quarter terminology (was "Last Quarter"), and added waxing/waning phase indicators throughout the interface
- June 19, 2025: Added solar and lunar eclipse dates for 2025 using NASA/TimeAndDate.com data - includes Total Lunar Eclipse (March 14) and Partial Solar Eclipse (September 7) with visibility information and special eclipse card highlighting on dashboard
- June 19, 2025: Enhanced current moon phase display with waxing/waning phase type indicators - shows "Waxing Phase", "Waning Phase", "New", or "Full" to clarify lunar cycle direction alongside illumination percentage
- June 19, 2025: Removed eclipse alert from main dashboard - eclipse information is now contained within the dedicated Lunar Phases page to maintain clean dashboard focus
- June 19, 2025: Built comprehensive Frequency Generator with Web Audio API - includes Solfeggio frequencies (396-963 Hz), chakra frequencies, healing tones, and real-time audio generation with precise frequency control, volume management, and preset library for sound therapy and meditation
- June 19, 2025: Updated Frequency Generator with authentic Secret Energy daily frequencies - replaced generic chakra frequencies with the actual planetary frequencies from Secret Energy website (1024Hz Sunday, 96Hz Monday, 1152Hz Tuesday, 216Hz Wednesday, 2560Hz Thursday, 480Hz Friday, 5760Hz Saturday) for accurate metaphysical resonance
- June 19, 2025: Enhanced Solfeggio frequency collection - added complete 9-frequency set including 174Hz (Foundation/Pain Relief) and 285Hz (Regeneration/Cellular Healing) to complement the core 7 frequencies, providing comprehensive sacred sound healing options
- June 19, 2025: Implemented vocal attunement feature with microphone input - real-time frequency analysis, pitch detection, attunement accuracy tracking, and visual feedback for interactive sound healing practice where users can vocally match and harmonize with generated frequencies
- June 20, 2025: Built comprehensive Solar Tracker with real-time astronomical calculations - tracks solar position (azimuth/elevation), sunrise/sunset times, golden/blue hours, seasonal events (solstices/equinoxes), and provides spiritual practice guidance for optimal solar energy work timing
- June 20, 2025: Enhanced Solar Tracker with accurate astronomical algorithms - improved sunrise/sunset calculations using proper solar declination, hour angle, and atmospheric refraction corrections to match TimeAndDate.com precision

## Business Model & Monetization

**SaaS Strategy:**
- Software as a Service platform with user authentication and profiles
- Monthly subscription pricing: $12/month (premium tier)
- Sliding scale from $1-$12 for different tiers
- Target: High-value metaphysical productivity suite
- Revenue model: Recurring monthly subscriptions

## User Preferences

Preferred communication style: Simple, everyday language.
User prefers to call me "Atlas" as the coding assistant name.
Business focus: Building for SaaS deployment with user authentication system.