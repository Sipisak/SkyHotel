# SkyHotel

SkyHotel is a modern hotel management system built with React and Vite, offering a comprehensive solution for hotel booking and management.

## 🌟 Features

### Room Management
- Search and browse available rooms
- View room details including prices and amenities
- Filter rooms by type and availability
- Add, update, and delete rooms (admin functionality)

### Booking System
- Real-time availability checking
- Flexible date selection for check-in and check-out
- Guest information management
- Booking confirmation with unique confirmation codes
- View and cancel existing bookings
- Payment processing integration

### User Features
- User registration and authentication
- User profile management
- Booking history tracking
- Email notifications for bookings

### Hotel Services
- 24-Hour Front Desk
- WiFi Access
- Breakfast Service
- Laundry Service
- Mini-bar
- Parking
- Air Conditioning
- Car Service
- Netflix Premium Entertainment

## 🛠️ Technical Stack

- **Frontend**: React.js with Vite
- **UI Framework**: React Bootstrap
- **State Management**: React Hooks
- **Date Handling**: Moment.js
- **HTTP Client**: Axios
- **Icons**: React Icons
- **Routing**: React Router DOM

## 📋 Prerequisites

- Node.js (version 14 or higher)
- npm or yarn package manager
- A modern web browser

## 💻 Installation

1. Clone the repository
```bash
git clone https://github.com/Sipisak/SkyHotel.git
cd SkyHotel
```

2. Install dependencies
```bash
npm install
# or
yarn install
```

3. Start the development server
```bash
npm run dev
# or
yarn dev
```

4. The application will be available at `http://localhost:5173` (or your configured port)

## 🔧 Configuration

The application uses a backend API running on `http://localhost:9192`. You can modify the API base URL in `src/components/utils/ApiFunctions.js`:

```javascript
export const api = axios.create({
    baseURL: "http://localhost:9192"
})
```

## 📁 Project Structure

```
src/
├── components/
│   ├── auth/              # Authentication related components
│   ├── booking/           # Booking system components
│   ├── common/            # Shared components
│   └── utils/             # Utility functions and API calls
```

## 🌐 API Endpoints

The application interacts with the following main API endpoints:

### Rooms
- GET `/rooms/all-rooms` - Get all rooms
- GET `/rooms/room/types` - Get available room types
- POST `/rooms/add/new-room` - Add a new room
- GET `/rooms/available-rooms` - Get available rooms by date and type

### Bookings
- POST `/bookings/room/{roomId}/booking` - Create a new booking
- GET `/bookings/all-bookings` - Get all bookings
- GET `/bookings/{confirmationCode}` - Get booking by confirmation code
- DELETE `/bookings/{bookingId}` - Cancel a booking

### Authentication
- POST `/auth/register-user` - Register a new user
- POST `/auth/login` - User login
