# NanaBank – Secure Banking Web Application

## Description

**NanaBank** is a simulated digital banking web application designed to demonstrate modern web development practices, secure authentication mechanisms, and financial transaction workflows.

This project focuses on building a full-stack banking system that allows users to register accounts, authenticate securely, manage balances, perform simulated money transfers, and view transaction history. NanaBank is designed as a learning and portfolio project to explore backend architecture, database management, security best practices, and responsive UI design.

The goal of this project is to replicate core features of modern fintech platforms while implementing strong security concepts such as password hashing, token-based authentication, role-based access control, and secure API design.

---

# Project Structure
```
NanaBank/
│
├── client/                     # Frontend application
│   ├── components/             # Reusable UI components
│   ├── pages/                  # Application pages
│   ├── services/               # API request logic
│   └── styles/                 # CSS / Tailwind styles
│
├── server/                     # Backend API
│   ├── controllers/            # Business logic
│   ├── routes/                 # API endpoints
│   ├── models/                 # Database models
│   ├── middleware/             # Authentication & security middleware
│   ├── config/                 # Database and app configuration
│   └── utils/                  # Helper utilities
│
├── database/                   # Database schema and seeds
│
├── docs/                       # Documentation
│
├── tests/                      # Application tests
│
├── .env.example                # Environment variable example
├── package.json
└── README.md
```

---

# Core Features

| Feature | Description |
|------|-------------|
| **User Registration** | Users can create secure accounts with email and password. |
| **User Authentication** | Secure login system using token-based authentication. |
| **User Dashboard** | Displays account information, balance, and recent transactions. |
| **Money Transfer** | Simulated transfer of funds between users within the system. |
| **Transaction History** | Logs all deposits, withdrawals, and transfers. |
| **Two-Factor Authentication (2FA)** | Optional OTP verification for enhanced account security. |
| **Role-Based Access Control** | Different permissions for normal users and administrators. |
| **Admin Dashboard** | Allows administrators to monitor users and transactions. |

---

# Technologies Used

## Frontend

- HTML5  
- CSS3 / TailwindCSS  
- JavaScript  
- React  

## Backend

- Node.js  
- Express.js  

## Database

- MongoDB  

## Authentication & Security

- JSON Web Token (JWT)  
- bcrypt  
- Input validation  
- Rate limiting  
- Secure HTTP headers  
- CSRF protection  

---

# Environment

Example development environment:

- Ubuntu 22.04 LTS  
- Node.js (v18+)  
- npm (v9+)  
- MongoDB  
- Git  

---

# Requirements

Before running the project, ensure you have:

- Node.js installed  
- MongoDB installed or cloud database  
- Git installed  

The following should also be configured:

- Environment variables  
- Database connection  
- Secure secret keys  

---

# Environment Variables

Create a `.env` file in the server directory.

### Example:
```
PORT=5000
MONGO_URI=mongodb://localhost:27017/nanabank
JWT_SECRET=your_jwt_secret
JWT_EXPIRE=24h
EMAIL_SERVICE=example_email_service
EMAIL_USER=example@email.com
EMAIL_PASS=yourpassword
```

---

# Learning Objectives

By completing this project, you will learn how to:

- Build a full-stack web application  
- Design and structure a RESTful API  
- Implement secure authentication systems  
- Apply password hashing and token authentication  
- Manage database models and relationships  
- Implement secure financial transaction logic  
- Design responsive web interfaces  
- Apply backend security best practices  

---

# API Endpoints

| Method | Endpoint | Description |
|------|---------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Authenticate user |
| GET | `/api/users/profile` | Retrieve user profile |
| GET | `/api/accounts/balance` | Get account balance |
| POST | `/api/transactions/transfer` | Transfer funds |
| GET | `/api/transactions/history` | Retrieve transaction history |

---

# Database Models

## User Model

### User
```
 ├── id
 ├── name
 ├── email
 ├── password (hashed)
 ├── role
 └── createdAt
```
## Account Model

### Account
```
 ├── id
 ├── userId
 ├── accountNumber
 ├── balance
 └── createdAt
```

## Transaction Model

### Transaction
```
 ├── id
 ├── senderAccount
 ├── receiverAccount
 ├── amount
 ├── transactionType
 ├── status
 └── timestamp
```

---

# Security Concepts Implemented

This project demonstrates several important web security principles:

- Password hashing with bcrypt  
- Authentication tokens using JSON Web Token (JWT)  
- Request validation and sanitization  
- API rate limiting  
- Protection against SQL/NoSQL injection  
- Role-based access control  
- Secure password storage  
- Session protection  

---

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/nanabank.git
cd nanabank

### Install backend dependencies:

```bash
cd server
npm install
```

### Install frontend dependencies:

```bash
cd client
npm install
```

---

# Running the Application

### Start the backend server:

```bash
cd server
npm run dev
```

### Start the frontend application:

```bash
cd client
npm start
```

The application should now be running locally.

### Frontend:

```
http://localhost:3000
```

### Backend API:

```
http://localhost:5000
```

---

# Example Workflow
	1.	A user registers an account.
	2.	The password is hashed using bcrypt.
	3.	The user logs in and receives a JSON Web Token.
	4.	The token is used to authenticate requests.
	5.	The user can transfer funds to another account.
	6.	The system records the transaction in the database.

---

# Future Improvements

### Planned features include:

	•	Multi-currency support
	•	Fraud detection simulation
	•	Email notifications
	•	Mobile responsive design improvements
	•	Integration with payment gateways
	•	Real-time notifications using WebSockets
	•	Transaction export as PDF

---

# Author

**Developer:** Gloria Ogunsemore

**Project:** NanaBank

**Purpose:** Learning advanced web development and security concepts.

---
