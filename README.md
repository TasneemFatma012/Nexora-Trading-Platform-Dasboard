# Zerodha Dashboard Clone

A modern trading dashboard inspired by Zerodha, built with React and Vite for portfolio tracking, holdings analysis, and market overview.

## Overview
This project recreates a simplified stock trading dashboard with sections for:
- holdings
- positions
- orders
- funds
- analytics
- app details
- user dashboard navigation

It is designed as a frontend dashboard that connects to a backend API for real or mock trading data.

## Features
- Portfolio summary cards
- Holdings table with investment and P&L values
- Positions tracking
- Orders management UI
- Funds and account balances
- App/category views
- Market and analytics dashboard cards
- Responsive desktop-first layout

## Tech Stack
- React
- Vite
- JavaScript
- Axios
- CSS
- Node.js + Express backend (separate project folder)
- MongoDB (for backend persistence)

## Project Structure
```bash
zerodha clone/
├── backend/
│   ├── controllers/
│   ├── model/
│   ├── routes/
│   ├── schemas/
│   ├── .env
│   ├── index.js
│   └── package.json
├── dashboard/
│   ├── src/
│   ├── public/
│   ├── .env
│   ├── package.json
│   ├── vite.config.js
│   └── README.md
└── README.md (optional root readme)
```

## Prerequisites
Before running the app, make sure you have installed:
- Node.js (v18 or newer recommended)
- npm
- MongoDB connection if using the backend database
- A working backend API or local mock server

## Getting Started

### 1. Install dashboard dependencies
```bash
cd dashboard
npm install
```

### 2. Configure environment variables
Create a `.env` file inside the `dashboard` folder:
```bash
VITE_API_URL=http://localhost:5000
```

If your backend is deployed elsewhere, replace the URL with the deployed API base URL.

### 3. Run the frontend locally
```bash
npm run dev
```

The app will usually run at:
```bash
http://localhost:5173
```

## Backend Setup
The frontend depends on an API backend located in the `backend` folder.

### Start the backend
```bash
cd backend
npm install
npm start
```

### Backend API endpoints used by the app
- `/holdings`
- `/positions`
- `/orders`
- `/funds`
- `/apps`
- `/market`
- `/users`

## Environment Configuration
### Dashboard `.env`
```bash
VITE_API_URL=http://localhost:5000
```

### Backend `.env`
Example values:
```bash
PORT=5000
MONGO_URL=mongodb+srv://<username>:<password>@cluster.mongodb.net/your-db
```

## Local Development Notes
- Ensure the backend is running before opening the dashboard.
- Keep both frontend and backend running in separate terminals.
- If the backend is unreachable, the dashboard may show empty or failed data states.
- Confirm your MongoDB Atlas whitelist includes your current IP if using remote MongoDB.

## Common Issues
### 1. Blank dashboard data
Check whether `VITE_API_URL` is correct in the dashboard `.env` file.

### 2. CORS error
Make sure the backend allows requests from the frontend origin (`localhost:5173` or similar).

### 3. MongoDB connection issue
If the backend fails to connect to MongoDB, verify the `.env` file in the backend has a valid `MONGO_URL` and IP whitelist access.

## Notes
- This is a frontend clone/demo project for learning and UI practice.
- Some features may require a real backend for data.
- In production, add proper authentication, validation, and security.

## License
This project is intended for educational and demo use.

## Future Improvements
- Add user authentication
- Improve state management
- Add real charting and watchlists
- Add a responsive mobile-first design
- Connect to a production-grade backend
- Add tests and API validation
