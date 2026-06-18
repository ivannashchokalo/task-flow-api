# 🚀 Task Flow API

Backend API for the Task Flow application — a personal note management system with authentication, avatar uploads, email notifications, and note organization.

## ✨ Features

### 🔐 Authentication & Security

* User registration and login
* Password hashing with bcrypt
* Session-based authentication using access and refresh tokens
* HTTP-only cookies for secure session storage
* Session refresh mechanism
* User logout with session invalidation

### 📧 Password Recovery

* Password reset via email
* Secure reset tokens using JWT
* Reset token expiration (15 minutes)
* Custom email templates with Handlebars
* Email delivery via Brevo (SMTP)

### 👤 User Management

* Get current authenticated user
* Avatar upload
* Image validation
* Cloudinary integration for image storage

### 📝 Notes Management

* Create notes
* Get all notes
* Get note by ID
* Update notes
* Delete notes
* Pagination support
* Search notes by text
* Filter notes by tag
* User-specific note access

### 🛡️ Additional Features

* Request validation
* Centralized error handling
* MongoDB integration
* RESTful API architecture

## 🛠️ Tech Stack

### Backend

* 🟢 Node.js
* ⚡ Express.js

### Database

* 🍃 MongoDB
* 📦 Mongoose

### Authentication

* 🍪 Cookie-based Sessions
* 🔄 Access & Refresh Tokens
* 🔑 JWT (Password Reset)

### File Storage

* ☁️ Cloudinary
* 📁 Multer

### Email Service

* 📨 Nodemailer
* 📧 Brevo SMTP

### Utilities

* 🔒 bcrypt
* 📄 Handlebars
* ✅ Celebrate/Joi
* ⚠️ http-errors

## 📂 Project Structure

```text
src/
├── constants/
├── controllers/
├── db/
├── middleware/
├── models/
├── routes/
├── services/
├── templates/
├── utils/
├── validations/
└── server.js
```

## 📥 Installation

Clone the repository:

```bash
git clone <repository-url>
cd task-flow-api
npm install
```

## ⚙️ Environment Variables

Create a `.env` file by copying the example file:

```bash
cp .env.example .env
```

Then replace the placeholder values with your own credentials:

```env
PORT=3000
NODE_ENV=development
MONGO_URL=your_mongodb_connection_string

FRONTEND_DOMAIN=https://your-frontend-domain.com


SMTP_HOST=smtp-relay.brevo.com
SMTP_PORT=587
SMTP_USER=your_smtp_user
SMTP_PASSWORD=your_smtp_password
SMTP_FROM=your_email

JWT_SECRET=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```


## ▶️ Running the Project

Development mode:

```bash
npm run dev
```

Production mode:

```bash
npm start
```

## 🔗 API Endpoints

### 🔐 Authentication

| Method | Endpoint               |
| ------ | ---------------------- |
| POST   | /auth/register         |
| POST   | /auth/login            |
| POST   | /auth/refresh          |
| POST   | /auth/logout           |
| POST   | /auth/send-reset-email |
| POST   | /auth/reset-password   |

### 👤 Users

| Method | Endpoint       |
| ------ | -------------- |
| GET    | /users/current |
| PATCH  | /users/avatar  |

### 📝 Notes

| Method | Endpoint       |
| ------ | -------------- |
| GET    | /notes         |
| GET    | /notes/:noteId |
| POST   | /notes         |
| PATCH  | /notes/:noteId |
| DELETE | /notes/:noteId |

## ☁️ File Upload

Avatar uploads:

* Supported formats: images only
* Maximum file size: 2 MB
* Storage provider: Cloudinary

## 👩‍💻 Author

**Ivanna Shchokalo**

* 💼 Junior Full-Stack Developer
* ⚛️ React & Next.js Developer
* 🟢 Node.js & Express Developer
