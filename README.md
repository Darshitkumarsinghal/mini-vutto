# 🚲 Mini Vutto – Used Bike Listings Platform

A full-stack web application for browsing, adding, and managing used bike listings.  
Built as a simplified version of **Vutto** — focusing on clean code, authentication, and a usable UI.

---

## ✨ Features

- **User Authentication** (JWT-based)
  - Register & Login with email/password
- **Bike Listings**
  - View all bikes with search by brand/model
  - View individual bike details
- **Manage Listings**
  - Add a new bike (authenticated users only)
  - Edit or delete own listings
- **User Dashboard**
  - "My Listings" page to manage bikes added by logged-in user
- **Responsive UI**
  - Works on desktop & mobile

---

## 🛠️ Tech Stack

### Backend
- Node.js + Express
- MongoDB (Atlas)
- JWT Authentication
- CORS & Validation Middleware
- Hosted on **Render**

### Frontend
- React (Vite)
- Axios for API calls
- Tailwind CSS (for styling)
- Hosted on **Vercel**

---

## 📂 Project Structure

```
mini-vutto/
├── backend/
│   ├── src/
│   │   ├── config/
│   │   │   └── db.js
│   │   ├── models/
│   │   │   ├── User.js
│   │   │   └── Bike.js
│   │   ├── routes/
│   │   │   ├── auth.js
│   │   │   └── bikes.js
│   │   ├── validators/
│   │   │   ├── auth.js
│   │   │   └── bike.js
│   │   └── middleware/
│   │       └── auth.js
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   ├── lib/
│   │   ├── main.jsx
|   |   |--- styles.css
│   │   └── App.jsx
│   ├── index.html
│   ├── vite.config.js
│   └── package.json
│
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone Repository
```bash
git clone https://github.com/Darshitkumarsinghal/mini-vutto
cd mini-vutto
```

### 2. Backend Setup
```bash
cd backend
npm install
```

Create `.env` file in `backend/`:
```env
PORT=5002
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
CLIENT_ORIGIN=http://localhost:5173
```

Start backend:
```bash
npm run dev
```

---

### 3. Frontend Setup
```bash
cd frontend
npm install
```

Create `.env` file in `frontend/`:
```env
VITE_API_BASE=http://localhost:5002
```

Start frontend:
```bash
npm run dev
```

---

### 4. Access App
- Backend: `http://localhost:5002`
- Frontend: `http://localhost:5173`

---

## 🚀 Deployment

### Backend (Render)
1. Push backend folder to GitHub.
2. Create a new **Render Web Service** → link repo.
3. Add environment variables (same as `.env`).
4. Deploy → get live API URL (e.g., `https://vutto-backend.onrender.com`).

### Frontend (Vercel)
1. Push frontend folder to GitHub.
2. Import repo in **Vercel**.
3. Add environment variable in Vercel:
   ```env
   VITE_API_BASE=https://vutto-backend.onrender.com
   ```
4. Deploy → get live frontend URL.

---

## 📖 Approach

The project was implemented using a **clean separation of concerns**:

- **Backend**:  
  - RESTful API in Express  
  - MongoDB for persistence  
  - JWT-based authentication  
  - Middleware for validation & authorization  
  - CORS configured to allow frontend origin  

- **Frontend**:  
  - React app with pages for Auth, Listings, Details, and My Listings  
  - Axios wrapper to handle API requests with `VITE_API_BASE` env  
  - Tailwind CSS for responsive UI  

- **Deployment**:  
  - Backend on Render (Node.js service)  
  - Frontend on Vercel (React build)  
  - Environment variables for seamless integration between FE + BE  

This ensures the app runs **locally for dev** and **scales on cloud platforms** for demo or production.

---

## 📹 Demo

- **Backend**: [https://vutto-backend.onrender.com](https://vutto-backend.onrender.com)  
- **Frontend**: [https://vutto-frontend-orpin.vercel.app](https://vutto-frontend-orpin.vercel.app) 
- **Demo video**: [https://drive.google.com/file/d/1RvgtXEjJUNihVAkk45lPQ1Nw8Y3mMZ59/view?usp=sharing](https://drive.google.com/file/d/1RvgtXEjJUNihVAkk45lPQ1Nw8Y3mMZ59/view?usp=sharing)
