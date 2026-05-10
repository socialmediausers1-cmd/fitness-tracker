# Fitness Tracker - Setup Guide

Complete setup instructions for the fitness tracker app.

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Git
- Android Studio (for Android development)
- Xcode (for iOS development on Mac)
- MongoDB (local or cloud - MongoDB Atlas)

## Backend Setup

### 1. Navigate to backend folder
```bash
cd backend
```

### 2. Install dependencies
```bash
npm install
```

### 3. Create `.env` file
Create a file named `.env` in the backend folder:
```
MONGODB_URI=mongodb://localhost:27017/fitness-tracker
# OR use MongoDB Atlas:
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/fitness-tracker

JWT_SECRET=your_jwt_secret_key_here
PORT=5000
NODE_ENV=development
```

### 4. Start the backend server
```bash
npm start
```

The backend will run on `http://localhost:5000`

---

## Mobile App Setup

### 1. Navigate to mobile folder
```bash
cd mobile
```

### 2. Install dependencies
```bash
npm install
```

### 3. Configure API connection
Edit `src/services/api.js` and update the API URL:
```javascript
const API_URL = 'http://localhost:5000/api';
```

### 4. Run on Android
```bash
npx react-native run-android
```

### 5. Run on iOS (Mac only)
```bash
npx react-native run-ios
```

---

## Database Setup

### Option 1: Local MongoDB
1. Install MongoDB Community Edition
2. Start MongoDB service
3. Create database: `fitness-tracker`

### Option 2: MongoDB Atlas (Cloud)
1. Go to https://www.mongodb.com/cloud/atlas
2. Create a free account
3. Create a cluster
4. Get connection string
5. Update `MONGODB_URI` in `.env`

---

## Troubleshooting

### Android issues:
- Clear cache: `cd android && ./gradlew clean && cd ..`
- Reset metro bundler: `npm start -- --reset-cache`

### iOS issues:
- Clear pods: `cd ios && rm -rf Pods && pod install && cd ..`
- Clear Xcode cache: `Cmd+Shift+K` in Xcode

### Port already in use:
- Change PORT in `.env` and restart backend

---

## Testing the App

1. Create a new account
2. Add your first workout
3. View your dashboard
4. Check progress charts
5. Add friends and compare results

---

## Next Steps

- Customize branding and colors
- Add push notifications
- Integrate with device sensors
- Deploy backend to a server
- Submit to App Store and Google Play

Good luck! 🚀
