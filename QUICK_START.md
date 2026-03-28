# Quick Start Guide

## Getting Started in 3 Steps

### Step 1: Install Dependencies
```bash
npm install
```

### Step 2: Start Development Server
```bash
npm run dev
```

### Step 3: Open in Browser
Navigate to `http://localhost:5173`

---

## What You'll See

### 🏠 Home Page (`/`)
- **Resource Grid**: Browse 6 different resources (rooms, equipment, parking, workspace)
- **Filter Buttons**: Filter by resource type
- **Quick Stats**: See total resources and availability
- **Booking Links**: Click "Book Now" on any resource

### 📅 Booking Page (`/book/:resourceId`)
- **Resource Details**: Full information about the selected resource
- **Booking Form**: Fill in your details
- **Available Times**: See available time slots
- **Confirmation**: Get booking confirmation with ID

---

## Available Resources

| Name | Type | Rate | Capacity |
|------|------|------|----------|
| Conference Room A | Room | $50/hr | 10 |
| Meeting Room B | Room | $35/hr | 6 |
| Projector Equipment | Equipment | $20/hr | 1 |
| Video Conferencing | Equipment | $40/hr | 1 |
| Parking Space A1 | Parking | $5/hr | 1 |
| Desk Space - Window | Workspace | $25/hr | 1 |

---

## Making a Booking

1. **Browse Resources** - View the home page
2. **Select Resource** - Click "Book Now" on desired resource
3. **Fill Details**:
   - Enter your Full Name
   - Enter your Email
   - Pick a Date (today or future)
   - Select Time Slot (based on availability)
   - Choose Duration (1-8 hours)
   - Add Optional Notes
4. **Confirm** - Click "Confirm Booking"
5. **See Confirmation** - Your booking ID and details

---

## Form Validation

The form validates:
- ✅ Email format is correct
- ✅ All required fields are filled
- ✅ Date is today or in future
- ✅ Time slot is available
- ✅ Duration is valid (1-8 hours)
- ✅ Slot hasn't been booked already

---

## Available Commands

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linting
npm run lint

# Install dependencies
npm install
```

---

## Key Features to Try

### 1. **Filter Resources**
Click filter buttons (All, room, equipment, parking, workspace) to see different resource types

### 2. **View Availability**
Each resource shows its available time slots (8:00 AM onwards)

### 3. **Form Validation**
Try entering invalid email or past date to see error messages

### 4. **Date-Dependent Slots**
Select different dates to see how available slots change

### 5. **Success Confirmation**
After booking, see your confirmation number and details

---

## Troubleshooting

### Port Already In Use
If port 5173 is busy, check running processes and kill them, or Vite will use the next available port.

### Dependencies Not Installing
```bash
# Clear npm cache
npm cache clean --force

# Try install again
npm install
```

### Build Errors
```bash
# Check for linting issues
npm run lint

# Fix auto-fixable issues
npm run lint -- --fix
```

---

## Tips

💡 **Try these combinations:**
- Book multiple resources for the same date
- Try unavailable time slots to see error handling
- Test on mobile by resizing browser
- Use keyboard navigation to test accessibility
- Try booking a full 8-hour day

---

## File Organization

```
PROJFWD/
├── src/
│   ├── components/         # Reusable components
│   ├── context/           # State management
│   ├── pages/             # Page components
│   ├── styles/            # Component styles
│   └── App.jsx            # Main app
├── package.json           # Dependencies
├── vite.config.js         # Build config
└── index.html             # HTML entry
```

---

## Need Help?

1. Check `PROJECT_DOCUMENTATION.md` for full documentation
2. Check `IMPLEMENTATION_SUMMARY.md` for what was built
3. Review component files for comments and logic
4. Run `npm run lint` to check code quality

---

## Next Steps

After exploring the basic functionality:

1. **Try Different Scenarios**:
   - Book resources across different dates
   - Check how time slots change per date
   - Test form validation thoroughly

2. **Explore the Code**:
   - Look at `BookingContext.jsx` for state logic
   - Check `BookingForm.jsx` for form handling
   - Review `BookingPage.jsx` for booking flow

3. **Extend Features** (Optional):
   - Add user profile management
   - Implement persistent storage
   - Add email notifications
   - Create admin dashboard

---

**Ready? Run `npm run dev` and start exploring!** 🚀

---

Version: 1.0.0  
Last Updated: February 28, 2026
