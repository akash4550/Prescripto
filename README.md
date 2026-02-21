🏥 Prescripto: Healthcare Orchestration Engine
Full-Stack Enterprise Appointment System
Prescripto is a production-grade healthcare orchestration platform engineered to solve the "double-booking" concurrency problem in medical scheduling. It features a triple-dashboard architecture (Patient, Doctor, Admin) and a robust, state-managed booking pipeline.

🛰️ Live Ecosystem
Patient Hub: prescriipto.netlify.app

Admin Command Center: prescriptionadmin.netlify.app

🛠️ Engineering Deep-Dive
1. Concurrency & Atomic Slot-Booking
To prevent race conditions, I engineered an atomic slot-booking logic. Unlike standard CRUD operations, this system verifies slot availability at the database level before confirmation, mathematically eliminating "double-booking" errors during high-traffic periods.

2. Deployment Architecture & DevOps
The application is deployed as a distributed system across Netlify (Frontend/Admin) and Render (Backend).

CORS Management: Successfully navigated complex cross-origin resource sharing and environment synchronization between distinct hosting providers.

Persistence: Configured custom edge-node redirect rules to handle the React Router lifecycle, ensuring zero "404 Not Found" errors on page refresh.

3. Multi-Role Security Model
Implemented a granular Role-Based Access Control (RBAC) system using JWT and Bcrypt. This ensures strict data isolation between:

Patients: Personal medical history and booking management.

Doctors: Availability orchestration and earnings analytics.

Admins: Global system oversight and provider onboarding.

🚀 Key Features
Smart Filtering: Real-time doctor discovery filtered by specialty.

Doctor Dashboard: Specialized view for tracking consultations and managing individual availability.

Payment Integration: Secure transaction processing via Stripe (Test Mode) for instant confirmations.

Cloud Media Assets: Cloudinary CDN integration for high-resolution, optimized doctor profile imagery.

📦 Technical Stack
Frontend: React.js, Tailwind CSS

Backend: Node.js (Runtime), Express.js (Framework)

Database: MongoDB Atlas (NoSQL)

Infrastructure: Cloudinary (Media), Stripe (FinTech), JWT (Security)

⚙️ Development Setup
Clone the Repo: git clone https://github.com/Akshay-Lakwal/prescripto.git

Environment Configuration:
Create a .env in the backend directory:

Code snippet
MONGODB_URI=your_uri
JWT_SECRET=your_secret
CLOUDINARY_NAME=your_name
STRIPE_SECRET_KEY=your_key
Execute:
npm run dev
