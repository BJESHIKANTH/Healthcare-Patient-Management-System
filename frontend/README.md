<<<<<<< HEAD
# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
=======
# 🏥 Healthcare Patient Management System

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)

A secure, full-stack hospital management web application designed to streamline patient record handling and role-based operations. Built with **Flask** (Python) for the backend and **React.js + Tailwind CSS + TypeScript** for the frontend, it supports multiple roles such as **Admin, Nurse, and Receptionist**, with secure **JWT authentication** and **MongoDB** integration.

---

## 🚀 Features

- 🔐 **JWT-based Authentication & Authorization**
  - Secure login system for Admin, Nurse, and Receptionist roles
  - Role-based access control (RBAC) for protected routes
  - Configurable password hashing with bcrypt
  - Rate limiting for security

- 🏥 **Patient Management (CRUD)**
  - Create, read, update, and delete patient records
  - Input validation and error handling
  - Advanced search with pagination
  - Data compression for better performance

- 🔍 **Search with Pagination**
  - Efficient server-side filtering of patient records with indexed queries
  - Supports pagination for large datasets
  - Real-time search capabilities

- 📊 **Admin Dashboard & Analytics**
  - Admin-only interface to view all registered users
  - Patient demographics and disease distribution analytics
  - Real-time charts and statistics
  - Excludes sensitive info like passwords and MongoDB `_id`

- 🎨 **Frontend**
  - Clean and responsive UI using **React** and **Tailwind CSS**
  - Authentication-aware navigation and route protection
  - Progressive Web App features
  - Optimized performance with React Query

- 🛡️ **Security & Performance**
  - Environment-based configuration
  - Health check endpoints
  - Comprehensive error handling
  - Database connection monitoring
  - Rate limiting and compression

---

## 🛠️ Tech Stack

### **Frontend**
- React.js
- Tailwind CSS
- Axios
- React Router DOM

### **Backend**
- Python (Flask)
- Flask-JWT-Extended
- Flask-CORS
- Flask-PyMongo
- Flask-Limiter (Rate Limiting)
- Flask-Compress (Data Compression)
- Gunicorn (Production Server)

### **Database**
- MongoDB (NoSQL)
- Indexing for optimized search and filtering

---

## 🧰 Installation & Setup

### 📌 Prerequisites
- Python 3.x
- Node.js + npm
- MongoDB running locally or cloud (e.g., MongoDB Atlas)

---

### ⚙️ Backend Setup

```bash
cd Project/healthcare_patient_system
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Flask app will start at: `http://localhost:5000`

**Environment Configuration:**
Copy `env.example` to `.env` and configure your environment variables:
```bash
cp env.example .env
```

---

### 🌐 Frontend Setup

```bash
cd Project/healthcare-frontend
npm install
npm start
```

React app will start at: `http://localhost:3000`

---

## 🧪 API Endpoints (Sample)

| Method | Endpoint                  | Description                      | Protected |
|--------|---------------------------|----------------------------------|-----------|
| POST   | `/api/login`              | Login for all roles              | ❌        |
| POST   | `/api/patients`           | Create patient record            | ✅        |
| GET    | `/api/patients?page=1`    | Get patients with pagination     | ✅        |
| PUT    | `/api/patients/:id`       | Update patient details           | ✅        |
| DELETE | `/api/patients/:id`       | Delete patient                   | ✅        |
| GET    | `/api/admin/users`        | View all users (Admin only)      | ✅        |
| GET    | `/api/health`             | Health check endpoint            | ❌        |
| GET    | `/api/analytics/age`      | Patient age distribution         | ✅        |
| GET    | `/api/analytics/diseases` | Disease distribution             | ✅        |

---

## 👤 Roles & Access

| Role          | Access Privileges                    |
|---------------|--------------------------------------|
| **Admin**     | Full access, manage users & patients |
| **Nurse**     | View & edit patient data             |
| **Receptionist** | Add/view patient entries         |

---

## 🧠 Project Structure

```
📦 project-root
├── backend
│   ├── app.py
│   ├── routes/
│   ├── models/
│   └── utils/
├── frontend
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.js
├── README.md
```

---
---

## 🧩 Future Improvements

- ✅ Email verification & password reset
- ✅ Deploy on Render/Netlify + MongoDB Atlas
- ⏳ Role-based analytics dashboard
- ⏳ Export patient data to PDF/Excel
- ⏳ Add doctor role and appointment module

---

## 🏁 Conclusion

This project demonstrates a full-stack solution for healthcare systems with secure authentication, clean UI, and scalable architecture. Perfect for hospitals, clinics, or medical institutions.

---

