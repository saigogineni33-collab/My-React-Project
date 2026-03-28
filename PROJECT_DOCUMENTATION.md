# Resource Booking & Availability System

A modern, scalable single-page booking application built with React and Vite, emphasizing best practices in state management, component architecture, route-driven navigation, and performance-aware rendering.

## Project Overview

The Resource Booking and Availability System is a front-end application that allows users to view resource availability and make bookings through a structured, intuitive interface. The project follows React best practices with predictable state flow, controlled user interactions, and comprehensive error handling.

## Key Features

### ✅ Resource Management
- **Resource Listing**: Browse all available resources with detailed information
- **Resource Types**: Filter resources by type (rooms, equipment, parking, workspace)
- **Availability Display**: Real-time display of available time slots for each resource
- **Resource Details**: Comprehensive information including capacity, hourly rates, and descriptions

### ✅ Booking System
- **Controlled Forms**: Form validation with real-time error messages
- **Date & Time Selection**: Date picker with future-date validation and time slot selection
- **Asynchronous Operations**: Simulated async API calls for availability checks and booking creation
- **Booking Confirmation**: Detailed confirmation with booking ID and summary
- **Form Accessibility**: Full ARIA labels, error descriptions, and semantic HTML

### ✅ Route-Based Navigation
- **Home Page** (`/`): Resource listing and filtering
- **Booking Page** (`/book/:resourceId`): Detailed booking form for selected resource
- **Dynamic Routing**: React Router enables seamless navigation between views

### ✅ State Management
- **Context API**: Centralized booking state using React Context
- **Custom Hooks**: `useBooking()` for easy state access across components
- **Predictable Flow**: Clear data flow from context to components

### ✅ Performance & UX
- **Lazy Loading**: Components load only when needed
- **Optimized Rendering**: Memoized callbacks and efficient state updates
- **Loading States**: Visual feedback during async operations
- **Error Handling**: Comprehensive error messages and recovery options
- **Responsive Design**: Mobile-first approach with responsive grid layouts

## Architecture

### Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── BookingForm.jsx     # Controlled form component
│   └── ResourceCard.jsx    # Resource display card
├── context/            # State management
│   └── BookingContext.jsx  # Global booking context
├── pages/              # Route pages
│   ├── ResourcesPage.jsx   # Home page with resource listing
│   └── BookingPage.jsx     # Booking form page
├── styles/             # CSS modules
│   ├── BookingForm.css
│   ├── BookingPage.css
│   ├── ResourceCard.css
│   └── ResourcesPage.css
├── App.jsx             # Main app with routing
├── App.css             # Global app styles
├── main.jsx            # React entry point
└── index.css           # Base styles
```

## Component Architecture

### BookingContext
**Purpose**: Centralized state management for bookings and resources

**Key Functions**:
- `checkAvailability()`: Verify if a resource is available at specific date/time
- `createBooking()`: Create new booking with async validation
- `getAvailableSlots()`: Get available time slots for a resource
- `cancelBooking()`: Cancel existing booking
- `getUserBookings()`: Retrieve user's bookings

### ResourceCard Component
**Purpose**: Display individual resource with booking button

**Features**:
- Resource icon and details
- Availability status badge
- Available slots count
- Link to booking page

### BookingForm Component
**Purpose**: Controlled form for creating bookings

**Features**:
- Controlled inputs for all form fields
- Real-time field validation
- Dynamic time slot filtering based on selected date
- Async form submission with loading state
- Comprehensive error messages
- Accessibility features (ARIA labels, error descriptions)

### ResourcesPage
**Purpose**: Home page with resource listing and filtering

**Features**:
- Grid layout for resources
- Filter buttons by resource type
- Quick stats (total resources, available count, types)
- Empty state handling

### BookingPage
**Purpose**: Detailed booking flow

**Features**:
- Resource details panel
- Booking form
- Available time slots display
- Success/error state handling
- Booking confirmation with summary

## State Management

### Booking Context Structure
```javascript
{
  id: timestamp,
  resourceId: number,
  userName: string,
  userEmail: string,
  date: string (YYYY-MM-DD),
  timeSlot: string (HH:MM),
  duration: number,
  notes: string,
  status: 'confirmed' | 'cancelled',
  createdAt: ISO timestamp
}
```

### Resource Structure
```javascript
{
  id: number,
  name: string,
  type: 'room' | 'equipment' | 'parking' | 'workspace',
  capacity: number,
  hourlyRate: number,
  description: string,
  available: boolean,
  availableSlots: string[],
  image: emoji
}
```

## Getting Started

### Installation

1. Install dependencies:
```bash
npm install
```

2. Start development server:
```bash
npm run dev
```

3. Open `http://localhost:5173` in your browser

### Build

```bash
npm run build
```

### Lint

```bash
npm run lint
```

## Technologies Used

- **React 19.2**: Modern UI library
- **React Router v6**: Client-side routing
- **Vite 7.3**: Fast build tool
- **CSS3**: Modern styling with gradients and animations
- **JavaScript ES6+**: Modern JavaScript features

## Accessibility Features

- ✅ ARIA labels for form inputs
- ✅ Error descriptions linked to form fields
- ✅ Semantic HTML structure
- ✅ Keyboard navigation support
- ✅ Focus management
- ✅ Loading state indicators (`aria-busy`)
- ✅ Accessible date pickers and selects

## Performance Optimizations

- ✅ Component-level CSS (scoped styles)
- ✅ Memoized callback functions
- ✅ Efficient re-rendering with controlled inputs
- ✅ Lazy loading of routes
- ✅ Optimized animations with CSS transitions
- ✅ Minimal dependencies

## Browser Support

- Chrome/Edge: Latest versions
- Firefox: Latest versions
- Safari: Latest versions
- Mobile browsers: Fully responsive

## Future Enhancements

- User authentication and profiles
- Booking history and management
- Calendar view for availability
- Payment integration
- Email notifications
- Admin dashboard
- Resource management panel
- Advanced filtering and search

## Code Quality

- **ESLint**: Configured for code quality
- **React Hooks**: Best practices for state and side effects
- **Form Validation**: Comprehensive client-side validation
- **Error Handling**: Graceful error states and recovery

## License

MIT

## Support

For support or questions, please contact the development team.

---

Built with React and Vite | Resource Booking System v1.0.0
