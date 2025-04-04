# 📝 EasyNotes
EasyNotes is a full-stack note-taking application built with the MERN stack (MongoDB, Express, React, Node.js). It allows users to securely register, log in, create, edit, pin, search, and delete notes. Clean UI, responsive design, and powerful note management all in one.

## 🚀 Live Demo
Access the live app here: [EasyNotes](https://easynotesks.netlify.app/)

## ✨ Features
- JWT-Based User Authentication
- Create, Edit, Delete, and Pin Notes
- Pinned Notes Always Display First
- Search Notes by Title or Content
- Fully Responsive for All Devices
- Toast Notifications for User Feedback
  
## 🛠 Tech Stack
- Frontend: React.js (Vite), Tailwind CSS
- Backend: Node.js, Express.js
- Database: MongoDB (Atlas)
- Hosting: Netlify (Frontend), Local/Cloud (Backend)

## Installation Instructions
### Prerequisites
**Ensure you have the following installed:**
- Node.js (v18+)
- MongoDB (Atlas)

### Backend Setup

1. **Clone the Repository:**
   ```bash
   https://github.com/karanshah1561998/EasyNotes.git
   cd easynotes
   
2. **Install dependencies:**
   ```bash
   cd easynotes/frontend/easynotes
   npm install

   cd easynotes/backend
   npm install
   
3. **Set up environment variables:**
   Create a `.env` file in the easynotes/backend directory and add:
   ```bash
   MONGO_CONNECTION_STRING = your_mongo_connection_string
   ACCESS_TOKEN_SECRET = your_jwt_secret

4. **Navigate to the backend directory and start the backend server:**
   ```bash
   cd easynotes/backend
   npm run dev

5. **Navigate to the frontend/easynotes directory and start the React app:**
   ```bash
   cd easynotes/frontend/easynotes
   npm run dev
   
   Open http://localhost:5173 to view the app in your browser.

## 🧩 Troubleshooting

### 1. Server Not Starting
- Confirm the `.env` file exists in the backend folder.
- Ensure `MONGO_CONNECTION_STRING` and `ACCESS_TOKEN_SECRET` are set correctly.
- Make sure your MongoDB cluster is accessible and not paused.

### 2. JWT Authentication Issues
- Check for expired or invalid JWT tokens.
- Make sure the token is stored correctly in `localStorage` and sent in the Authorization header.
- Verify that protected routes on the backend require authentication properly.

### 3. Notes Not Loading
- Confirm that the backend server is running at `http://localhost:8000`.
- Check that frontend API requests are targeting the correct backend URL.
- Ensure CORS is configured correctly in the Express server.

### 4. CORS Errors
- Make sure you're using the `cors` middleware in your Express app.
- Set `Access-Control-Allow-Origin` to the correct frontend origin (e.g., `http://localhost:5173`).

### 5. Environment Variables Not Working
- Restart the server after creating or updating the `.env` file.
- Double-check for typos or missing variables.
