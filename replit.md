# MedBook - Doctor Booking Platform

## Overview

MedBook is a comprehensive healthcare platform that connects patients with doctors through an intuitive booking system. The application supports multiple user roles (patients, doctors, and admin) with role-specific dashboards and functionality. Built as a full-stack web application, it provides features for doctor discovery, appointment scheduling, payment processing, reviews, and administrative management.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: React Context API for global state (auth, app state) with React Query for server state management
- **UI Components**: Radix UI primitives with shadcn/ui design system for consistent, accessible components
- **Styling**: Tailwind CSS with custom design tokens and CSS variables for theming
- **Form Handling**: React Hook Form with Zod for validation and type safety
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript for full-stack type safety
- **API Design**: RESTful API with JSON responses
- **Middleware**: Custom logging, error handling, and request parsing middleware
- **Development**: Hot module replacement with Vite integration for seamless development experience

### Data Storage Solutions
- **Primary Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Schema Management**: Drizzle Kit for migrations and schema management
- **Fallback Storage**: In-memory storage implementation for development/testing scenarios

### Authentication and Authorization
- **Primary Auth**: Firebase Authentication (Project: drlink-237a0) for secure user management
- **Social Login**: Google OAuth integration through Firebase (configured and ready)
- **Session Management**: Firebase Auth tokens with backend user synchronization via /api/auth/firebase endpoint
- **Role-based Access**: Three user roles (patient, doctor, admin) with protected routes and role-specific UI components
- **Firebase Config**: Complete configuration with real project credentials (updated: 2025-08-10)

### External Service Integrations
- **Payment Processing**: Stripe integration for handling appointment payments (with mock payment flows for development)
- **File Storage**: Firebase Storage for profile images and document uploads
- **Real-time Features**: Prepared for push notifications through Expo Notifications (mobile-ready architecture)

### Key Design Patterns
- **Component Architecture**: Functional components with custom hooks for reusable logic
- **Error Handling**: Centralized error boundaries and graceful fallbacks
- **Data Fetching**: React Query for caching, synchronization, and optimistic updates
- **Type Safety**: End-to-end TypeScript with shared schemas between frontend and backend
- **Responsive Design**: Mobile-first approach with bottom navigation and mobile-optimized layouts
- **Progressive Enhancement**: Core functionality works without JavaScript, enhanced with interactive features

## External Dependencies

### Core Framework Dependencies
- **React Ecosystem**: React, React DOM, React Query for state management and data fetching
- **TypeScript**: Full-stack type safety with shared type definitions
- **Vite**: Modern build tool with HMR and optimized production builds

### UI and Styling
- **Radix UI**: Comprehensive set of accessible, unstyled UI primitives
- **Tailwind CSS**: Utility-first CSS framework with custom design system
- **Lucide React**: Consistent icon library with tree-shaking support
- **Class Variance Authority**: Type-safe styling variants for components

### Backend Infrastructure
- **Express.js**: Web application framework for Node.js
- **Drizzle ORM**: TypeScript ORM with excellent PostgreSQL support
- **Neon Database**: Serverless PostgreSQL database provider

### Authentication and Security
- **Firebase**: Authentication, user management, and file storage
- **Zod**: Runtime type validation and schema definition

### Payment Processing
- **Stripe**: Payment processing with React Stripe.js integration
- **Mock Payments**: Development-friendly payment simulation

### Development and Deployment
- **Replit**: Cloud-based development environment with live deployment
- **ESBuild**: Fast JavaScript bundler for production builds
- **PostCSS**: CSS processing pipeline with Autoprefixer

### Utility Libraries
- **Date-fns**: Comprehensive date manipulation library
- **Wouter**: Lightweight client-side routing
- **React Hook Form**: Performant form library with minimal re-renders
- **clsx/cn**: Conditional className utilities for dynamic styling