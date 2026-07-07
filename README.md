<div align="center">

<img src="https://img.shields.io/badge/Status-Live%20%26%20Production%20Ready-brightgreen?style=for-the-badge&logo=checkmarx" />
<img src="https://img.shields.io/badge/Stack-MERN-61DAFB?style=for-the-badge&logo=mongodb" />


<br /><br />

```
██████╗ ██████╗ ███████╗███████╗ ██████╗██████╗ ██╗██████╗ ████████╗ ██████╗
██╔══██╗██╔══██╗██╔════╝██╔════╝██╔════╝██╔══██╗██║██╔══██╗╚══██╔══╝██╔═══██╗
██████╔╝██████╔╝█████╗  ███████╗██║     ██████╔╝██║██████╔╝   ██║   ██║   ██║
██╔═══╝ ██╔══██╗██╔══╝  ╚════██║██║     ██╔══██╗██║██╔═══╝    ██║   ██║   ██║
██║     ██║  ██║███████╗███████║╚██████╗██║  ██║██║██║        ██║   ╚██████╔╝
╚═╝     ╚═╝  ╚═╝╚══════╝╚══════╝ ╚═════╝╚═╝  ╚═╝╚═╝╚═╝        ╚═╝    ╚═════╝
```

### 🏥 Healthcare. Reimagined. Digitized. Delivered.

**A production-grade, full-stack doctor appointment booking platform built for the modern patient.**

<br />

