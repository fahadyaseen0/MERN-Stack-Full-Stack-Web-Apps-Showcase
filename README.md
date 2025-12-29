# 🚀 MERN Stack Portfolio

A comprehensive collection of production-ready **MERN** (MongoDB, Express, React, Node.js) stack applications. This repository showcases three distinct full-featured projects demonstrating modern web development practices, best practices, and advanced features.

![MERN](https://img.shields.io/badge/MERN-Stack-61DAFB?style=flat-square&logo=mongodb)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)

## 📚 Projects Overview

### 1. ☁️ [CloudNotes](#cloudnotes)
A secure, full-stack note-taking application with user authentication and real-time synchronization.
<!-- Image of CloudNotes -->
![CloudNotes](./CloudNotes/src/public/MERN%201-Cover.jpg)
**Tech:** React, Express, MongoDB, JWT, Tailwind CSS, Framer Motion

**Key Features:** User auth, CRUD operations, Protected routes, Responsive UI

**Status:** ✅ Production Ready

---

### 2. 🏥 [Doctor Appointment System](#doctor-appointment-system)
A comprehensive healthcare management platform for booking and managing doctor appointments with real-time updates.

![Doctor Appointment System](./Doctor%20Appointment%20System/frontend/src/public/app.JPG)

**Tech:** React, TypeScript, Express, MongoDB, Socket.IO, Material-UI, Zustand

**Key Features:** Real-time notifications, Multi-role system (Patient/Doctor/Admin), Image uploads, Analytics dashboard

**Status:** ✅ Production Ready

---

### 3. 💬 [MERN Chat App](#mern-chat-app)
A full-featured real-time messaging application with one-on-one and group chat capabilities.

![Chatt App](./MERN%20Chat%20App/FrontEnd/src/public/chatapp.jfif)
**Tech:** React, Express, MongoDB, Socket.IO, Tailwind CSS, Emoji support

**Key Features:** Real-time messaging, User search, Group chats, Typing indicators, Image sharing

**Status:** ✅ Production Ready

---

## 🎯 Quick Navigation

| Project | Directory | Frontend | Backend | Database |
|---------|-----------|----------|---------|----------|
| CloudNotes | `/CloudNotes` | React + Vite | Express.js | MongoDB |
| Doctor Appointment | `/Doctor Appointment System` | React + TypeScript | Express.js | MongoDB |
---

## 🛠️ Tech Stack Summary

### Frontend Technologies
| Technology | Purpose | Version |
|-----------|---------|---------|
| React | UI Library | 18.2+ |
| Vite | Build Tool | Latest |
| Tailwind CSS | Styling | 3.x |
| React Router | Routing | 6.x |
| Axios | HTTP Client | 1.x |
| Socket.IO Client | Real-time Updates | 4.7+ |
| TypeScript | Type Safety | 5.x |
| Material-UI | Component Library | 6.x |

### Backend Technologies
| Technology | Purpose | Version |
|-----------|---------|---------|
| Express.js | Web Framework | 4.18+ |
| Node.js | Runtime | 14+ |
| MongoDB | Database | 5.0+ |
| Mongoose | ODM | 8.x |
| Socket.IO | Real-time | 4.7+ |
| JWT | Authentication | jsonwebtoken 9.x |
| Bcryptjs | Password Hashing | 2.4+ |
| Multer | File Upload | 1.4+ |
| Cloudinary | Image Hosting | 1.41+ |

---

## 🔧 General Setup Instructions

### Prerequisites
- **Node.js** v14 or higher
- **npm** or **yarn** package manager
- **MongoDB** (local or cloud-based via MongoDB Atlas)
- **Cloudinary Account** (for image-based projects)

### Environment Variables

Each project requires environment configuration. Here's a template:

**Backend `.env` Template:**
```env
# Server
PORT=5000
NODE_ENV=development

# Database
MONGODB_URI=mongodb://localhost:27017/database-name
# Or MongoDB Atlas:
# MONGODB_URI=mongodb+srv://user:password@cluster.mongodb.net/db?retryWrites=true&w=majority

# Authentication
JWT_SECRET=your_very_secret_key_here_make_it_long
JWT_EXPIRE=7d

# Cloudinary (if applicable)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Socket.IO (if applicable)
SOCKET_CLIENT_URL=http://localhost:5173
```

**Frontend `.env` Template:**
```env
VITE_API_URL=http://localhost:5000
VITE_SOCKET_URL=http://localhost:5000
```

---

## 📦 Installation & Setup

### Option 1: Setup Individual Projects

Each project can be set up independently:

```bash
# Navigate to project directory
cd CloudNotes  # or "Doctor Appointment System" or "MERN Chat App"

# Install dependencies
npm install

# Configure .env file with required variables

# Run the project
npm run dev  # or npm start / npm run dev:all depending on project
```

### Option 2: Setup All Projects

```bash
# Install dependencies for all projects
for dir in CloudNotes "Doctor Appointment System" "MERN Chat App"; do
  cd "$dir"
  npm install
  cd ..
done
```

---

## 🚀 Running Applications

### Development Mode

Each project has specific startup commands. Refer to individual README files for exact commands.

**General Pattern:**
- Backend: `npm start` or `npm run dev`
- Frontend: `npm run dev`

### Production Build

```bash
# Build frontend
npm run build

# Backend is production-ready as-is (Node.js)
```

---

## 📱 Application Features Comparison

| Feature | CloudNotes | Doctor App | Chat App |
|---------|-----------|-----------|----------|
| User Authentication | ✅ | ✅ | ✅ |
| Real-time Updates | ⚡ | ✅ Socket.IO | ✅ Socket.IO |
| Image Upload | ❌ | ✅ Cloudinary | ✅ Cloudinary |
| Multi-role System | ❌ | ✅ | ⚡ Basic |
| Search Functionality | ❌ | ✅ | ✅ |
| Notifications | ✅ Toast | ✅ Real-time | ✅ Real-time |
| Mobile Responsive | ✅ | ✅ | ✅ |
| TypeScript | ❌ | ✅ | ❌ |
| Material-UI | ❌ | ✅ | ❌ |
| Analytics | ❌ | ✅ | ❌ |
| Group Conversations | ❌ | ❌ | ✅ |

---

## 🏗️ Directory Structure

```
MERN-Stack/
├── README.md                          # This file
├── CloudNotes/
│   ├── README.md
│   ├── server/                        # Backend
│   ├── src/                           # Frontend
│   └── package.json
├── Doctor Appointment System/
│   ├── README.md
│   ├── backend/
│   ├── frontend/
│   └── package.json
├── MERN Chat App/
│   ├── README.md
│   ├── BackEnd/
│   ├── FrontEnd/
│   └── package.json
```

---

## 🔐 Security Best Practices Implemented

- ✅ JWT token-based authentication
- ✅ Password hashing with bcryptjs
- ✅ Protected API routes with middleware
- ✅ CORS configuration for security
- ✅ Environment variables for sensitive data
- ✅ HTTP-only cookies (where applicable)
- ✅ Input validation and sanitization
- ✅ Error handling with detailed logging

---

## 🎓 Learning Outcomes

This portfolio demonstrates:

1. **Full-Stack Development**: End-to-end application development
2. **Real-time Communication**: Socket.IO implementation
3. **Authentication**: JWT and secure session management
4. **Database Design**: MongoDB schemas and relationships
5. **Frontend Architecture**: React components and state management
6. **API Design**: RESTful endpoints and error handling
7. **Deployment Ready**: Production-level code quality
8. **Modern Tooling**: Vite, TypeScript, Tailwind CSS

---

## 📖 Documentation

Each project includes comprehensive README with:
- Feature description
- Tech stack details
- Installation instructions
- Configuration guide
- API endpoint documentation
- Usage examples
- Troubleshooting tips

---

## 🚀 Deployment Guide

### Backend Deployment Options
- **Heroku**: Free tier available
- **Railway**: Modern alternative to Heroku
- **Render**: Free tier with MongoDB support
- **DigitalOcean**: Affordable VPS options
- **AWS**: Scalable solutions

### Frontend Deployment Options
- **Vercel**: Optimized for React apps
- **Netlify**: Git-connected deployment
- **GitHub Pages**: Free static hosting
- **Surge**: Simple CLI deployment

### Database Deployment
- **MongoDB Atlas**: Cloud-hosted MongoDB (recommended)
- **Self-hosted**: With DigitalOcean or AWS

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📝 License

All projects in this repository are licensed under the **MIT License**. See individual project directories for license files.

---

## 📞 Support & Issues

For issues and questions:
1. Check individual project README files first
2. Review existing issues on GitHub
3. Create a detailed issue with:
   - Project name
   - Steps to reproduce
   - Expected vs actual behavior
   - Environment details

---

## 🌟 Project Status

| Project | Status | Last Updated | Maintenance |
|---------|--------|--------------|-------------|
| CloudNotes | ✅ Active | 2025-12-22 | Maintained |
| Doctor Appointment | ✅ Active | 2025-12-22 | Maintained |
| Chat App | ✅ Active | 2025-12-22 | Maintained |

---

## 💡 Tips for Getting Started

1. **Start with CloudNotes** - Simplest project, great for learning fundamentals
2. **Move to Doctor App** - Learn multi-role systems and real-time updates
3. **Explore Chat App** - Master Socket.IO and complex state management
4. **Compare Implementations** - See different approaches to same problems

---

## 🎯 Next Steps

- [ ] Deploy projects to production
- [ ] Add unit tests using Jest
- [ ] Implement CI/CD with GitHub Actions
- [ ] Add E2E tests with Cypress
- [ ] Improve performance with caching
- [ ] Add dark mode theme
- [ ] Implement WebRTC for video calls (Chat App)
- [ ] Add payment integration (Doctor App)

---

## 📞 Quick Links

- [CloudNotes Documentation](./CloudNotes/README.md)
- [Doctor Appointment System Documentation](./Doctor%20Appointment%20System/README.md)
- [MERN Chat App Documentation](./MERN%20Chat%20App/README.md)

---

<div align="center">

**Made with ❤️ using MERN Stack**

*Happy Coding! 🚀*

</div>
- Real-time one-on-one and group messaging
- Socket.IO for instant message delivery
- User search and discovery
- Online status indicators
- Typing indicators
- Emoji picker integration
- Image sharing with Cloudinary
- Responsive mobile-friendly UI

### 🚀 Quick Start
```bash
cd MERN\ Chat\ App
# Install backend
cd BackEnd && npm install
# Install frontend
cd ../FrontEnd && npm install
# Configure .env files with MongoDB and Cloudinary credentials
# Terminal 1: Start backend
npm start
# Terminal 2: Start frontend
npm run dev
```

### 📖 [Full Documentation](./MERN%20Chat%20App/README.md)
4. **Set up environment variables:**
   Create a .env file in the root directory with the following variables:
    ```bash
    JWT_SECRET=your_jwt_secret_key
    MONGO_URI=mongodb://localhost:27017/your_database_name
5. **Run the application:**
   To run both the frontend and backend concurrently, execute the following command:
   ```bash
   npm run dev:all
  The frontend will be available at http://localhost:3000 and the backend at http://localhost:5000.


### Folder Structure
  The folder structure is organized as follows:
   ```graphql
   mern-stack-projects/
  ├── project-name/               # Folder for the project
  │   ├── client/                 # React frontend forproject
  │   ├── server/                 # Express API for project
  │   └── .env                    # Environment variables for project
  ├── other-project-1/            # Other MERN stack project
  ├── other-project-2/            # Other MERN stack project
  ├── .gitignore                  # Git ignore file
  ├── README.md                   # This file
  └── package.json                # Root dependencies and scripts
  ```
### Contribution
Contributions are welcome! If you would like to contribute to this repository, please follow these steps:

1. Fork the repository.
2. Create a new branch .
   ```bash
   git checkout -b feature/your-feature
3. Make your changes and commit them.
   ```bash
   git commit -am 'Add new feature
4. Push your changes.
   ```bash
   git push origin feature/your-feature
5. Create a pull request.
    



<p align="center">
  <a href="https://www.linkedin.com/in/alikhan-devs/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  &nbsp;
  <a href="mailto:alikhandevs@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white" alt="Email" />
  </a>
  &nbsp;
  <a href="https://wa.me/923429327224" target="_blank">
    <img src="https://img.shields.io/badge/WhatsApp-25D366?style=flat&logo=whatsapp&logoColor=white" alt="WhatsApp" />
  </a>
</p>

<p align="center">Made with ❤️ by <strong>Ali Khan</strong></p>

