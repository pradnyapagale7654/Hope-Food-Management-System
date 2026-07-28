🍲 Hope Food Management System

A full-stack food donation and food-waste-reduction platform that connects people with surplus food (Donors) to people who need it (Receivers), with Volunteers to help coordinate pickup/transport. Built with the MERN stack and real-time chat.

📖 About the Project

Every day, usable food goes to waste while others go hungry. Hope bridges that gap by letting donors quickly list surplus food — with quantity, category, expiry, and location — and letting nearby receivers browse and claim it. Once claimed, a donor and receiver can chat in real time to coordinate handoff, and afterward rate each other to build trust in the community.

Key Features
🔐 User authentication — signup/login with hashed passwords (bcrypt)
🎭 Role-based accounts — Donor, Receiver, Volunteer, Admin
🥗 Food listings by category — Veg, Non-Veg, Drinks, Snacks, Celebration/leftovers
📍 Location-aware listings — map view via Leaflet, latitude/longitude on each post
🖼️ Image uploads for food listings and user avatars (Multer)
💬 Real-time chat between donor and receiver per food item (Socket.io)
🔔 Live notifications when a new message arrives
⭐ Ratings & reviews — post-transaction feedback builds a trust score per user
⏱️ Automatic cleanup — expired food listings are removed automatically
🌐 Multi-language support via a language context/switcher
🚚 Volunteer dashboard to view available pickup tasks

# Frontend

React 19 + Vite
React Router v7
Tailwind CSS v4
Axios
Socket.io-client
Leaflet / React-Leaflet (maps)
GSAP & Framer Motion (animations)
Lucide React (icons)

# Backend

Node.js + Express 5
MongoDB with Mongoose
Socket.io (real-time chat & notifications)
Multer (file uploads)
bcryptjs (password hashing)
dotenv (environment config)

🏗️ Architecture

React (Vite) Frontend  ──REST API (Axios)──▶  Express Server ──Mongoose──▶ MongoDB Atlas
        ▲                                            │
        └──────────── WebSocket (Socket.io) ─────────┘
        
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


