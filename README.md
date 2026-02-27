# ♻️ Parivartan – Smart Waste Management Platform

> **Turning Awareness into Action — One Household at a Time**

Parivartan is an AI-powered, technology-driven waste management platform that digitally connects **citizens**, **waste collection partners**, and **administrators** in one unified ecosystem. It promotes proper solid waste segregation at source, real-time pickup tracking, environmental impact monitoring, and reward-based participation — aligned with India's **Swachh Bharat Mission**.

---

## 🌍 The Problem We Solve

India generates over **62 million tonnes** of waste annually. Despite cleanliness campaigns, the most critical step — **segregation at source** — remains widely ignored.

- Households mix biodegradable, plastic, and recyclable waste
- Recyclable materials end up in landfills due to improper separation
- Rural and semi-urban areas lack structured digital waste solutions
- No single platform connects citizens, collectors, and recyclers

**Parivartan bridges this gap.**

---

## 🔄 How It Works

### 👤 User Flow
1. Register / Log in to the app
2. Upload a waste image (optional)
3. AI identifies and suggests the correct waste category
4. Schedule a pickup — select category, address, and time
5. Request is stored in Firestore; nearby partner gets notified
6. Track pickup status in real time
7. Partner collects waste and marks request as completed
8. User receives confirmation + reward points
9. Environmental impact dashboard is updated automatically

### 👨‍💼 Partner Flow
1. Register as a collection partner
2. Admin verifies and approves the partner account
3. View assigned waste pickup requests on dashboard
4. Accept request and navigate to pickup location
5. Update status: `Assigned → In Progress → Completed`
6. Earn reward points for successful collections
7. Collection data syncs with admin analytics panel

### 🧑‍💻 Admin Flow
1. Log into admin dashboard
2. Review and approve partner registrations
3. Monitor all active and completed pickup requests
4. Track waste collection statistics and CO₂ reduction metrics
5. Manage rewards, users, and system settings

---

## ✨ Key Features

### 🤖 AI-Based Waste Identification
- Upload an image of your waste
- AI model suggests the correct category (Dry / Wet / E-waste / Plastic)
- Encourages proper segregation at source

### 📍 Real-Time Tracking
- Live tracking of assigned waste collection partners
- Status updates at every stage of the pickup process
- Instant confirmation after collection

### 🎖️ Reward System
- Users earn points for responsible waste segregation
- Partners earn points for successful pickups
- Points redeemable for vouchers and incentives

### 🌱 Environmental Impact Dashboard
- Personal contribution metrics per user
- Total CO₂ reduction tracked across the platform
- Area-wise collection performance analytics

### 🔐 Role-Based Access Control
- Separate secure portals for Citizens, Partners, and Admins
- Firebase Authentication with admin approval workflow
- Verified partner onboarding system

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18, TypeScript, Vite |
| Mobile | Expo, React Native, TypeScript |
| Styling | Tailwind CSS |
| Backend | Firebase (Authentication + Firestore) |
| File Storage | Cloudinary |
| Charts & Analytics | Recharts |
| Routing | React Router |
| On-Device AI | TensorFlow Lite |
| Cloud AI | Google Gemini | 
| APIReal-Time Processing | Pathway|

---

---

## 🤖 AI & Intelligence Layer
Parivartan uses a multi-model AI architecture combining on-device inference, cloud intelligence, and real-time data processing.

### 1️⃣ On-Device AI — TensorFlow Lite (Mobile App)
The mobile app runs a TensorFlow Lite model directly on the user's device for instant waste image classification — no internet required.
Feature     Detail
Model Type  Image Classification (Waste Categories)
Framework   TensorFlow LiteWorks 
Offline     ✅ Yes
Categories  Plastic / Paper / Metal

#### Why TensorFlow Lite?

Optimized and lightweight for mobile hardware
Offline capability — works in low-connectivity rural areas
Faster response with no server round-trip
Reduces backend load and cost


### 2️⃣ Cloud AI — Gemini API (Web Platform)
The web platform integrates Google Gemini for higher-level intelligence and data-driven insights beyond simple classification.

#### Gemini powers:

📊 Intelligent waste analytics and trend detection
🌱 Environmental impact suggestions and recommendations
🧠 AI-powered decision support for administrators
📈 Smart performance insights for collection partners


### 3️⃣ Real-Time Data Processing — Pathway
Pathway handles all live data streaming and dynamic analytics across the platform.

#### Pathway enables:

