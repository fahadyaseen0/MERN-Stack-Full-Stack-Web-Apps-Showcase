# 🏥 Doctor Appointment System

A comprehensive full-stack web application for managing doctor appointments, scheduling consultations, and tracking medical professionals. Built with the **MERN** stack with real-time updates using Socket.IO.

![React](https://img.shields.io/badge/React-18.2-61DAFB?style=flat-square&logo=react)
![Node.js](https://img.shields.io/badge/Node.js-Express-green?style=flat-square&logo=node.js)
![MongoDB](https://img.shields.io/badge/MongoDB-8.0-green?style=flat-square&logo=mongodb)
![Socket.IO](https://img.shields.io/badge/Socket.IO-4.7-black?style=flat-square&logo=socket.io)
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
- [Database Schema](#database-schema)
- [Usage Guide](#usage-guide)
- [Real-time Features](#real-time-features)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

### User Features
- **User Registration & Login**: Secure authentication with JWT
- **Profile Management**: Update user profile and medical information
- **Browse Doctors**: View available doctors with specialization and ratings
- **Book Appointments**: Schedule appointments with preferred doctors
- **Appointment History**: View past and upcoming appointments
- **Appointment Status**: Track appointment status in real-time

### Doctor Features
- **Doctor Registration**: Specialized registration for healthcare professionals
- **Schedule Management**: Set availability and working hours
- **Appointment Dashboard**: View all scheduled appointments
- **Patient Information**: Access patient details and medical history
- **Appointment Updates**: Real-time notifications for new bookings

### Admin Features
- **Doctor Verification**: Approve or reject doctor registrations
- **Analytics Dashboard**: View charts and statistics
- **User Management**: Manage user accounts
- **System Statistics**: Monitor platform usage

## 🛠️ Tech Stack

### Frontend
- **React** 18.2 - UI library
- **Vite** - Next-generation build tool
- **TypeScript** - Type safety
- **Material-UI (MUI)** - Component library
- **React Router** - Client-side routing
- **Zustand** - State management
- **Socket.IO Client** - Real-time communication
- **Axios** - HTTP client
- **Chart.js & React Chart.js 2** - Data visualization
- **React Hot Toast** - Notifications
- **Tailwind CSS** - Utility styling

### Backend
- **Node.js** - Runtime environment
- **Express** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - ODM library
- **Socket.IO** - Real-time bidirectional communication
- **JWT** - Authentication
- **Bcryptjs** - Password hashing
- **Multer** - File upload handling
- **Cloudinary** - Image hosting and optimization
- **CORS** - Cross-origin requests

## 📁 Project Structure

```
Doctor Appointment System/
├── backend/
│   ├── index.js                 # Server entry point
│   ├── package.json
│   ├── controllers/
│   │   ├── authController.js    # Authentication logic
│   │   └── (other controllers)
│   ├── models/
│   │   ├── User.js              # User schema
│   │   ├── Appointment.js       # Appointment schema
│   │   └── Doctor.js
│   ├── routes/
│   │   ├── auth.js              # Auth endpoints
│   │   ├── appointments.js      # Appointment endpoints
│   │   └── doctors.js           # Doctor endpoints
│   ├── middleware/
│   │   └── auth.js              # Auth middleware
│   └── utils/
│       └── cloudinary.js        # Image upload utility
│
├── frontend/
│   ├── src/
│   │   ├── main.jsx             # Entry point
│   │   ├── App.jsx              # Main component
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── ProtectedRoute.jsx
│   │   │   └── ImageUpload.jsx
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── DoctorRegister.jsx
│   │   │   ├── DoctorDashboard.jsx
│   │   │   ├── UserDashboard.jsx
│   │   │   ├── About.jsx
│   │   │   ├── Contact.jsx
│   │   │   └── Settings.jsx
│   │   └── store/
│   │       └── authStore.js     # Zustand state management
│   ├── package.json
│   ├── vite.config.ts
│   ├── tsconfig.json
│   └── tailwind.config.js
```

## 📦 Prerequisites

- **Node.js** v14+ or higher
- **npm** or **yarn** package manager
- **MongoDB** database (local or MongoDB Atlas)
- **Cloudinary Account** (for image hosting)

## 🚀 Installation

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd Doctor\ Appointment\ System
```

### Step 2: Install Dependencies

**Backend:**
```bash
cd backend
npm install
```

**Frontend:**
```bash
cd ../frontend
npm install
```

### Step 3: Set Up Environment Variables

**Backend `.env` file** (in `backend/` directory):
```env
# Server Configuration
PORT=5000
NODE_ENV=development

# Database Configuration
MONGODB_URI=mongodb://localhost:27017/doctor-appointments
# Or MongoDB Atlas:
# MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/appointments?retryWrites=true&w=majority

# JWT Configuration
JWT_SECRET=your_secret_key_here_make_it_very_secure
JWT_EXPIRE=7d

# Cloudinary Configuration (for image uploads)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Socket.IO Frontend URL
SOCKET_URL=http://localhost:5173
```

**Frontend `.env` file** (in `frontend/` directory):
```env
VITE_API_URL=http://localhost:5000
VITE_SOCKET_URL=http://localhost:5000
```

## ⚙️ Configuration

### Cloudinary Setup
1. Sign up at [Cloudinary](https://cloudinary.com/)
2. Get your Cloud Name, API Key, and API Secret
3. Add them to your backend `.env` file

### MongoDB Atlas Setup
1. Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create a cluster and database
3. Get your connection string
4. Add to `.env` file

## ▶️ Running the Application

### Option 1: Run Both Services Concurrently
```bash
# From the project root or backend directory
npm start
```

### Option 2: Run Separately

**Terminal 1 - Start Backend:**
```bash
cd backend
npm start
```

**Terminal 2 - Start Frontend:**
```bash
cd frontend
npm run dev
```

### Build for Production
```bash
# Frontend
cd frontend
npm run build

# Backend is ready to deploy as-is
```

## 📡 API Endpoints

### Authentication Routes (`/api/auth`)
- `POST /register` - Register new user
- `POST /login` - User login
- `POST /doctor-register` - Doctor registration
- `GET /profile` - Get user profile
- `PUT /profile` - Update user profile

### Appointment Routes (`/api/appointments`)
- `GET /` - Get all appointments
- `GET /user` - Get user appointments
- `POST /` - Create new appointment
- `PUT /:id` - Update appointment
- `DELETE /:id` - Cancel appointment
- `PATCH /:id/complete` - Mark appointment as completed

### Doctor Routes (`/api/doctors`)
- `GET /` - Get all doctors
- `GET /:id` - Get specific doctor
- `GET /:id/schedule` - Get doctor schedule
- `PUT /:id/availability` - Update availability

## 💾 Database Schema

### User Model
```javascript
{
  name: String,
  email: String (unique),
  password: String (hashed),
  phone: String,
  role: String (patient/doctor/admin),
  profilePicture: String,
  createdAt: Date
}
```

### Appointment Model
```javascript
{
  patient: ObjectId (ref: User),
  doctor: ObjectId (ref: User),
  date: Date,
  time: String,
  status: String (pending/confirmed/completed/cancelled),
  notes: String,
  createdAt: Date
}
```

## 💡 Usage Guide

### For Patients
1. **Sign Up**: Click "Register" and fill in your details
2. **Browse Doctors**: View available doctors on the platform
3. **Book Appointment**: Select a doctor and choose available time slot
4. **Manage Bookings**: View, reschedule, or cancel appointments
5. **View History**: Check past appointment records

### For Doctors
1. **Register**: Complete doctor registration with credentials
2. **Set Schedule**: Define working hours and availability
3. **Manage Appointments**: View incoming appointment requests
4. **Update Status**: Mark appointments as completed or cancelled
5. **Dashboard**: View statistics and upcoming appointments

## 🔄 Real-time Features

The application uses **Socket.IO** for real-time updates:

- **Appointment Notifications**: Get instant notifications when appointments are booked
- **Status Updates**: Real-time appointment status changes
- **Live Dashboard**: Dashboards update instantly with new data
- **Automatic Refresh**: No need to manually refresh pages

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
