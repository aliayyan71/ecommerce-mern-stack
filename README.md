# 🛒 MERN Ecommerce Platform

A full-stack ecommerce web application built with the **MERN Stack (MongoDB, Express.js, React, and Node.js)**. The platform provides a complete online shopping experience with secure authentication, product browsing, shopping cart functionality, online payments, and a powerful administrative dashboard for managing products, categories, users, and orders.

---

## ✨ Features

### 👤 Customer Features

- ✅ User Registration & Login
- ✅ Secure JWT Authentication
- ✅ Password Reset
- ✅ Browse Products
- ✅ Search Products
- ✅ Filter by Category
- ✅ Filter by Price
- ✅ Product Details Page
- ✅ Similar Product Recommendations
- ✅ Shopping Cart
- ✅ Update Cart Quantity
- ✅ Secure Checkout
- ✅ Braintree Payment Integration
- ✅ Order History
- ✅ Responsive Design

---

### 🛠 Admin Features

- ✅ Admin Dashboard
- ✅ Create Products
- ✅ Edit Products
- ✅ Delete Products
- ✅ Category Management
- ✅ Order Management
- ✅ Update Order Status
- ✅ User Management

---

## 🏗️ Architecture

```text
                 React Frontend
                        │
                        ▼
               Express REST API
                        │
                        ▼
                 MongoDB Database
                  ▲            ▲
                  │            │
          JWT Authentication   │
                               │
                Braintree Payment Gateway
                               │
                        SendGrid Email API
```

---

## 🛠 Tech Stack

### Frontend

- React
- React Router
- Context API
- Axios
- Ant Design
- CSS

### Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- JSON Web Tokens (JWT)
- bcrypt

### Integrations

- Braintree Payments
- SendGrid Email Service

### Development Tools

- Nodemon
- Concurrently
- dotenv
- Git
- GitHub

---

## 📂 Project Structure

```text
.
├── client/
│   └── src/
│       ├── assets/
│       ├── components/
│       ├── context/
│       ├── hooks/
│       ├── pages/
│       ├── styles/
│       ├── App.js
│       └── index.js
│
├── config/
│
├── controllers/
│
├── helpers/
│
├── middlewares/
│
├── models/
│
├── routes/
│
├── server.js
│
├── package.json
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Before running the project, make sure you have installed:

- Node.js (v16 or later)
- npm
- MongoDB (Local or Atlas)
- Git
- Braintree Sandbox Account
- SendGrid API Key

---

### Installation

Clone the repository.

```bash
git clone https://github.com/<your-username>/ecommerce-mern-stack.git
```

Navigate into the project.

```bash
cd ecommerce-mern-stack
```

Install backend dependencies.

```bash
npm install
```

Install frontend dependencies.

```bash
cd client
npm install
cd ..
```

---

## ⚙️ Environment Variables

Create a `.env` file in the project root.

```env
PORT=8080

DEV_MODE=development

MONGO_URL=your_mongodb_connection_string

JWT_SECRET=your_secret_key

BRAINTREE_MERCHANT_ID=your_merchant_id

BRAINTREE_PUBLIC_KEY=your_public_key

BRAINTREE_PRIVATE_KEY=your_private_key

SENDGRID_API_KEY=your_sendgrid_key
```

---

## ▶️ Running the Application

Run both frontend and backend.

```bash
npm run dev
```

Run the backend only.

```bash
npm run server
```

Run the frontend only.

```bash
npm run client
```

Backend:

```
http://localhost:8080
```

Frontend:

```
http://localhost:3000
```

---

## 📡 API Overview

### Authentication

```
POST   /api/v1/auth/register
POST   /api/v1/auth/login
POST   /api/v1/auth/forgot-password
GET    /api/v1/auth/user-auth
GET    /api/v1/auth/admin-auth
```

---

### Categories

```
POST   /api/v1/category/create-category
GET    /api/v1/category/get-category
PUT    /api/v1/category/update-category/:id
DELETE /api/v1/category/delete-category/:id
```

---

### Products

```
POST   /api/v1/product/create-product
GET    /api/v1/product/get-product
GET    /api/v1/product/get-product/:slug
PUT    /api/v1/product/update-product/:id
DELETE /api/v1/product/delete-product/:id
POST   /api/v1/product/product-filters
GET    /api/v1/product/product-search/:keyword
```

---

## 💳 Payment Flow

1. Customer adds items to cart.
2. Checkout page requests a Braintree client token.
3. Payment information is securely processed.
4. Order is stored in MongoDB.
5. User can view the order in Order History.
6. Admin can update order status.

---

## 🎯 Skills Demonstrated

This project demonstrates experience with:

- Full-Stack MERN Development
- REST API Design
- Authentication & Authorization
- JWT Security
- Password Hashing
- MongoDB Database Design
- CRUD Operations
- React Context API
- Payment Gateway Integration
- Email API Integration
- State Management
- Protected Routes
- Role-Based Access Control
- Responsive UI Development

---

## 🚀 Future Improvements

- Product Reviews & Ratings
- Wishlist
- Coupons & Discounts
- Inventory Management
- Product Image Upload to Cloudinary
- Product Pagination
- Admin Analytics Dashboard
- Stripe Payment Support
- Docker Support
- CI/CD with GitHub Actions
- Unit & Integration Testing
- Progressive Web App (PWA)

---

## 📚 What I Learned

Building this project helped me gain practical experience in:

- Developing scalable MERN applications
- Structuring large full-stack projects
- Building secure authentication systems
- Managing application state using React Context
- Designing RESTful APIs
- Integrating third-party services
- Connecting frontend and backend applications
- Handling asynchronous operations
- Deploying production-ready applications

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Ali Ayyan**

Software Engineering & Artificial Intelligence Enthusiast

GitHub: https://github.com/aliayyan71

---

⭐ If you found this project useful, consider giving it a star!
