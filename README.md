# EasyNotes

EasyNotes is a full-stack note-taking application built with the **MERN stack** (MongoDB, Express, React, Node.js). This application enables users to register, log in, create, edit, pin, and delete notes. Additionally, users can search their notes by keywords.

## Live Demo

Access the live app here: [EasyNotes](https://easynotesks.netlify.app/)

## Features

1. **User Authentication**
   - Secure user registration and login.
   - Protected routes, accessible only by authenticated users.
   - Authentication with JWT (JSON Web Tokens) for secure access to user-specific data.

2. **CRUD Operations for Notes**
   - **Create, Read, Update, and Delete** notes.
   - Notes are stored in MongoDB and are user-specific.

3. **Pin/Unpin Notes**
   - Users can toggle the "pinned" status of notes.
   - Pinned notes appear at the top of the notes list for easy access.

4. **Search and Filter**
   - Search for notes by keywords in the title or content.

5. **Responsive Design**
   - The application is responsive and compatible with mobile and desktop views.

6. **Toast Notifications**
   - Provides feedback on actions such as creating, updating, and deleting notes.
  
## How to Use

- **Sign Up**: Register with a unique email and password.
- **Log In**: Access the app with your credentials.
- **Add a Note**: Click the "Add Note" button to create a new note with a title, content, and optional tags.
- **Edit a Note**: Click on a note to edit its details.
- **Pin/Unpin a Note**: Toggle the pinned status to prioritize a note at the top.
- **Search**: Use the search bar to find specific notes by keywords.

## Installation Instructions

### Prerequisites
Ensure you have the following installed:
- **Node.js** (v14+)
- **MongoDB** (local instance or MongoDB Atlas)

### Backend Setup

1. **Clone the Repository:**
   
   ```bash
   git clone https://github.com/your-username/easynotes.git
   cd easynotes/backend
   
2. **Install backend dependencies:**
   
   ```bash
   npm install
   
3. **Create a .env file in the backend directory:**
   
   ```bash
   MONGO_CONNECTION_STRING = your_mongo_connection_string
   ACCESS_TOKEN_SECRET = your_jwt_secret
   
4. **Start the backend server:**

   ```bash
   npm start

  **The backend server will run on http://localhost:8000.**

### Frontend Setup

1. **Navigate to the frontend folder:**
   
   ```bash
   cd ../frontend/easynotes
   
2. **Install frontend dependencies:**
   
   ```bash
   npm install

3. **Start the Frontend Server:**
   
   ```bash
   npm run dev

  **Open http://localhost:5173 to view the app in your browser.**

## API Endpoints

### Authentication
- **POST** `/create-account` - Register a new user
- **POST** `/login` - Log in an existing user
- **GET** `/get-user` - Retrieve authenticated user's details

### Notes
- **POST** `/add-note` - Add a new note
- **GET** `/get-all-notes` - Retrieve all notes for the logged-in/authenticated user
- **PUT** `/edit-note/:noteId` - Edit an existing note
- **PUT** `/update-note-pinned/:noteId` - Toggle the pinned status of a note
- **DELETE** `/delete-note/:noteId` - Delete a note by ID
- **GET** `/search-notes` - Search notes by title or content

## Future Enhancements

- **Tag-Based Filtering**: Users can categorize and filter notes by tags.
- **Rich Text Editing**: Support for bold, italic, and other formatting in notes.
- **Reminders and Notifications**: Set reminders for notes and receive notifications.

## Troubleshooting

- **Server Not Starting**: Ensure `MONGO_CONNECTION_STRING` and `ACCESS_TOKEN_SECRET` are set correctly in `.env`.
- **JWT Authentication Issues**: If you’re frequently redirected to log in, verify the localStorage token storage in the front end.
- **Unable to Fetch Notes**: Confirm that the backend server is running on port 8000 and that CORS is configured properly.
