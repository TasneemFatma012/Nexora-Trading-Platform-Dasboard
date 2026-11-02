# ⚡ Nexora Trading Platform

### Where data meets decisions.

Nexora is a full-stack trading dashboard built to bring market data, investments, orders, and portfolio activity into a single streamlined workspace.

The project focuses on recreating the kind of experience users expect from modern trading platforms — fast navigation, clear insights, organized data, and simple interactions.

### 🔎 Inside Nexora

Market → Watchlist → Orders → Holdings → Funds → KYC

Everything connects through a REST-based architecture, creating a complete flow from exploring the market to managing a portfolio.

### 🧩 Built With

React · Vite · Node.js · Express.js · MongoDB · MUI · Axios · REST API

### 🎯 The Idea

Nexora isn't just a dashboard UI. It is a practical exploration of how frontend, backend, APIs, database, and financial workflows come together to build a real-world web application.

> Observe the market. Manage the portfolio. Make the move.

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
- Node.js + Express backend
- MongoDB

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

