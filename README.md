📈 SB Stocks – Full Stack Paper Trading Platform

A full-stack stock market simulation platform that allows users to practice trading using virtual funds in a realistic market environment. Users can buy and sell stocks, track portfolios, analyze price trends, manage transactions, and monitor performance through an interactive dashboard.

🌐 Live Demo: https://sb-stocks-sigma.vercel.app
⚙️ Backend API: https://sb-stocks-production.up.railway.app

🚀 Features
👤 User Features
User Registration & Login (JWT Authentication)
Secure Password Hashing with Bcrypt
Portfolio Management
Buy & Sell Stocks
Transaction History
Virtual Wallet Management
Deposit & Withdrawal Simulator
Real-Time Stock Price Updates
Watchlist Dashboard
Interactive Stock Charts
📊 Market Simulation
Dynamic stock price fluctuations
Multiple US stock listings
Historical price tracking
Live market updates
Portfolio valuation tracking
🔐 Authentication & Security
JWT-based authentication
Protected routes
Role-based authorization
Secure password storage
🛠️ Admin Features
User Management
Order Monitoring
Transaction Logs
Stock Management Dashboard
Administrative Analytics
🏗️ Tech Stack
Frontend
React.js
Vite
React Router DOM
Axios
Chart.js
React Toastify
Context API
CSS3
Backend
Node.js
Express.js
JWT Authentication
Bcrypt.js
Database
MongoDB Atlas
Mongoose ODM
Deployment
Frontend: Vercel
Backend: Railway
Database: MongoDB Atlas
📂 Project Structure
sb-stocks/
│
├── client/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   │   └── admin/
│   │   ├── App.jsx
│   │   ├── index.css
│   │   └── main.jsx
│   ├── package.json
│   └── vite.config.js
│
├── server/
│   ├── config/
│   ├── controllers/
│   ├── middlewares/
│   ├── models/
│   ├── Routes/
│   ├── index.js
│   └── verify_server.js
│
└── README.md
📸 Application Modules
Landing Page
Introduction to platform
Login & Registration
Dashboard
Trending Stocks
Watchlist
Market Overview
Stock Details
Real-Time Price Data
Historical Charts
Trading Interface
Portfolio
Holdings Overview
Investment Performance
Profit/Loss Tracking
Transaction History
Buy/Sell Records
Wallet Activity
Admin Dashboard
User Management
Orders Management
Transactions Monitoring
⚡ Installation & Setup
Prerequisites
Node.js (v16+)
MongoDB Atlas Account or Local MongoDB
Git
Clone Repository
git clone https://github.com/IllaVenkatesh/sb-stocks.git
cd sb-stocks
Backend Setup
cd server
npm install

Create .env

MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=5000

Run Server

npm run dev

Server runs on:

http://localhost:5000
Frontend Setup
cd client
npm install
npm run dev

Frontend runs on:

http://localhost:3000
🔌 API Endpoints
Authentication
POST /api/users/register
POST /api/users/login
Stocks
GET /api/stocks/list
GET /api/stocks/trending
GET /api/stocks/:symbol
Orders
POST /api/orders/buy
POST /api/orders/sell
GET /api/orders/history
Transactions
GET /api/transactions
POST /api/transactions/deposit
POST /api/transactions/withdraw
📈 Future Enhancements
Real Stock Market API Integration
Candlestick Charts
Watchlist Customization
Email Notifications
Portfolio Analytics
AI-Based Stock Insights
Multi-Currency Support
Dark Mode
👨‍💻 Developer

Venkatesh Illa

GitHub: https://github.com/IllaVenkatesh
LinkedIn: https://www.linkedin.com/in/illa-venkatesh/
⭐ Project Highlights
Full-Stack MERN Application
JWT Authentication & Authorization
MongoDB Atlas Integration
Railway Backend Deployment
Vercel Frontend Deployment
Responsive UI
Real-Time Stock Simulation Engine
