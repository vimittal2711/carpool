# 🚗 RideShare — Adobe Noida Carpool App

A modern, responsive web application for Adobe employees at the Noida office to find carpools, offer rides, and manage ride-sharing requests.

## ✨ Features

- **Find Rides** 🔍 - Search available rides by location, colleague name, or time of day
- **Post Rides** 🚗 - Offer your commute and specify available seats
- **Manage Requests** 📩 - Accept or decline ride requests from colleagues
- **Ride Preferences** ⚙️ - Set preferences (music, smoking, conversation, women-only mode, notifications)
- **Profile Management** 👤 - Edit your profile and track ride statistics
- **Responsive Design** 📱 - Works seamlessly on desktop, tablet, and mobile devices
- **Local Storage** 💾 - All data persists in your browser

## 🎯 Features Included

- **Search & Filter** - Find rides by pickup/destination area, time of day (morning/evening), or availability
- **Ride Cards** - View driver info, ratings, car details, seats available, and notes
- **Modal Forms** - Easy-to-use forms for posting and editing rides with date/time pickers
- **Real-time Updates** - Counters and badges update automatically
- **Toast Notifications** - Feedback for all actions

## 🚀 Getting Started

### Option 1: Live on GitHub Pages
Open your browser and visit: `https://vimittal2711.github.io/carpool/`

### Option 2: Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/vimittal2711/carpool.git
   ```
2. Open `index.html` in your web browser
3. Data is stored in your browser's localStorage

## 🛠️ Technology Stack

- **HTML5** - Semantic markup
- **CSS3** - Responsive design with CSS variables and flexbox
- **Vanilla JavaScript** - No dependencies or frameworks
- **localStorage API** - Browser-based data persistence

## 📊 Data Model

### Ride Object
```javascript
{
  id: string,              // Unique identifier
  mine: boolean,           // Is this ride posted by you?
  driverName: string,
  driverRole: string,
  from: string,           // Pickup location
  to: string,             // Destination
  date: string,           // YYYY-MM-DD format
  time: string,           // HH:MM format
  seats: number,          // Total available seats
  takenSeats: number,     // Seats already booked
  type: string,           // "daily" | "weekly" | "onetime"
  car: string,            // Car details (optional)
  notes: string,          // Notes for riders
  rating: number          // Driver rating (1-5)
}
```

### Request Object
```javascript
{
  id: string,
  rideId: string,         // Reference to ride
  name: string,           // Requester's name
  date: string,           // Request date
  status: string          // "pending" | "accepted" | "declined"
}
```

### Profile Object
```javascript
{
  name: string,
  role: string,           // Team/Role
  area: string,           // Home area
  phone: string           // Contact number
}
```

## 🎨 Design System

- **Primary Color**: #1C6BF0 (Adobe Blue)
- **Success**: #16A34A (Green)
- **Warning**: #D97706 (Amber)
- **Error**: #E53E3E (Red)
- **Font**: Outfit (headings & body), JetBrains Mono (times)
- **Radius**: 16px (cards), 10px (inputs)

## 📝 Demo Data

The app comes with pre-populated demo rides from colleagues:
- **Priya Kapoor** - Silver Honda City (Daily, 08:30)
- **Arjun Singh** - White Brezza (Daily, 08:15)
- **Sunita Patel** - Black Creta (Weekly, 08:45)
- **Vikram Mehta** - One-time ride (09:00)

Clear your browser data to reset demo rides.

## 🔄 Usage Flow

1. **Browse Available Rides** → Check the "Find Rides" tab to see what's available
2. **Post Your Ride** → Switch to "My Rides" and click "+ Offer ride"
3. **Manage Requests** → In the "Requests" tab, accept/decline incoming requests
4. **Update Profile** → Go to "Profile" to edit your details and preferences

## 🚀 Publishing (GitHub Pages)

The app is automatically published at: `https://vimittal2711.github.io/carpool/`

To deploy any changes:
1. Push updates to the `main` branch
2. GitHub Pages will automatically rebuild within seconds
3. Visit the URL above to see the changes

## 📄 File Structure

```
carpool/
├── index.html          # Complete single-page application
└── README.md          # This file
```

## 🔒 Privacy & Data

- **No Server** - All data stays in your browser
- **Local Storage** - Uses browser's localStorage API (cleared if you clear browser data)
- **No Cloud Sync** - Changes don't sync across devices
- **No User Tracking** - Completely private

## 🎓 Demo Credentials

Default profile: **Rahul Sharma** (Experience Cloud)
- You can modify your name and role in the Profile tab
- Try creating rides and managing requests!

## 🐛 Known Limitations

- Data is stored only in localStorage (not synced across devices or browsers)
- No backend authentication or real-time updates
- Phone numbers are for display only (no automatic calling)
- No map integration for location picking

## 🚀 Future Enhancements

- Backend API integration with real database
- Real-time notifications with WebSockets
- Map integration with Google Maps API
- User authentication with SSO
- Rating and review system
- Payment integration for shared fuel costs
- Push notifications

## 📞 Support

For issues or suggestions, please open a GitHub issue.

## 📄 License

This project is part of the Adobe Noida office carpool initiative.

---

Made with ❤️ for carpooling colleagues at Adobe Noida
