# 🧑‍💼 Job Portal Backend API

A robust and scalable **Job Portal REST API** built with **Node.js**, **Express**, and **MongoDB**. This backend supports **role-based access control** for Employers and Job Seekers, secure **authentication using JWT**, and structured **job application workflows** — designed for real-world job board platforms.

---

## 🚀 Features

- 🔐 **User Authentication** (Register/Login with JWT)
- 👥 **Role-Based Access Control** (Employer, Jobseeker)
- 📄 **File Uploads** (Resume handling)
- 💼 **Job Management**  
  - Create, Read, Delete Jobs (Employer)
  - Browse Jobs (Public)
- 📥 **Job Applications**  
  - Apply to Jobs (Jobseeker)
  - View Applications (Employer)
- 📦 **RESTful API** built with modular architecture
- ✅ Middleware for error handling and access validation

---

## 🧠 Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB (with Mongoose ODM)
- **Authentication:** JWT, bcryptjs
- **File Uploads:** express-fileupload
- **Environment Config:** dotenv

---

## 📁 Folder Structure
```
job-portal-backend/
├── config/
|
│ └── db.js # MongoDB connection setup
|
├── controllers/
|
│ ├── authController.js # Register/Login logic
|
│ └── jobController.js # Job CRUD and application handling
|
├── middlewares/
|
│ ├── auth.js # JWT auth middleware
|
│ ├── role.js # Role-based access
|
│ └── errorHandler.js # Centralized error handling
|
├── models/
|
│ ├── User.js
|
│ ├── Job.js
|
│ └── Application.js
|
├── routes/
|
│ ├── authRoutes.js
|
│ └── jobRoutes.js
|
├── uploads/ # Resumes and user files
|
├── .env # Environment variables
|
├── server.js
|
└── README.md

```
## 📦 API Endpoints

### 🔐 Authentication Routes (`/api/auth`)
- `POST /register` – Register new user
- `POST /login` – Login and receive JWT token

### 💼 Job Routes (`/api/jobs`)
- `POST /` – Create job (Employer only)
- `GET /` – Get all jobs
- `GET /:id` – Get job by ID
- `DELETE /:id` – Delete job (Employer only)

### 📥 Application Routes (To be added)
- `POST /:id/apply` – Apply to a job (Jobseeker)
- `GET /applications` – Employer can view applications for their jobs

---

## 🧪 Running the Project

### 🔧 Setup

```bash
git clone https://github.com/your-username/job-portal-backend.git
cd job-portal-backend
npm install
