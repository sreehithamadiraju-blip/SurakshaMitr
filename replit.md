# SurakshaMitr - Smart Tourist Safety Application

## Overview

SurakshaMitr (meaning "Safety Friend" in Hindi) is a comprehensive tourist safety and incident response web application designed to provide tourists with instant access to emergency services, safety information, and digital identification tools. The application features a mobile-first design with emergency SOS functionality, interactive safety maps, real-time alerts, and an AI-powered administrative dashboard for authorities to manage incidents and generate electronic reports.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **Routing**: Wouter for lightweight client-side routing
- **UI Components**: ShadCN/UI components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom design tokens for safety-focused color scheme
- **State Management**: TanStack Query for server state management and local storage for user data persistence
- **Form Handling**: React Hook Form with Zod validation for type-safe form management

### Backend Architecture
- **Server Framework**: Express.js with TypeScript
- **Database Layer**: Drizzle ORM with PostgreSQL using Neon Database serverless driver
- **API Design**: RESTful API endpoints for user management, SOS alerts, safety alerts, and E-FIR generation
- **Development Storage**: In-memory storage with seed data for development and testing

### Data Storage Solutions
- **Primary Database**: PostgreSQL managed through Drizzle ORM
- **Schema Design**: Structured tables for users, SOS alerts, safety alerts, E-FIRs, and emergency contacts
- **Local Storage**: Browser localStorage for user session persistence and offline capability
- **Data Validation**: Zod schemas shared between frontend and backend for consistent validation

### Authentication and Authorization
- **User Registration**: Multi-step onboarding with language selection and identity verification
- **Digital Identity**: QR code-based digital tourist ID system for quick identification
- **Session Management**: localStorage-based session persistence for mobile app-like experience
- **Role-Based Access**: Separate interfaces for tourists and administrative authorities

### Core Features Implementation
- **Emergency SOS System**: One-tap emergency service contact with automatic location sharing
- **Interactive Safety Maps**: Google Maps integration showing risk zones and safe locations
- **Real-time Alerts**: Dynamic alert system for scam warnings, police bulletins, and safety tips
- **Multi-language Support**: Internationalization ready with language selection on onboarding
- **Mobile-First Design**: Bottom navigation and touch-optimized interface for mobile devices

### AI Integration
- **E-FIR Generation**: Google Gemini AI integration for automated Electronic First Information Report creation
- **Document Processing**: Structured report generation from incident details using AI prompts
- **Administrative Tools**: AI-assisted report generation for law enforcement workflows

## External Dependencies

### Third-Party Services
- **Google Gemini AI**: AI-powered E-FIR document generation using @google/genai
- **Google Maps API**: Interactive mapping, location services, and geolocation features
- **QR Code Generation**: External QR code service (QR-Server API) for digital ID generation

### Database and Infrastructure
- **Neon Database**: Serverless PostgreSQL hosting with @neondatabase/serverless driver
- **Drizzle Kit**: Database migration and schema management tooling

### Development and Build Tools
- **Vite**: Modern build tool with React plugin and development server
- **TypeScript**: Type safety across the entire application stack
- **ESBuild**: Fast bundling for production server builds
- **Replit Integration**: Development environment plugins for cartographer and dev banner

### UI and Styling Dependencies
- **Radix UI**: Accessible component primitives for complex UI components
- **Tailwind CSS**: Utility-first CSS framework with custom design system
- **Lucide React**: Icon library for consistent iconography
- **PT Sans Font**: Google Fonts integration for typography

### Utility Libraries
- **date-fns**: Date manipulation and formatting utilities
- **clsx & tailwind-merge**: Conditional CSS class composition
- **nanoid**: Unique ID generation for various application needs