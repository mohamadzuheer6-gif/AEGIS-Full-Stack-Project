# AEGIS – Full-Stack Campus Grievance & Opportunity Management Platform

A comprehensive full-stack institutional platform designed to manage student grievances, academic resources, internship opportunities, and faculty-student communication within a university ecosystem.

🔗 **Live Deployment:**  
https://aegis-krack-hack.vercel.app/

---

## 🚀 Overview

AEGIS is a modular full-stack web application built using a React frontend and Node.js/Express backend, with PostgreSQL for relational data persistence.

The system implements:

- Role-based access control (RBAC)
- JWT-based authentication
- RESTful API architecture
- Relational database modeling
- Real-time grievance tracking
- Opportunity lifecycle management
- Task and communication systems

---

## 🏗️ System Architecture

```
Client Layer
    React (Vite + Tailwind CSS)
        ↓
Application Layer
    Node.js + Express.js (REST API)
        ↓
Authentication Layer
    JWT (Role-based Access Control)
        ↓
Database Layer
    PostgreSQL
        ├── Users
        ├── Grievances
        ├── Academic Events
        ├── Opportunities
        ├── Applications
        ├── Bookmarks
        ├── Tasks
        └── Opportunity Messages
```

---

## 🎯 Core Functional Pillars

### 🔹 Pillar I & II – Identity & Grievance Management

- Submit grievances anonymously or with identity
- Status tracking & updates
- Authority dashboard for review & action
- Department-level grievance management
- Role-based permission enforcement

---

### 🔹 Pillar III – Chronos Calendar & Academic Tools

- Centralized academic calendar
- Event & deadline tracking
- Vault of Knowledge (academic resources & past papers)
- Destiny Manager (course tracking & credits)

---

### 🔹 Pillar IV – Opportunities & Scholar’s Ledger

- Faculty internship & research postings
- Student filtering by skills, duration, stipend
- Resume-based application tracking
- Bookmarking system
- Scholar’s Ledger task manager
- Faculty-student inbox messaging

---

## 🧠 Engineering Highlights (Full-Stack Focus)

- Modular backend architecture (controllers, routes, middleware separation)
- Secure JWT-based authentication
- Relational PostgreSQL schema design
- Role-based authorization middleware
- Scalable REST API design
- File upload handling using Multer
- Protected frontend routes using React Router
- API service abstraction layer in frontend
- Deployment-ready environment configuration

---

## 🛠️ Tech Stack

### Backend
- Node.js
- Express.js
- PostgreSQL
- JWT Authentication
- Multer (File Uploads)

### Frontend
- React 18
- Vite
- Tailwind CSS
- React Router v6
- Fetch API

---

## 📂 Project Structure

```
aegis/
├── aegis-backend/
│   ├── controllers/
│   ├── middleware/
│   ├── routes/
│   ├── db.js
│   ├── server.js
│   └── package.json
│
├── aegis-frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── App.jsx
│   └── package.json
│
├── .gitignore
└── README.md
```

---

## 🗄️ Database Schema

Core relational tables:

- `users` – Role-based user accounts
- `grievances` – Grievance records & status tracking
- `academic_events` – Calendar events
- `opportunities` – Internship & research listings
- `applications` – Student applications
- `bookmarks` – Saved opportunities
- `tasks` – Scholar’s Ledger tasks
- `opportunity_messages` – Faculty-student communication

---

## 🔐 Authentication & Authorization

- JWT stored in `localStorage['aegis_token']`
- JWT payload contains:
  ```
  { id, user_id, email, role, iat, exp }
  ```
- Protected routes require:
  ```
  Authorization: Bearer <token>
  ```
- Role-based access:
  - Student
  - Faculty
  - Authority
  - Admin

---

## ⚙️ Installation & Setup

### Prerequisites
- Node.js 16+
- PostgreSQL
- Git

---

### Backend Setup

```bash
cd aegis-backend
npm install
```

Create a `.env` file:

```
DB_HOST=localhost
DB_PORT=5432
DB_NAME=aegis_db
DB_USER=your_db_user
DB_PASS=your_db_password
JWT_SECRET=your_jwt_secret_key
NODE_ENV=development
PORT=5000
```

Run backend:

```bash
npm start
```

---

### Frontend Setup

```bash
cd aegis-frontend
npm install
npm run dev
```

Visit:

```
http://localhost:5173
```

---

## 📦 Deployment

### Backend
- Deploy to AWS / Render / DigitalOcean
- Configure environment variables
- Ensure PostgreSQL access

### Frontend
- Build with:
  ```bash
  npm run build
  ```
- Deploy `dist/` folder to Vercel / Netlify
- Update API base URL accordingly

---

## 👥 User Roles

| Role      | Capabilities |
|-----------|--------------|
| Student   | Submit grievances, apply to opportunities, manage tasks |
| Faculty   | Post opportunities, review applications, message students |
| Authority | Manage grievances, assign & update statuses |
| Admin     | Full system control |

---

## 🧪 Development

Run backend tests:

```bash
npm test
```

Build frontend:

```bash
npm run build
```

---

## 📄 License

This project is licensed under the MIT License.

---

## ✨ AEGIS

Empowering campus communities through transparent grievance resolution and structured opportunity access.
