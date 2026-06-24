# SB Stocks - Full Stack Paper Trading Web Application

SB Stocks is a full-stack web application designed for stock market enthusiasts to simulate trading US stocks in real-time using virtual funds ($0 default wallet balance, which can be topped up via a deposit panel). 

The platform features high-fidelity price fluctuations, historical charts, order tracking, portfolio holdings, wallet deposit/withdrawal mechanisms, and an admin dashboard.

---

## 🛠️ Technology Stack
- **Frontend:** React.js, Vite, Axios, Chart.js, React Router, React Toastify, Vanilla CSS (clean dashboard theme).
- **Backend:** Node.js, Express.js, JWT Authentication, Bcrypt password hashing.
- **Database:** MongoDB (using Mongoose schemas).

---

## 📂 Project Structure
```
sb-stocks/
├── client/                      # Frontend component (Vite + React)
│   ├── public/
│   ├── src/
│   │   ├── assets/              # Premium vectors and images
│   │   ├── components/          # Reusable cards & layout components (Login, Register, Navbar)
│   │   ├── context/             # Global Auth & Transaction Context (GeneralContext)
│   │   ├── pages/               # Views (Landing, Home, StockChart, Portfolio, History, Profile)
│   │   │   └── admin/           # Admin pages (Admin, Users, AllOrders, AllTransactions, AdminStockChart)
│   │   ├── App.jsx              # Routing rules
│   │   ├── index.css            # Styling sheet (dashboard theme)
│   │   └── main.jsx
│   ├── index.html
│   ├── package.json
│   └── vite.config.js
│
└── server/                      # Backend component (Express + Mongoose)
    ├── config/
    │   └── db.js                # Database connection
    ├── controllers/             # Request handlers (user, stock, order, transaction)
    ├── middlewares/
    │   └── authMiddleware.js    # JWT protectors
    ├── models/                  # Schemas (userModel, stockSchema, transactionModel, orderSchema)
    ├── Routes/                  # Router bindings (userRoute, stockRoute, orderRoute, transactionRoute)
    ├── .env                     # Server environment variables
    ├── index.js                 # Entry point (running simulation ticks)
    ├── Schemas.js               # Central exports for schemas
    └── verify_server.js         # Backend compile check script
```

---

## 🚀 How to Run the Project Locally

### Prerequisites
- Make sure [Node.js](https://nodejs.org/) (v16 or above) and `npm` are installed.
- Ensure [MongoDB](https://www.mongodb.com/) is installed and running locally.

### Setup Instructions

1. **Open the Project Folder:**
   Open the root `sb-stocks` directory in your IDE/Code Editor (such as Visual Studio Code).

2. **Run the Backend Server:**
   - Open a terminal and navigate to the `server` folder:
     ```bash
     cd server
     ```
   - Install dependencies:
     ```bash
     npm install
     ```
   - Run in development mode (with hot reloading via `nodemon`):
     ```bash
     npm run dev
     ```
   - The server will start on port `5000` and connect to the local MongoDB database.

3. **Run the Frontend Client:**
   - Open a second terminal window and navigate to the `client` folder:
     ```bash
     cd client
     ```
   - Install dependencies:
     ```bash
     npm install
     ```
   - Start the Vite development server:
     ```bash
     npm run dev
     ```
   - Open [http://localhost:3000](http://localhost:3000) in your browser to view the application.

---

## 💡 Key Features of the Simulation
- **Live Stock Ticks:** The server runs an in-memory background loop that fluctuates asset prices (TSLA, NVDA, AAPL, MSFT, etc.) every 4 seconds. The frontend polls these updates instantly.
- **Deposit & Withdrawal:** Since users register with a $0 balance, they can visit the **Profile** page to top up virtual funds (via net banking or IMPS simulator) before trading.
- **Interactive Graphs:** Detailed charts rendering simulated historical prices are generated using Chart.js on the **Stock Details** page.
- **Role-Based Views:** Registered accounts marked as `admin` have access to administrative views (Users lists, All Orders logs, All Transactions logs, and admin stock browser).
