# WellnessPath - Daily-Journey - ADHD-Friendly Goal Planning

## Overview

WellnessPath is a mobile-first wellness and goal-planning application specifically designed for people with ADHD. The application focuses on helping users track their goals, plan their day, and celebrate their achievements across six key wellness dimensions: Physical, Mental, Social, Financial, Career, and Spiritual.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Styling**: Tailwind CSS with custom CSS variables for ADHD-friendly color schemes
- **UI Components**: Radix UI primitives with shadcn/ui component library
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Mobile-First Design**: Responsive design optimized for mobile devices with bottom navigation

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database serverless PostgreSQL
- **Schema Management**: Drizzle Kit for migrations and schema management
- **API Design**: RESTful API with Express routes

### Key Components

1. **Wellness Dimensions System**
   - Six predefined wellness categories with custom icons and colors
   - Each dimension has associated goals and tasks
   - Visual progress tracking with color-coded indicators

2. **Goal Management**
   - SMART goal structure with target values and deadlines
   - Priority levels (low, medium, high)
   - Status tracking (active, completed, paused)
   - Progress visualization with percentage completion

3. **Task Planning**
   - Daily task scheduling with date/time management
   - Task association with goals and wellness dimensions
   - Completion tracking with achievement celebrations

4. **Progress Tracking**
   - Visual charts and graphs using Recharts
   - Dimension-wise progress analytics
   - Achievement system for motivation

5. **Mobile-First UI**
   - Bottom navigation for easy thumb navigation
   - Floating action buttons for quick task/goal creation
   - Card-based layouts for scannable content
   - ADHD-friendly color palette with high contrast

## Data Flow

1. **User Interaction**: User interacts with React components
2. **State Management**: TanStack Query manages server state and caching
3. **API Requests**: HTTP requests to Express.js REST API endpoints
4. **Database Operations**: Drizzle ORM queries PostgreSQL database
5. **Response Handling**: JSON responses cached and displayed in UI
6. **Real-time Updates**: Optimistic updates with query invalidation

## External Dependencies

### Frontend Dependencies
- **React Ecosystem**: React, React DOM, React Router (Wouter)
- **UI Libraries**: Radix UI primitives, Lucide React icons
- **State Management**: TanStack Query
- **Styling**: Tailwind CSS, class-variance-authority, clsx
- **Form Handling**: React Hook Form with Zod validation
- **Charts**: Recharts for data visualization
- **Date Management**: date-fns utility library

### Backend Dependencies
- **Server Framework**: Express.js
- **Database**: Drizzle ORM, Neon Database serverless
- **Validation**: Zod schema validation
- **Development**: tsx for TypeScript execution, esbuild for production builds

### Development Tools
- **Build Tools**: Vite, esbuild
- **TypeScript**: Full TypeScript support across frontend and backend
- **Code Quality**: ESLint, Prettier (implied by structure)
- **Development Server**: Vite dev server with HMR

## Deployment Strategy

### Production Build Process
1. **Frontend Build**: Vite builds React app to `dist/public`
2. **Backend Build**: esbuild bundles TypeScript server to `dist/index.js`
3. **Static Assets**: Frontend assets served by Express in production
4. **Database**: PostgreSQL hosted on Neon Database
5. **Environment**: Production environment variables for database connection

### Development Workflow
- **Local Development**: Vite dev server with Express API proxy
- **Database Migrations**: Drizzle Kit for schema changes
- **Type Safety**: Shared schema types between frontend and backend
- **Hot Reloading**: Vite HMR for fast development cycles

### Architectural Decisions

1. **Monorepo Structure**: Single repository with shared TypeScript types
   - **Problem**: Type safety between frontend and backend
   - **Solution**: Shared schema definitions in `/shared` directory
   - **Benefits**: Reduced type mismatches, easier refactoring

2. **Mobile-First Design**: Optimized for mobile ADHD users
   - **Problem**: ADHD users need simple, distraction-free interfaces
   - **Solution**: Bottom navigation, large touch targets, high contrast colors
   - **Benefits**: Better accessibility and user experience

3. **Serverless Database**: Neon Database for PostgreSQL
   - **Problem**: Need scalable, managed database solution
   - **Solution**: Serverless PostgreSQL with connection pooling
   - **Benefits**: Auto-scaling, reduced operational overhead

4. **ORM Choice**: Drizzle ORM over Prisma
   - **Problem**: Need type-safe database queries with good performance
   - **Solution**: Drizzle ORM with TypeScript-first approach
   - **Benefits**: Better TypeScript integration, smaller bundle size

## Recent Changes

- **July 03, 2025**: Initial setup with mobile-first wellness app
- **July 03, 2025**: Expanded wellness dimensions from 6 to 10 comprehensive areas:
  - Added: Emotional, Environmental, Intellectual, Creative dimensions
  - Enhanced wellness tracking with more holistic approach
- **July 03, 2025**: Created comprehensive Life Planner feature:
  - Life Balance Score calculation across all dimensions
  - Wellness insights and recommendations
  - Goal organization by timeframes (short/medium/long term)
  - Priority goal identification with deadline awareness
  - Roadmap view for structured life planning
- **July 03, 2025**: Improved navigation:
  - Updated bottom navigation to include Life Planner
  - Reorganized tabs: Home, Life Plan, Daily, Goals, Progress
  - Enhanced ADHD-friendly color scheme with new dimension colors

## User Preferences

Preferred communication style: Simple, everyday language.
