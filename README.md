# Event & Ticket Management Platform - UI Design Files

This package contains complete UI design for Smart Event & Ticket Management Platform.

##  Files Included

### HTML Mockup Files (8 separate screens)

1. **01_auth_onboarding.html**
   - Onboarding screen with app features
   - Login screen with email/password
   - Registration screen with role selection (User/Organizer)

2. **02_user_discovery.html**
   - User home screen with event discovery
   - Search functionality
   - Category filters
   - Featured event cards
   - Bottom navigation

3. **03_event_details_seats.html**
   - Event details screen with complete information
   - Interactive seat selection map
   - Seat availability visualization
   - Booking summary

4. **04_booking_tickets.html**
   - Booking confirmation screen
   - My Tickets list view
   - QR code display (SVG-based)
   - Expandable ticket cards

5. **05_organizer_dashboard.html**
   - Organizer analytics dashboard
   - Quick stats (events, bookings, revenue, attendance)
   - Event management cards
   - Progress indicators

6. **06_create_event_seats.html**
   - Multi-step event creation form
   - Seat allocation configuration
   - Pricing tier management
   - Revenue projection calculator

7. **07_qr_scanner_validation.html**
   - Camera-based QR scanner interface
   - Valid ticket validation screen
   - Invalid ticket error screen
   - Ticket details display

8. **08_notifications_profile.html**
   - Notification center with tabs
   - User profile management
   - Settings and preferences
   - Account configuration

### Design System Document

**event_booking_design_system.md**
- Complete color palette with Flutter code
- Typography system
- Component library (buttons, cards, forms)
- Database schemas (SQLite)
- Flutter implementation examples
- State management patterns
- Navigation architecture
- API integration
- Testing strategies
- Deployment checklist

##  Design Features

### Icon-Free Professional Design
All mockups use a clean, icon-free approach:
- Text labels instead of icon fonts
- Letter placeholders (e.g., "EH" for EventHub, "JD" for John Doe)
- Geometric shapes and color coding
- Professional, corporate aesthetic

### Color Scheme
- Primary: Blue (#185FA5)
- Success: Green (#639922)
- Warning: Amber (#BA7517)
- Danger: Red (#E24B4A)
- Neutral grays for backgrounds and text

### Key UI Elements
- Clean card-based layouts
- Subtle borders (0.5px)
- Rounded corners (8-12px radius)
- Professional typography (Roboto/Inter recommended)
- Responsive 380px mobile width

##  How to Use These Files

### Viewing the Mockups
1. Open any HTML file in your web browser
2. Each file is standalone and fully styled
3. Screens are designed for 380px mobile viewport
4. All HTML files are production-ready reference designs

### Implementing in Flutter
1. Review the `event_booking_design_system.md` for:
   - Exact color codes
   - Widget structures
   - Database schemas
   - Implementation patterns

2. Each screen in the HTML corresponds to a Flutter screen:
   - HTML structure → Flutter widget tree
   - CSS classes → Flutter widget properties
   - Colors → Material theme colors

3. Use provided Flutter code snippets for:
   - Authentication flows
   - State management
   - QR code generation
   - API integration
   - Database operations

##  Project Requirements Coverage

 **Advanced Navigation**
- Named routes
- Nested navigation (bottom navigation with stacks)
- Route guards (auth-based routing)

 **State Management**
- Riverpod/Bloc patterns provided
- Clean separation of UI and business logic

 **Clean Architecture**
- Presentation Layer
- Business Logic Layer
- Data Layer (Repository pattern)

 **Local & Remote Data**
- SQLite schemas for all tables
- REST API integration examples
- Async/await patterns

 **Authentication**
- Multi-role system (User/Organizer)
- Mock/Firebase compatible

 **Device Features**
- QR code generation and scanning
- Push notifications scheduling

 **Performance & UX**
- Lazy loading examples
- Form validation
- Loading states
- Error handling

##  Implementation Steps

1. **Set up Flutter project structure**
   - Create folders: lib/presentation, lib/business_logic, lib/data
   - Set up navigation with go_router

2. **Implement authentication**
   - Create auth screens from 01_auth_onboarding.html
   - Set up state management
   - Add route guards

3. **Build user journey**
   - Event discovery (02_user_discovery.html)
   - Event details (03_event_details_seats.html)
   - Booking flow (04_booking_tickets.html)

4. **Build organizer features**
   - Dashboard (05_organizer_dashboard.html)
   - Event creation (06_create_event_seats.html)
   - QR scanner (07_qr_scanner_validation.html)

5. **Add auxiliary features**
   - Notifications (08_notifications_profile.html)
   - Profile settings

6. **Integrate backend**
   - Set up SQLite with provided schemas
   - Implement API calls
   - Add error handling

##  Screen Navigation Flow

```
Authentication
├── Onboarding → Login → Register
└── Main App (Role-based routing)

User Role:
├── Home (Event Discovery)
├── My Tickets (with QR codes)
├── Notifications
└── Profile

Organizer Role:
├── Dashboard (Analytics)
├── My Events (Management)
├── QR Scanner (Validation)
└── Settings
```

##  Key Implementation Notes

### QR Code Generation
- Use `qr_flutter` package
- Format: "TKT-YYYY-SEATS" (e.g., TKT-2026-A3A4)
- Display in My Tickets screen
- White background for scanning

### Seat Selection
- Interactive grid layout
- Three states: available, selected, booked
- Color-coded visualization
- Real-time selection updates

### Multi-Role Authentication
- UserRole enum: user, organizer
- Different bottom navigation per role
- Role-based route access
- Database user.role field

### Database Relationships
- users → events (organizer_id)
- events → seats (event_id)
- bookings → tickets (booking_id)
- tickets → seats (seat_id)

##  Support & Questions

Refer to the design system document for:
- Detailed component specifications
- Complete code examples
- Database migration guides
- Testing strategies
- Performance optimization tips

##  License

These design files are provided for your ICT4153 academic project.

---

