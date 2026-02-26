# ♻️ Parivartan – Smart Waste Management Platform  

Parivartan is a technology-driven waste management platform that connects citizens, waste collection partners, and administrators in one unified system.  

It promotes proper solid waste segregation, real-time tracking, environmental impact monitoring, and reward-based participation.

---

# 🔄 System Pathway (How It Works)

## 👤 User Flow

1. User registers / logs in.
2. User uploads waste image (optional).
3. AI suggests correct waste category.
4. User schedules pickup (select category, address, time).
5. Request is stored in Firestore database.
6. Nearby approved partner gets notification.
7. User can track pickup status in real time.
8. Partner collects waste and marks request as completed.
9. User receives confirmation and reward points.
10. Environmental impact data is updated on dashboard.

---

## 👨‍💼 Partner Flow

1. Partner registers on platform.
2. Admin verifies and approves partner.
3. Partner logs into dashboard.
4. Views assigned waste pickup requests.
5. Accepts request and navigates to pickup location.
6. Updates status: Assigned → In Progress → Completed.
7. Earns reward points for successful collection.
8. Collection data updates in admin analytics panel.

---

## 🧑‍💻 Admin Flow

1. Admin logs into admin dashboard.
2. Reviews and approves partner registrations.
3. Monitors all pickup requests.
4. Tracks waste collection statistics.
5. Analyzes environmental impact (CO₂ reduction).
6. Manages rewards and system settings.

---

# 👨‍💼 Partner & Admin Panel  

This module is designed for waste collection partners and system administrators.

## 🔐 Authentication & Approval  
- Secure login/signup using Firebase Authentication  
- Admin approval system for partner verification  
- Role-based access control (Admin / Partner)

## 📦 Waste Request Management  
- View assigned waste pickup requests  
- Accept or reject requests  
- Update status (Assigned → In Progress → Completed)  
- Track pickup history  

## 📊 Real-Time Dashboard  
- Monitor active and completed requests  
- View total waste collected  
- Track CO₂ reduction metrics  
- Analyze area-wise performance  

## 🗺️ Route & Location Tracking  
- View user pickup locations  
- Plan optimized collection routes  
- Real-time request tracking  

## 🎁 Rewards & Incentives  
- Earn reward points for completed pickups  
- Redeem points for vouchers  
- View transaction history  

## 👤 Profile & Verification  
- Manage organization details  
- Upload verification documents  
- Track approval status  

---

# 👤 User Panel  

This module is designed for citizens who want to dispose of waste responsibly.

## 📝 Request Waste Pickup  
- Schedule waste collection  
- Select waste category (Dry / Wet / E-waste / Plastic)  
- Add pickup address and preferred time  

## 🤖 AI-Based Waste Identification  
- Upload image of waste  
- AI suggests correct waste category  
- Encourages proper segregation at source  

## 📍 Real-Time Tracking  
- Track assigned partner  
- View pickup status updates  
- Get confirmation after collection  

## 🌱 Impact Awareness  
- View personal contribution to waste reduction  
- Track environmental impact metrics  

## 🎖️ Reward System  
- Earn points for proper segregation  
- Redeem rewards and vouchers  
- Encourage responsible behavior  

---

# 🛠️ Tech Stack  

Frontend: React 18, TypeScript, Vite  
Styling: Tailwind CSS  
Backend: Firebase (Authentication, Firestore)  
File Storage: Cloudinary  
Charts: Recharts  
Routing: React Router  

---

# 🎯 Vision  

Parivartan is more than a waste management app.  
It is a digital ecosystem that builds accountability, encourages segregation at source, and creates a sustainable connection between citizens and waste management partners.

Together, we move toward a cleaner and greener future.
