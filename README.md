## 🍲 Hope Food Management System

A full-stack food donation and food-waste-reduction platform that connects people with surplus food (Donors) to people who need it (Receivers), with Volunteers to help coordinate pickup/transport. Built with the MERN stack and real-time chat.

## 📖 About the Project

Every day, usable food goes to waste while others go hungry.  
**Hope** bridges that gap by enabling donors to quickly list surplus food — with details like quantity, category, expiry, and location — and allowing nearby receivers to browse and claim it.  

Once claimed, donors and receivers can **chat in real time** to coordinate handoff, and afterward **rate each other** to build trust within the community.


## ✨ Key Features

- 🔐 Secure signup/login 
- 🎭 Role-based accounts: Donor, Receiver, Volunteer, Admin
- 🥗 Food listings by category (Veg, Non-Veg, Drinks, Snacks, Leftovers)
- 📍 Location-aware posts with **Leaflet maps**
- 🖼️ Image uploads for listings & avatars (**Multer**)
- 💬 Real-time donor ↔ receiver chat (**Socket.io**)
- 🔔 Instant notifications for new messages
- ⭐ Ratings & reviews to build user trust
- ⏱️ Auto-removal of expired listings
- 🌐 Multi-language support with context switcher
- 🚚 Volunteer dashboard for pickup tasks


##  Tech Stack

### Frontend
- React 19 + Vite (fast build tool & dev server)
- React Router v7 (client-side routing)
- Tailwind CSS v4 (utility-first styling)
- Axios (HTTP requests)
- Socket.io-client (real-time communication)
- Leaflet / React-Leaflet (interactive maps)
- GSAP & Framer Motion (animations)
- Lucide React (modern icons)

### Backend
- Node.js + Express 5 (REST APIs)
- MongoDB with Mongoose (database modeling)
- Socket.io (real-time chat & notifications)
- Multer (file uploads)
- bcryptjs (password hashing)
- dotenv (environment configuration)


🏗️ Architecture

```text
React (Vite) Frontend  ──REST API (Axios)──▶  Express Server ──Mongoose──▶ MongoDB Atlas
        ▲                                            │
        └──────────── WebSocket (Socket.io) ─────────┘

```
        
The frontend is a single-page React app served by Vite, communicating with the backend via REST for data and Socket.io for real-time chat/notifications.
The backend is an Express server following an MVC-style structure (models → controllers → routes), backed by MongoDB Atlas.
Uploaded images are served statically from the backend's /uploads directory.


# 📁 Project Structure

```text
Hope-Food-Management-System/
│
├── backend/
│   ├── controllers/        # Business logic (auth, donate, order)
│   ├── models/             # Mongoose schemas (User, Food, Donate, Chat, Review)
│   ├── routes/             # Express route definitions
│   ├── uploads/            # Uploaded images (food photos, avatars)
│   ├── server.js           # App entry point (Express + Socket.io + DB)
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── pages/           # Route-level pages (Home, Login, Order, Chat)
│   │   ├── donate/          # Donor-facing forms
│   │   ├── order/           # Receiver-facing pages
│   │   ├── components/      # Reusable UI components
│   │   ├── context/         # Language context/provider
│   │   ├── App.jsx
│   │   └── main.jsx
│   │
│   └── package.json
│
└── README.md
```

# 🔄 Application Workflow

Donor
  |
  |
Creates Food Donation
  |
  |
Food Stored in Database
  |
  |
Receiver Searches Food
  |
  |
Receiver Claims Donation
  |
  |
Real-Time Chat
  |
  |
Food Pickup / Delivery
  |
  |
Rating & Review

# 🔮 Future Enhancements


- 🤖 AI-based donor-receiver matching
- 📱 Mobile application using React Native
- 🔔 Push notifications
- 🗺️ Smart delivery route optimization
- 📊 Donation analytics dashboard
- 🏢 NGO partnership integration
- 📦 QR based food pickup verification

# 🌍 Social Impact


This project contributes towards:

### Sustainable Development Goal 2
**Zero Hunger**

### Sustainable Development Goal 12
**Responsible Consumption and Production**


The system helps:

- Reduce food wastage
- Improve food accessibility
- Encourage community participation
- Build a sustainable donation network


