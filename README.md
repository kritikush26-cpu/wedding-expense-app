# 💍 Wedding Expense App

A modern, real-time wedding budget tracker with vendor management and expense tracking powered by Firebase.

## Features

✨ **Budget Tracker**
- Track budgets by category (Venue, Catering, Decor, etc.)
- Monitor planned vs actual spending
- Real-time budget calculations
- Visual expense breakdown with charts

📊 **Expense Management**
- Log individual expenses
- Categorize by vendor and type
- Track payment methods and dates
- Filter and sort by multiple criteria

🎯 **Vendor Directory**
- Manage venue, vendor, and transportation contacts
- Track vendor status (Planning, Contacted, Finalized)
- Store contact information
- Budget allocation per vendor

🔄 **Real-Time Sync**
- Firebase Firestore integration
- Auto-refresh on all changes
- Cloud-based data sync

## Tech Stack

- **Frontend**: HTML5, Tailwind CSS, Chart.js
- **Backend**: Firebase Firestore
- **Authentication**: Firebase Auth
- **Hosting**: GitHub Pages / Firebase

## Getting Started

### Option 1: Live Demo
Visit the deployed app at: https://kritikush26-cpu.github.io/wedding-expense-app/

### Option 2: Local Setup

1. Clone the repository:
```bash
git clone https://github.com/kritikush26-cpu/wedding-expense-app.git
cd wedding-expense-app
```

2. Open `index.html` in your browser

3. Configure Firebase credentials in the code (if needed)

## Usage

### Budget Planning
1. Go to "Budget Planning" tab
2. Click "Add Plan" button
3. Enter category, vendor name, and budget
4. Track changes in real-time

### Log Expenses
1. Navigate to "Recent Expenses" tab
2. Click "Log Expense" button
3. Add transaction details
4. View updated dashboard summary

### Analyze Spending
- Use sort options to organize by budget, status, or date
- Check dashboard cards for budget vs actual spending
- View expense breakdown chart by category

## Features in Detail

### Smart Sorting (6 options per view)
- Alphabetical (Category/Subcategory/Name)
- Budget Range (High-Low, Low-High)
- Status (Planning → Contacted → Finalized)
- Date Range (Newest/Oldest for expenses)

### Custom Confirmations
- Modern, non-native delete confirmations
- Glass-morphism backdrop design
- Clear action messaging

### Real-Time Calculations
- Total Budget: Sum of all planned amounts
- Total Spent: Sum of actual expenses only
- Remaining: Budget minus actual spending
- Per-category breakdowns with charts

## Data Structure

### Masters Collection (Budget/Vendors)
```json
{
  "Master Category": "Venue",
  "Sub Category": "Banquet Hall",
  "Name": "Grand Palace",
  "Status": "Finalized",
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

