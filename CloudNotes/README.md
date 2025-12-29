# ☁️ CloudNotes

A full-stack note-taking application built with the **MERN** stack (MongoDB, Express, React, Node.js). Create, manage, and organize your notes seamlessly with secure authentication and real-time synchronization.

![React](https://img.shields.io/badge/React-18.3-61DAFB?style=flat-square&logo=react)
![Node.js](https://img.shields.io/badge/Node.js-Express-green?style=flat-square&logo=node.js)
![MongoDB](https://img.shields.io/badge/MongoDB-8.0-green?style=flat-square&logo=mongodb)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Usage](#usage)
- [Key Features Explained](#key-features-explained)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

- **User Authentication**: Secure signup and login with JWT tokens
- **Create Notes**: Add new notes with title and content
- **Edit & Delete**: Modify or remove existing notes
- **User Dashboard**: View all personal notes in an organized dashboard
- **Real-time Updates**: Instant note synchronization
- **Protected Routes**: Secure access to user-specific content
- **Responsive Design**: Beautiful UI with Tailwind CSS and animations using Framer Motion
- **Toast Notifications**: User-friendly feedback with React Hot Toast
- **Error Handling**: Comprehensive error management and logging

## 🛠️ Tech Stack

### Frontend
- **React** 18.3 - UI library
- **Vite** - Fast build tool
- **React Router** - Client-side routing
- **Axios** - HTTP client
- **Tailwind CSS** - Utility-first CSS
- **Framer Motion** - Animation library
- **React Hot Toast** - Notification system
- **Lucide React** - Icon library

### Backend
- **Node.js** - Runtime environment
- **Express** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - ODM library
- **JWT** - Authentication
- **Bcryptjs** - Password hashing
- **CORS** - Cross-origin requests
- **Morgan** - HTTP logging

## 📁 Project Structure

```
CloudNotes/
├── server/                 # Backend server
│   ├── index.js           # Server entry point
│   ├── controllers/       # Route handlers
│   │   ├── authController.js
│   │   └── noteController.js
│   ├── middleware/        # Custom middleware
│   │   └── auth.js
│   ├── models/            # Database schemas
│   │   ├── User.js
│   │   └── Note.js
│   └── routes/            # API routes
│       ├── auth.js
│       └── notes.js
├── src/                   # Frontend React app
│   ├── main.jsx          # Entry point
│   ├── App.jsx           # Main component
│   ├── components/       # Reusable components
│   │   ├── Layout.jsx
│   │   ├── Navbar.jsx
│   │   ├── NoteCard.jsx
│   │   ├── CreateNoteForm.jsx
│   │   ├── Footer.jsx
│   │   └── ProtectedRoute.jsx
│   ├── context/          # React Context
│   │   └── AuthContext.jsx
│   ├── pages/            # Page components
│   │   ├── Home.jsx
│   │   ├── Login.jsx
│   │   ├── Register.jsx
│   │   ├── Dashboard.jsx
│   │   └── NotFound.jsx
│   └── services/         # API services
│       ├── api.js
│       └── noteService.js
├── package.json
├── vite.config.js
├── tailwind.config.js
└── postcss.config.js
```

## 📦 Prerequisites

- **Node.js** v14+ or higher
- **npm** or **yarn** package manager
- **MongoDB** database (local or cloud-based like MongoDB Atlas)

## 🚀 Installation

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd CloudNotes
```

### Step 2: Install Dependencies

**Install backend dependencies:**
```bash
npm install
```

**Install frontend dependencies:**
```bash
npm install
```

### Step 3: Set Up Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
# Server Configuration
PORT=5000
NODE_ENV=development

# Database Configuration
MONGODB_URI=mongodb://localhost:27017/cloudnotes
# Or use MongoDB Atlas:
# MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/cloudnotes?retryWrites=true&w=majority

# JWT Configuration
JWT_SECRET=your_secret_key_here_make_it_long_and_random

# Frontend API URL (if different)
VITE_API_URL=http://localhost:5000
```

## ⚙️ Configuration

### MongoDB Setup

**Option 1: Local MongoDB**
```bash
# Install MongoDB Community Edition
# Start MongoDB service
mongod
```

**Option 2: MongoDB Atlas (Cloud)**
1. Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create an account and cluster
3. Get your connection string
4. Add it to your `.env` file

### Port Configuration
- Backend server runs on: `http://localhost:5000`
- Frontend development runs on: `http://localhost:5173`

## ▶️ Running the Application

### Option 1: Run Both Frontend and Backend Concurrently
```bash
npm run dev:all
```

### Option 2: Run Separately

**Terminal 1 - Start Backend Server:**
```bash
npm run server
```

**Terminal 2 - Start Frontend Development Server:**
```bash
npm run dev
```

### Build for Production
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

## 📡 API Endpoints

### Authentication Routes (`/api/auth`)
- `POST /register` - Create new user account
- `POST /login` - User login
- `POST /logout` - User logout

### Note Routes (`/api/notes`)
- `GET /` - Get all notes for authenticated user
- `POST /` - Create a new note
- `GET /:id` - Get specific note
- `PUT /:id` - Update note
- `DELETE /:id` - Delete note

## 💡 Usage

### Create an Account
1. Click "Register" on the home page
2. Enter email and password
3. Click "Sign Up"

### Create a Note
1. Log in to your account
2. Navigate to Dashboard
3. Click "Create New Note"
4. Enter title and content
5. Click "Save Note"

### Manage Notes
- **View**: All notes appear on the dashboard
- **Edit**: Click on a note and modify its content
- **Delete**: Click the delete button to remove a note

## 🔑 Key Features Explained

### Protected Routes
The application uses `ProtectedRoute` component to ensure only authenticated users can access the dashboard.

### JWT Authentication
Tokens are stored in localStorage and sent with each API request via Authorization header.

### Real-time Updates
Note changes are immediately reflected across all components using React state management.

### Error Handling
Comprehensive try-catch blocks and error middleware provide detailed feedback for debugging.

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**Made with ❤️ using MERN Stack**
