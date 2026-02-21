🏥 Prescripto | Healthcare Orchestration Platform
Prescripto is a production-grade healthcare ecosystem engineered to bridge the gap between patients and medical professionals. Unlike standard booking apps, it utilizes a triple-dashboard architecture and an atomic slot-booking engine to ensure data integrity and a seamless user experience.

🛰️ Live Ecosystem
Patient Hub: prescriipto.netlify.app

Admin Command Center: prescriptionadmin.netlify.app

🏗️ Technical Architecture & Impact
1. Atomic Slot-Booking Logic
To eliminate the risk of "double-booking" during high-traffic periods, I engineered an atomic verification engine. The system performs a real-time availability check at the database level immediately before transaction finalization, preventing race conditions.

2. Advanced Deployment & DevOps
The platform is deployed as a distributed system across Netlify (Frontend) and Render (Backend).

SPA Persistence: Solved the common "404 Not Found" refresh error on static hosting by configuring custom redirect rules to handle the React Router lifecycle at the edge.

CORS & Sync: Successfully navigated complex cross-origin resource sharing (CORS) and environment synchronization challenges between disparate hosting providers.

3. Multi-Role RBAC (Role-Based Access Control)
Implemented a granular security model using JWT and Bcrypt, providing distinct, isolated environments for three key stakeholders:

Patients: Self-service discovery, profile management, and appointment history.

Doctors: Consultation tracking, availability orchestration, and earnings analytics.

Admins: Global system oversight, provider onboarding, and appointment auditing.

🛠️ Tech Stack
Frontend: React.js, Tailwind CSS

Backend: Node.js, Express.js

Database: MongoDB Atlas (Cloud)

Payment: Stripe SDK (Test Mode)

Media: Cloudinary CDN for optimized asset delivery

🚀 Key Features
Smart Discovery: Real-time doctor filtering by specialty and availability.

FinTech Integration: Secure payment processing via Stripe for instant booking confirmation.

Real-time Analytics: Integrated dashboards for doctors to monitor their professional growth and consultation metrics.

⚙️ Local Setup
Clone the Repository:

Bash
git clone https://github.com/Akshay-Lakwal/prescripto.git
Environment Configuration:
Create a .env in the backend directory with keys for MONGODB_URI, JWT_SECRET, STRIPE_SECRET_KEY, and CLOUDINARY credentials.

Install & Run:

Bash
# For Backend
cd backend && npm install && npm start
# For Frontend
cd frontend && npm install && npm run dev