⚡ Real-time waste data streaming as pickups happen
📡 Live analytics generation across all user activity
🌍 Dynamic environmental impact metrics (CO₂ reduction)
📊 Performance tracking updated without page refresh

---

---
## 📁 Project Structure
```
Parivaratan-full/
│
├── Imagine/                          # 🌐 Web Application (React + Vite)
│   ├── src/
│   │   ├── components/               # Reusable UI components
│   │   │   ├── admin/                # Admin panel components
│   │   │   ├── partner/              # Partner dashboard components
│   │   │   └── shared/               # Shared/common components
│   │   ├── pages/                    # Route-level pages
│   │   │   ├── AdminDashboard.tsx
│   │   │   ├── PartnerDashboard.tsx
│   │   │   └── Login.tsx
│   │   ├── services/                 # Firebase & API calls
│   │   │   ├── firebase.ts
│   │   │   ├── auth.ts
│   │   │   └── gemini.ts
│   │   ├── hooks/                    # Custom React hooks
│   │   ├── context/                  # React context & state
│   │   ├── utils/                    # Helper functions
│   │   └── main.tsx                  # App entry point
│   ├── public/                       # Static assets
│   ├── index.html
│   ├── vite.config.ts
│   ├── tailwind.config.js
│   ├── tsconfig.json
│   ├── package.json
│   └── .env.example                  # Environment variable template
│
├── Parivartan/                       # 📱 Mobile Application (Expo + React Native)
│   ├── app/                          # Expo Router screens
│   │   ├── (tabs)/                   # Bottom tab navigation
│   │   ├── pickup/                   # Pickup scheduling screens
│   │   ├── tracking/                 # Real-time tracking screens
│   │   └── rewards/                  # Rewards & points screens
│   ├── components/                   # Reusable mobile components
│   ├── services/                     # Firebase & TensorFlow Lite services
│   │   ├── firebase.ts
│   │   ├── wasteClassifier.ts        # TensorFlow Lite AI model
│   │   └── pathway.ts                # Real-time data streaming
│   ├── assets/                       # Images, icons, fonts
│   │   └── ml-model/                 # TFLite model files
│   │       └── waste_classifier.tflite
│   ├── hooks/
│   ├── constants/
│   ├── app.json
│   ├── package.json
│   └── tsconfig.json
│
└── README.md
```

---

## ⚙️ Getting Started

### Prerequisites
- Node.js v18+
- npm or yarn
- Firebase project with Firestore enabled
- Cloudinary account

### 1. Clone the Repository
```bash
git clone https://github.com/alpana11/parivartan.git
cd parivartan
```

### 2. Setup Frontend (Web App)
```bash
cd frontend
npm install
cp .env.example .env
# Add your Firebase and Cloudinary credentials to .env
npm run dev
```

### 3. Setup Mobile App
```bash
cd mobile
npm install
npx expo start
```

### 4. Environment Variables
Create a `.env` file in `/frontend` with:
```env
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_storage_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
VITE_CLOUDINARY_CLOUD_NAME=your_cloudinary_name
```

---

## 🗺️ Roadmap

- [x] User waste pickup scheduling
- [x] AI-based waste category identification
- [x] Real-time pickup tracking
- [x] Partner and Admin dashboards
- [x] Reward points system
- [x] Offline mode for low-connectivity areas
- [x] Carbon credit tracking

---

## 📊 Market Opportunity

- India's waste management market: **₹35,000+ crore**
- Target: **500+ Tier 2 and Tier 3 cities** — starting with Marathwada region
- Aligned with **Swachh Bharat Mission 2.0** national goals
- Addresses 62 million tonnes of annual solid waste generation

---

## 👥 Team

| Name | Role | GitHub |
|------|------|--------|
| [Alpana Pardesi] | Web Developer | [@alpana11](https://github.com/alpana11) |
| [Kishori Birari] | Backend Developer | [@kishori-12](https://github.com/Kishori-12) |
| [Shraddha Pawar] | Mobile Developer | [@ShraddhaPawar05](https://github.com/ShraddhaPawar05) |

---

## 🙏 Acknowledgements

- [Swachh Bharat Mission](https://swachhbharat.mygov.in/) for inspiring this initiative
- The citizens of Chhatrapati Sambhajinagar for motivating us to act
- All open-source contributors whose tools power this project

---

<div align="center">
  <strong>Parivartan — Not just an app. A responsibility.</strong><br/>
  Made with ❤️ for a cleaner, greener Bharat 🇮🇳
</div>
