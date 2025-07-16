# Bright Auto Connect - Car Dealership Application

## Overview

This is a full-stack web application for a car dealership called "Bright Auto Connect" that specializes in car sourcing, buying, and selling services. The application features a modern, responsive design with a single-page layout showcasing services, featured cars, testimonials, and contact functionality.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Routing**: Wouter for lightweight client-side routing
- **UI Framework**: Tailwind CSS with shadcn/ui components
- **State Management**: TanStack Query (React Query) for server state management
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon serverless PostgreSQL
- **Session Management**: Express sessions with PostgreSQL store
- **API Pattern**: RESTful API endpoints

### Key Components

#### Database Schema
- **Users**: Authentication and user management
- **Cars**: Vehicle inventory with details like make, model, year, price, mileage
- **Testimonials**: Customer reviews and ratings
- **Contact Messages**: Customer inquiries and service requests
- **Chat Messages**: Real-time chat conversations with automatic agent responses

#### Frontend Components
- **Navigation**: Sticky header with smooth scrolling to sections
- **Hero Section**: Call-to-action with phone and WhatsApp integration
- **About Section**: "Driven by Trust. Built for Convenience" with company promise
- **Services Section**: Display of core business services (auction sourcing, ready-to-go cars, delivery)
- **Featured Cars**: Grid of available vehicles with pricing
- **Testimonials**: Customer feedback display
- **FAQ Section**: Expandable frequently asked questions
- **Contact Form**: Multi-field form with service selection
- **Footer**: Company information and links
- **Chat Box**: Real-time chat widget with auto-responses

#### Storage Layer
- **Abstract Interface**: IStorage interface for data operations
- **Memory Storage**: In-memory implementation for development/testing
- **Database Storage**: PostgreSQL implementation for production

## Data Flow

1. **Client Requests**: Frontend makes API calls using TanStack Query
2. **API Processing**: Express server handles requests and validates data
3. **Database Operations**: Drizzle ORM executes queries against PostgreSQL
4. **Response Handling**: Data is returned to client and cached by React Query
5. **UI Updates**: Components re-render with fresh data

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL connection
- **drizzle-orm**: Type-safe database operations
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Accessible UI primitives
- **react-hook-form**: Form state management
- **zod**: Schema validation
- **tailwindcss**: Utility-first CSS framework

### Development Tools
- **Vite**: Fast build tool and dev server
- **TypeScript**: Static type checking
- **ESLint**: Code linting
- **Prettier**: Code formatting

## Deployment Strategy

### Build Process
1. **Frontend Build**: Vite builds React app to `dist/public`
2. **Backend Build**: ESBuild bundles server code to `dist/index.js`
3. **Database Migration**: Drizzle pushes schema changes to PostgreSQL

### Environment Configuration
- **Development**: Uses tsx for hot reloading
- **Production**: Serves static files and API from single Express server
- **Database**: Requires `DATABASE_URL` environment variable

### Key Features
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Form Validation**: Client and server-side validation with Zod
- **Error Handling**: Comprehensive error boundaries and API error handling
- **Performance**: Optimized with React Query caching and Vite bundling
- **Accessibility**: Built with Radix UI primitives for screen reader support
- **Vibrant Design**: Colorful gradient backgrounds and animations throughout
- **Enhanced Visual Appeal**: Floating animations, hover effects, and modern card designs

## Recent Changes (July 2025)
- **Enhanced Visual Design**: Added vibrant gradient backgrounds to all sections
- **New Auction Cars Section**: Comprehensive pricing table with service tiers
- **Improved Color Scheme**: Added custom CSS variables for orange, purple, pink, and cyan
- **Animation Effects**: Floating animations and hover lift effects throughout
- **Updated Content**: Added detailed auction car pricing from user's price list
- **Enhanced Chat**: More colorful chat widget with improved automated responses
- **Navigation Update**: Added Auction Cars section to navigation menu

The application is designed as a showcase website for a car dealership, emphasizing user experience, professional presentation, and vibrant visual appeal of automotive services.