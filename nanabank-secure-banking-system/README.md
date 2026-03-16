# NanaBank – Secure Digital Banking Web Application

## Description

**NanaBank** is a simulated secure digital banking platform designed to demonstrate modern fintech development practices, backend architecture, and secure financial transaction systems.

The project replicates the core components of a modern online banking system, including user authentication, account management, internal money transfers, and transaction auditing.

## Objectives

NanaBank is designed as a learning and portfolio project focused on:

	•	Full-stack web application development
	•	Secure authentication systems
	•	Financial transaction logic
	•	API architecture
	•	Web application security
	•	Backend scalability concepts used in modern fintech platforms

The architecture follows a Security-by-Design approach, where security controls are embedded in every layer of the application.

---

## Key Objectives

This project demonstrates how modern banking platforms implement:

	•	Secure authentication workflows
	•	Financial transaction processing
	•	API-based backend services
	•	Secure database storage
	•	Fraud prevention concepts
	•	Role-based authorization systems

The goal is to simulate the core structure of a digital bank backend while applying industry best practices.

---

# Learning Objectives

By completing this project, you will learn how to:

- Build a full-stack web application  
- Design and structure a RESTful API  
- Implement secure authentication systems(Authentication tokens using JSON Web Token (JWT)) 
- Apply password hashing and token authentication with bcrypt
- Request validation and sanitization  
- API rate limiting  
- Protection against SQL/NoSQL injection  
- Role-based access control  
- Secure password storage  
- Session protection  
- Manage database models and relationships  
- Implement secure financial transaction logic  
- Design responsive web interfaces  
- Apply backend security best practices  

---

## System Architecture

The application follows a modular service-based architecture to separate responsibilities and improve maintainability.

```
Client (React Frontend)
        │
        ▼
API Gateway / Express Server
        │
        ▼
Application Services
 ├── Authentication Service
 ├── Account Service
 ├── Transaction Service
 └── Admin Service
        │
        ▼
Database Layer
(MongoDB)
```

### Architectural Principles
	•	API-First Design
	•	Service Separation
	•	Secure Authentication Layer
	•	Input Validation
	•	Scalable Backend Structure

# Project Structure

```
NanaBank/
│
├── client/                     # React frontend application
│   ├── components/
│   ├── pages/
│   ├── services/
│   └── styles/
│
├── server/                     # Backend API
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── middleware/
│   ├── config/
│   └── utils/
│
├── database/                   # Schema and seed data
├── docs/                       # Technical documentation
├── tests/                      # Unit and integration tests
│
├── .env.example
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
- bcrypt password hashing  

---

## Security Architecture

Security is a critical component of financial systems. NanaBank implements several security controls inspired by industry standards.

## Authentication Security

	•	Password hashing using bcrypt
	•	Token-based authentication using JWT
	•	Token expiration and refresh logic
	•	Optional Two-Factor Authentication

## API Security

	•	Rate limiting
	•	Input validation
	•	Request sanitization
	•	Secure HTTP headers
	•	CSRF protection

---

# Data Protection

	•	Sensitive data hashing
	•	Environment variable protection
	•	Secure secret key management
	•	Prevention of NoSQL injection attacks

---

# Secure Coding Practices

This project follows secure development guidelines including:

	•	Input validation
	•	Authentication enforcement
	•	Access control verification
	•	Protection against common vulnerabilities

---

# Database Models

### User Model

#### User
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

# API Endpoints

| Method | Endpoint | Description |
|------|---------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Authenticate user |
| GET | `/api/users/profile` | Get user profile |
| GET | `/api/accounts/balance` | Retrieve account balance|
| POST | `/api/transactions/transfer` | Transfer funds |
| GET | `/api/transactions/history` | View transaction history |

---

# Environment

Development environment:

- Ubuntu 22.04 LTS  
- Node.js (v18+)  
- npm (v9+)  
- MongoDB  
- Git  

---

# Requirements

**Before running the project, ensure you have:**

- Node.js installed  
- MongoDB installed or cloud database  
- Git installed  

**The following should also be configured:**

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

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/nanabank.git
cd nanabank
```

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

# Features

## Customer-Facing Features
	1.	User Accounts & Authentication
	•	Sign-up/login (email, phone, biometrics)
	•	Two-factor authentication (2FA)
	•	Password recovery
	2.	Dashboard
	•	Account balances
	•	Recent transactions
	•	Notifications
	3.	Transfers & Payments
	•	Internal transfers (within bank)
	•	External transfers (other banks, same country)
	•	Bill payments, mobile money integration
	•	Scheduled or recurring payments
	4.	Cards & Loans
	•	Request debit/credit cards
	•	Manage card limits, freeze/unfreeze
	•	Loan applications and repayment tracking
	5.	Customer Support
	•	Chatbot or live chat
	•	FAQ and knowledge base
	•	Ticket tracking
	6.	Security & Alerts
	•	SMS/email alerts for transactions
	•	Fraud detection flags
	•	Secure logout and session timeout

---

## Admin / Bank Staff Features
	1.	User Management
	•	Approve new accounts
	•	Manage KYC documents
	2.	Transaction Monitoring
	•	Flag suspicious activities
	•	Daily transaction reports
	3.	Product Management
	•	Configure loans, interest rates, and card types
	•	Manage promotional offers

---


## Technology Stack
	•	Frontend: React for responsive UI
	•	Backend: Node.js (Express), Django, or Spring Boot
	•	Database: PostgreSQL or MySQL for accounts, Redis for caching
	•	Authentication: OAuth2 + JWT + 2FA
	•	Security: HTTPS, encryption for data at rest & in transit
	•	Deployment: Docker + Kubernetes, cloud hosting (AWS, GCP, Azure)
	•	Notifications: Twilio (SMS), SendGrid (Email)
	•	Mobile Apps: React Native or Flutter for mobile version

---

## UI/UX Considerations
	•	Simple, clean dashboards
	•	Easy navigation between accounts, transfers, payments
	•	Mobile-first design
	•	Accessibility standards (WCAG)

---

## Compliance & Security
	•	KYC/AML checks
	•	PCI DSS compliance for card payments
	•	Strong encryption (AES-256 for data, TLS 1.3 for network)
	•	Regular security audits

---

# Future Improvements

### Planned upgrades include:

	•	Passkey authentication (WebAuthn)
	•	Fraud detection simulation
	•	Device-based login verification
	•	Email transaction alerts(Email notifications)
	•	Real-time notifications using WebSockets
	•	Multi-currency account support
	•	Payment gateway integration
	•	Transaction export as PDF
	•	Microservices architecture(backend system design pattern where an application is divided into small independent services. Instead of one large backend (monolith), the system is split into multiple services.)
	•	Mobile responsive design improvements(website automatically adjusts to different screen sizes:phone, tablet, laptop, desktop)
	
---

# Learning Resources

These books guided the design and security principles used in this project.

## Core Banking Systems
	•	Banking Solutions: Building Secure and Scalable Financial Systems — Surendra Pandey

## Secure Development
	•	Alice and Bob Learn Application Security — Tanya Janca
	•	Web Security for Developers — Malcolm McDonald

## System Architecture
	•	Building Microservices — Sam Newman
	•	Designing Data-Intensive Applications — Martin Kleppmann

## Node.js Stack
	•	Beginning Node.js, Express & MongoDB Development — Greg Lim

---

# Author

**Developer:** Gloria Ogunsemore

**Project:** NanaBank

**Purpose:** Learning secure fintech application development.

---

# License

**This project is for educational purposes only and does not represent a production banking system.**

---
