# 💍 Our Wedding - Budget Tracker

A beautiful, modern wedding budget tracker designed to help couples easily monitor and manage their wedding expenses. Built with a clean, intuitive interface featuring real-time calculations, visual analytics, and comprehensive expense tracking.

## Features

### 📊 **Dashboard**
- Visual doughnut chart showing spent vs budget allocation
- Key metrics at a glance:
  - **You've Spent**: Track actual expenses against total budget
  - **Total Planned Expense**: Sum of all budgeted amounts
  - **Payments Made**: Total amount already paid out
  - **Future Payments**: Upcoming expenses to be paid
- **Spent by Source**: Breakdown of expenses by payment source/vendor

### 📈 **Statistics & Analytics**
- Comprehensive expense analytics with doughnut chart visualization
- View total spent across all categories
- Dynamic category legend with color coding
- Expense history with full details (All Expenses list)
- Smart sorting options for expense data

### 💰 **Expense Management**
- Log individual expenses with full details
- Categorize expenses by type and vendor
- Track payment methods and transaction dates
- Multiple sorting options:
  - By amount (High to Low, Low to High)
  - By date (Newest to Oldest, Oldest to Newest)
  - By category
  - By vendor/source

### 🏖️ **Budget Planning**
- Create and manage budget plans by category and vendor
- Track planned amounts vs actual spending
- Monitor vendor status throughout planning process
- Real-time budget calculations and updates

### 🔐 **Secure Access**
- Email and password authentication
- Personalized dashboard for each user ("Hello, Lovebirds")
- Logout functionality
- Secure session management

## Tech Stack

- **Frontend**: 
  - HTML5
  - Tailwind CSS (responsive design framework)
  - Chart.js (data visualization)
  - Plus Jakarta Sans font (modern typography)
  
- **Backend**: Firebase Firestore (cloud database)
- **Authentication**: Firebase Auth
- **Design**: Modern, mobile-optimized UI with smooth animations

## Getting Started

### Quick Start
Simply open `index.html` in your web browser to get started. The application features a responsive design that works seamlessly on desktop, tablet, and mobile devices.

### Navigation
The app uses a bottom navigation bar with multiple tabs:
1. **Dashboard** - Home view with overview and key metrics
2. **Statistics** - Detailed expense analytics and breakdowns
3. Additional tabs for budget planning and expense management

## User Interface Highlights

- **Clean, Minimalist Design**: Built with Tailwind CSS and a custom color palette (soft lavender blue, candy rose pink)
- **Smooth Animations**: Fade and scale transitions for tab switching
- **Responsive Layout**: Mobile-first design with max-width container (420px on desktop)
- **Interactive Charts**: Visual representations of budget data using Chart.js
- **Bottom Sheet Modals**: Modern modal interface for data entry
- **Custom Radio Inputs**: Styled form elements with color customization

## Features Breakdown

### Calculations & Summaries
- Real-time sum calculations for total budget and expenses
- Automatic tracking of paid vs future payments
- Per-source expense consolidation
- Dynamic legend generation for chart categories

### Data Organization
- Budget tracking by category and vendor
- Expense logging with transaction details
- Source-based expense breakdown
- Status tracking for planning purposes

### Visual Feedback
- Animated loading indicators (pulse effect)
- Toast notifications for user actions
- Modal confirmations for critical actions
- Status indicator for real-time data sync
  "Fixed Budget": 150000,
  "Contact": "john@grandpalace.com",
  "Number": "+91-9876543210",
  "Finalized At": "2026-02-15"
}
```

### Expenses Collection (Actual Spending)
```json
{
  "category": "Venue",
  "subcategory": "Banquet Hall",
  "description": "Hall Deposit",
  "amount": 50000,
  "paymentType": "Online",
  "paymentDate": "2026-02-15",
  "source": "Bank Transfer"
}
```

## Deployment

### GitHub Pages
1. Push code to GitHub
2. Go to Settings → Pages
3. Select main branch as source
4. Visit `https://username.github.io/wedding-expense-app/`

### Firebase Hosting
1. Install Firebase CLI: `npm install -g firebase-tools`
2. Initialize: `firebase init hosting`
3. Deploy: `firebase deploy`

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (responsive design)

## Firebase Setup

This app requires Firebase credentials. Add your config:

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

## Tips for Best Experience

✓ Use on desktop for full feature access
✓ Keep browser updated for best performance
✓ Enable browser notifications for sync updates
✓ Use Chrome for optimal Tailwind CSS rendering

## Contributing

This is a personal project for wedding planning. Customization for other events is welcome!

## License

Personal Use License - Feel free to fork and customize for your event!

## Author

Created with 💜 for wedding planning

---

**Last Updated**: April 2026