[![Patient Portal](https://img.shields.io/badge/🌐%20Patient%20Portal-Live-success?style=for-the-badge)](https://prescriipto.netlify.app)
[![Admin & Doctor Dashboard](https://img.shields.io/badge/⚙️%20Admin%20Dashboard-Live-success?style=for-the-badge)](https://prescriptionadmin.netlify.app)

<br />

---

</div>

## 📋 Table of Contents

- [Overview](#-overview)
- [Live Ecosystem](#-live-ecosystem)
- [Feature Showcase](#-feature-showcase)
- [Architecture](#-system-architecture)
- [Tech Stack](#-tech-stack)
- [Engineering Highlights](#-engineering-highlights)
- [Local Setup](#-local-setup)
- [Environment Variables](#-environment-variables)
- [Project Structure](#-project-structure)
- [Admin Access](#-admin-access)

---

## 🌟 Overview

**Prescripto** is a production-grade healthcare orchestration platform that eliminates the friction between patients and medical professionals. Built on the MERN stack, it delivers a seamless real-time appointment booking experience — from doctor discovery to payment confirmation — all within a single unified ecosystem.

> *"From browsing a specialist to booking a confirmed slot in under 60 seconds."*

The platform operates across **three distinct interfaces** — each purpose-built for its user role, unified by a shared backend and secured with enterprise-grade authentication.

---

## 🛰️ Live Ecosystem

| Interface | URL | Role |
|-----------|-----|------|
| 🩺 **Patient Hub** | [prescriipto.netlify.app](https://prescriipto.netlify.app) | Book appointments, manage profile, process payments |
| 🛡️ **Admin Command Center** | [prescriptionadmin.netlify.app](https://prescriptionadmin.netlify.app) | {Manage doctors, monitor system by admin}, {control appointments by doctors} |
| ⚙️ **Backend API** | Hosted on Render | RESTful API serving all clients |

---

## ✨ Feature Showcase

### 🩺 Patient Portal
- **Smart Doctor Discovery** — Filter and browse verified specialists by medical specialty, experience, and availability
- **Comprehensive Doctor Profiles** — View credentials, specialization, consultation fees, and real-time availability
- **Intelligent Slot Booking** — Book precise 30-minute appointment windows from live availability grids
- **Stripe Payment Integration** — Secure, instant payment processing with confirmation receipts (Test Mode)
- **Appointment Management** — View, track, and cancel upcoming bookings from a personal dashboard
- **Profile Management** — Update personal details and upload profile photos seamlessly

### 🛡️ Admin Command Center
- **Doctor Onboarding** — Register new doctors with profile images, specialty, credentials, and fee structures via Cloudinary-powered uploads
- **System-Wide Appointment Monitor** — Real-time overview of all bookings across every doctor and patient
- **Live Status Control** — Mark appointments as completed, pending, or cancelled in real-time
- **Analytics Dashboard** — Bird's-eye view of platform metrics — total doctors, patients, and appointment volumes
- **Doctor Management** — Edit profiles, toggle availability, and manage the entire clinical roster

### 👨‍⚕️ Doctor Portal
- **Consultation Schedule** — View all upcoming and historical appointments in a clean, organized interface
- **Availability Toggle** — Control booking availability status directly from the dashboard
- **Earnings Tracker** — Monitor per-appointment and cumulative earnings in real time
- **Patient Overview** — Access patient details for each scheduled consultation

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                     PRESCRIPTO ECOSYSTEM                         │
├──────────────────┬──────────────────┬───────────────────────────┤
│   PATIENT HUB    │   ADMIN CENTER   │      DOCTOR PORTAL        │
│  (React + TW)    │  (React + TW)    │      (React + TW)         │
│  Netlify CDN     │  Netlify CDN     │      Netlify CDN          │
└────────┬─────────┴────────┬─────────┴──────────┬────────────────┘
         │                  │                      │
         └──────────────────┼──────────────────────┘
                            │  HTTPS / REST API
                  ┌─────────▼──────────┐
                  │   EXPRESS.JS API   │
                  │   Node.js Server   │
                  │   Render Cloud     │
                  └─────────┬──────────┘
                            │
          ┌─────────────────┼──────────────────┐
          │                 │                  │
  ┌───────▼──────┐  ┌───────▼───────┐  ┌──────▼──────────┐
  │  MongoDB     │  │   Cloudinary  │  │  Stripe Payment │
  │  Atlas Cloud │  │   CDN / Media │  │  Gateway (Test) │
  └──────────────┘  └───────────────┘  └─────────────────┘
```

**Authentication Flow:**
```
Client Request → JWT Middleware → Role Check (Patient | Doctor | Admin) → Protected Route → Response
```

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Frontend** | React.js | Component-driven SPA architecture |
| **Styling** | Tailwind CSS | Utility-first responsive UI design |
| **Backend** | Node.js + Express.js | RESTful API server |
| **Database** | MongoDB Atlas | Cloud-hosted NoSQL persistence |
| **Authentication** | JWT + Bcrypt | Secure, stateless multi-role auth |
| **Payments** | Stripe SDK | PCI-compliant payment processing |
| **Media** | Cloudinary CDN | Optimized image hosting & delivery |
| **Deployment** | Netlify + Render | Frontend on CDN, Backend on cloud |

</div>

---

## ⚡ Engineering Highlights

### 🔒 Atomic Slot-Booking Engine
Implemented MongoDB-level atomic operations to prevent race conditions during high-traffic concurrent booking windows. Two patients cannot book the same slot — guaranteed at the database transaction layer.

### 🧱 Triple-Interface RBAC Architecture
Engineered a clean Role-Based Access Control system serving three distinct user types (Patient, Doctor, Admin) from a single backend API, each with dedicated route guards, JWT scopes, and tailored analytical dashboards.

### 🌐 Zero-Downtime SPA Routing
Configured custom `_redirects` rules on Netlify to handle the React Router lifecycle on static hosting — eliminating all `404 Not Found` errors on page refresh or direct URL access.

### 🔐 Layered Security
- **JWT** for stateless, expirable session tokens
- **Bcrypt** for password hashing with salting
- **CORS Whitelisting** for strict cross-origin access control between frontend and backend
- **Environment Variable Isolation** for all third-party API keys

### ☁️ Optimized Media Pipeline
Integrated Cloudinary API for automated image upload, transformation, and CDN delivery — ensuring doctor profile images are compressed, cached, and served globally with minimal latency.

---

## ⚙️ Local Setup

### Prerequisites
- Node.js `v18+`
- npm `v9+`
- MongoDB Atlas account (or local MongoDB)
- Stripe account (Test Mode)
- Cloudinary account

### 1. Clone the Repository

```bash
git clone https://github.com/akash4550/Prescripto.git
cd Prescripto
```

### 2. Configure Environment Variables

Create a `.env` file inside the `/backend` directory:

```bash
cd backend
cp .env.example .env  # or create manually
```

See the [Environment Variables](#-environment-variables) section below for required keys.

### 3. Install & Run — Backend

```bash
cd backend
npm install
npm start
# Server starts on http://localhost:4000
```

### 4. Install & Run — Frontend (Patient Portal)

```bash
cd frontend
npm install
npm run dev
# App runs on http://localhost:5173
```

### 5. Install & Run — Admin Dashboard

```bash
cd admin
npm install
npm run dev
# Admin runs on http://localhost:5174
```

---

## 🔑 Environment Variables

Create a `.env` file in the `/backend` directory with the following keys:

```env
# ─── Database ─────────────────────────────────────────
MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/prescripto

# ─── Authentication ───────────────────────────────────
JWT_SECRET=your_super_secret_jwt_key

# ─── Stripe Payment Gateway ───────────────────────────
STRIPE_SECRET_KEY=sk_test_your_stripe_secret_key

# ─── Cloudinary Media ─────────────────────────────────
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# ─── Server ───────────────────────────────────────────
PORT=4000
```

> ⚠️ **Never commit your `.env` file.** It's already listed in `.gitignore`.

---

## 📁 Project Structure

```
Prescripto/
│
├── 📁 backend/                  # Node.js + Express API Server
│   ├── 📁 controllers/          # Route logic & business handlers
│   ├── 📁 models/               # Mongoose data schemas
│   ├── 📁 routes/               # API route definitions
│   ├── 📁 middlewares/          # Auth guards & validators
│   ├── 📁 config/               # DB & Cloudinary config
│   └── server.js                # App entry point
│
├── 📁 frontend/                 # Patient Portal (React)
│   ├── 📁 src/
│   │   ├── 📁 pages/            # Route-level page components
│   │   ├── 📁 components/       # Reusable UI components
│   │   └── 📁 context/          # Global state management
│   └── _redirects               # Netlify SPA routing fix
│
├── 📁 admin/                    # Admin + Doctor Dashboard (React)
│   ├── 📁 src/
│   │   ├── 📁 pages/            # Admin & Doctor views
│   │   ├── 📁 components/       # Dashboard UI components
│   │   └── 📁 context/          # Role-aware state management
│   └── _redirects               # Netlify SPA routing fix
│
├── .gitignore
└── README.md
```

---

## 🔐 Admin Access

> **For demo/testing purposes only.**

| Role | Email | Password |
|------|-------|----------|
| **Admin** | `admin@medisync.com` | `rdx12345678` |

Access the Admin Command Center at: [prescriptionadmin.netlify.app](https://prescriptionadmin.netlify.app)

> 💳 **Stripe Test Card:** `4242 4242 4242 4242` — Any future expiry, any 3-digit CVC

---

## 🚀 Deployment

| Service | Platform | Notes |
|---------|----------|-------|
| Frontend (Patient) | Netlify | Auto-deploy from `/frontend`, with `_redirects` for SPA |
| Admin Dashboard | Netlify | Auto-deploy from `/admin`, with `_redirects` for SPA |
| Backend API | Render | Always-on Node.js web service with env vars configured |
| Database | MongoDB Atlas | Free tier M0 cluster, IP-whitelisted |
| Media | Cloudinary | Free tier, auto-compression enabled |

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request

---


