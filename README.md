
---

## Backend — `README.md`

```md
# 📚 Book Manager – Backend

A RESTful backend API for the Book Manager application built with **Node.js, Express, MongoDB, and Mongoose**.

The backend provides authentication, book CRUD operations, image uploads, and dashboard statistics.

## ✨ Features

### 🔐 Authentication

- User registration
- User login
- JWT authentication
- Protected routes
- Password hashing with bcryptjs

### 📚 Book Management

- Create books
- Get all books
- Get a single book
- Update books
- Delete books
- Book categories
- Book prices
- Published dates
- Book descriptions
- Cover image uploads

### 📊 Dashboard Statistics

The backend provides authenticated dashboard statistics including:

- Total books
- Total collection value
- Books grouped by category
- Books added over time
- Average price by category

Dashboard statistics are calculated server-side using MongoDB aggregation pipelines.

### 🛡️ Security

- Helmet
- CORS
- Express Rate Limit
- JWT authentication
- Password hashing
- Server-side validation

## 🛠️ Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- bcryptjs
- Multer
- Helmet
- CORS
- Express Rate Limit
- dotenv

## 📁 Project Structure

```text
backend/
├── config/
│   └── db.js
├── controllers/
│   ├── authController.js
│   ├── bookController.js
│   └── dashboardController.js
├── middleware/
│   ├── auth.js
│   ├── errorHandler.js
│   └── upload.js
├── models/
│   ├── User.js
│   └── Book.js
├── routes/
│   ├── authRoutes.js
│   ├── bookRoutes.js
│   └── dashboardRoutes.js
├── uploads/
├── server.js
└── package.json
🚀 Installation

Clone the repository:

git clone https://github.com/Abdulkhaliqdev2007/book-manager-week4-backend.git

Go to the project directory:

cd book-manager-week4-backend

Install dependencies:

npm install
⚙️ Environment Variables

Create a .env file in the backend root:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret

Replace the values with your own configuration.

Do not commit the .env file to GitHub.

▶️ Run the Server
Development
npm run dev
Production
npm start

The API normally runs on:

http://localhost:5000
🔗 API Endpoints
Authentication
POST /api/auth/signup
POST /api/auth/login
Books
GET    /api/books
GET    /api/books/:id
POST   /api/books
PUT    /api/books/:id
DELETE /api/books/:id

Creating, updating, and deleting books require authentication.

Dashboard
GET /api/dashboard/stats

The dashboard endpoint requires a valid JWT token.

📊 Dashboard API Response

The dashboard endpoint returns statistics in the following structure:

{
  "success": true,
  "data": {
    "totalBooks": 0,
    "totalValue": 0,
    "booksByCategory": [],
    "booksOverTime": [],
    "averagePriceByCategory": []
  }
}
🖼️ Image Uploads

Book cover images are uploaded using Multer.

Uploaded images are served through:

/uploads
🔐 Authentication

Protected routes require a JWT token:

Authorization: Bearer <token>

The authentication middleware verifies the token and attaches the authenticated user to:

req.user
🛡️ Security

The API uses:

Helmet
CORS
Express Rate Limit
JWT
bcryptjs
Environment variables
Protected API routes
Server-side validation
📌 Project Status

Week 4 – Dashboard with Data Visualization

The backend now provides dashboard statistics through a protected API endpoint using MongoDB aggregation.

👨‍💻 Author

Abdulkhaliqdev2007

GitHub:

https://github.com/Abdulkhaliqdev2007
📄 License

This project is licensed under the MIT License.
