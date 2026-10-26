# BugTracker - Issue Management System

A full-stack Bug Tracking System built with **Node.js, Express.js, MongoDB (Mongoose)** on the backend, and **Vanilla HTML, CSS, and JavaScript** on the frontend.

---

## Features

1. **Authentication & Authorization:**
   - User registration and login.
   - Password hashing with bcrypt.
   - JWT authentication middleware protecting backend routes.
   - Persistent user sessions via localStorage.

2. **Bug Management (CRUD):**
   - **Report:** Create new bugs with Title, Description, Priority (Low, Medium, High), and Status (Open, In Progress, Resolved).
   - **Track:** Real-time dashboard with search, status filtering, priority filtering, and sorting.
   - **Update:** View bug details, update bug information, or change status directly.
   - **Delete:** Remove bugs with confirmation.

3. **Metrics Overview:**
   - Counts for Total, Open, In Progress, Resolved, and High Priority bugs.

---

## Project Structure

```
mp/
├── package.json
├── vercel.json
├── .env.example
├── .env
├── .gitignore
├── README.md
├── api/
│   └── index.js
├── src/
│   ├── config/
│   │   └── db.js
│   ├── middleware/
│   │   └── auth.js
│   ├── models/
│   │   ├── User.js
│   │   └── Bug.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   └── bugRoutes.js
│   ├── seed.js
│   └── server.js
└── public/
    ├── index.html
    ├── css/
    │   └── styles.css
    └── js/
        └── app.js
```

---

## Setup & Running

### 1. Install Dependencies
```bash
npm install
```

### 2. Configure Environment
Set `MONGODB_URI` and `JWT_SECRET` in `.env`:
```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

### 3. Start Local Server
```bash
npm start
```
Open `http://localhost:5000` in your browser.

---

## Deploying to Vercel

1. Push the repository to GitHub.
2. In the Vercel Dashboard, import the repository.
3. In **Settings > Environment Variables**, add:
   - `MONGODB_URI`: your MongoDB Atlas connection string (with your real password)
   - `JWT_SECRET`: your secret key
4. In MongoDB Atlas, ensure **Network Access** allows `0.0.0.0/0`.
5. Deploy.
