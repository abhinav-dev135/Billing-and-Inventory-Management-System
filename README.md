# Billing & Inventory Management System

> A full-stack web application for streamlined business operations — manage products, billing, customers, suppliers, and inventory with built-in AI-powered stock prediction.

![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat&logo=express&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)

---

## Overview

The **Billing & Inventory Management System** is a web-based business tool designed to simplify day-to-day operations for small and medium enterprises. It provides a centralized platform to handle product management, billing workflows, customer and supplier records, and inventory tracking — all from a single dashboard.

A standout feature is the integrated **AI-based stock prediction module**, which analyzes sales data to help businesses anticipate inventory needs and reduce stockouts or overstocking.

---

## Features

| Feature | Description |
|---|---|
| 📊 Dashboard | Real-time overview of key business metrics and statistics |
| 📦 Product & Inventory Management | Add, update, and track products and stock levels |
| 🧾 Billing System | Create and manage bills with ease |
| 🤖 AI Stock Prediction | ML-driven forecasting to optimize inventory decisions |
| 📈 Sales & Inventory Reports | Generate detailed reports for data-driven decisions |
| 👥 Customer Management | Maintain customer profiles and purchase history |
| 🏭 Supplier Management | Manage supplier information and procurement records |
| 🖨️ Invoice Generation | Auto-generate professional invoices |
| 📉 Stock Tracking | Monitor real-time stock movements and alerts |

---

## Tech Stack

### Frontend
- **React.js** — Component-based UI library
- **CSS** — Custom styling

### Backend
- **Node.js** — JavaScript runtime environment
- **Express.js** — Lightweight web application framework

### AI Service
- **Python** — Core language for the prediction service
- **Flask** — Lightweight API server for the AI module
- **Prophet / scikit-learn** — Time-series forecasting and ML models
- **Pandas / NumPy** — Data processing

### Database
- **MySQL** — Relational database for structured business data

---

## Project Structure

```
Billing_and_Inventory_Management_System/
├── frontend/                  # React.js client
│   └── src/
│       ├── components/        # AppLayout, shared UI
│       ├── pages/             # Auth, Setup, Discovery flows
│       ├── modules/           # Feature modules (AI, Billing, Dashboard,
│       │                      #   Inventory, Reports, Suppliers, B2B, ...)
│       ├── services/          # Centralised API layer (api.js)
│       ├── styles/            # Global stylesheets
│       ├── data/              # Static/seed data
│       ├── App.jsx
│       └── main.jsx
├── backend/                   # Node.js + Express server
│   └── src/
│       ├── modules/           # Feature modules (auth, billing, products,
│       │                      #   customers, suppliers, stock, reports, ai, ...)
│       ├── config/            # DB and app configuration
│       ├── middleware/        # Auth, error handling
│       ├── utils/             # Helper utilities
│       ├── app.js
│       └── server.js
├── ai-service/                # Python Flask AI microservice
│   ├── app.py                 # Flask API entry point
│   ├── predictor.py           # Stock prediction logic
│   ├── database.py            # DB access layer
│   ├── data_generator.py      # Synthetic data utilities
│   ├── models/                # Trained ML model artifacts
│   └── requirements.txt
└── README.md
```

---

## Installation & Setup

**Prerequisites:** Node.js v16+, Python 3.9+, MySQL 8+, Git

```bash
# 1. Clone the repo
git clone https://github.com/abhinav-dev135/Billing_and_Inventory_Management_System.git
cd Billing_and_Inventory_Management_System

# 2. Install dependencies
cd backend && npm install && cd ..
cd frontend && npm install && cd ..
cd ai-service && pip install -r requirements.txt && cd ..

# 3. Set up the database
mysql -u root -p -e "CREATE DATABASE billing_inventory_db;"
```

### Environment Variables

Create a `.env` file in `backend/`:

```env
PORT=5000
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=billing_inventory_db
JWT_SECRET=your_jwt_secret_key
```

Create a `.env` file in `ai-service/`:

```env
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=billing_inventory_db
```

> Never commit `.env` files — they are in `.gitignore`.

---

## Running the Project

Open three terminals and run each service:

```bash
# Terminal 1 — Backend
cd backend && npm start

# Terminal 2 — Frontend
cd frontend && npm start

# Terminal 3 — AI Service
cd ai-service && python app.py
```

| Service | URL |
|---|---|
| Frontend | http://localhost:3000 |
| Backend API | http://localhost:5000 |
| AI Service | http://localhost:5001 |

---

## Future Enhancements

- [ ] Mobile-responsive UI improvements
- [ ] Integration with payment gateways
- [ ] Multi-warehouse / multi-branch support
- [ ] REST API documentation with Swagger

---

## Author

**Abhinav Singh Yadav**
Full-Stack Developer

- GitHub: [@abhinav-dev135](https://github.com/abhinav-dev135)
- Repository: [Billing_and_Inventory_Management_System](https://github.com/abhinav-dev135/Billing_and_Inventory_Management_System)

---

> Built with focus on clean architecture and practical business value.
