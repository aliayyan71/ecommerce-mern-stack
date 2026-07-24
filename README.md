# Ecommerce MERN Stack

A full-stack ecommerce web application built with MongoDB, Express, React, and Node.js (MERN). It includes customer-facing shopping features (browsing, search, filtering, cart, checkout) and an admin dashboard for managing products, categories, and orders.

## Features

**Customer**
- Browse products by category, with search and price/category filters
- Product details page with similar product recommendations
- Shopping cart with add/remove and running total
- User registration, login, and password reset
- Checkout with Braintree payment integration
- Order history

**Admin**
- Dashboard for managing products (create, update, delete)
- Category management
- Order management and status updates
- User management

## Tech Stack

**Frontend:** React, React Router, Context API (auth/cart/search state), Ant Design components, Axios

**Backend:** Node.js, Express, MongoDB with Mongoose, JSON Web Tokens (auth), bcrypt (password hashing), Braintree (payments), SendGrid (email)

**Tooling:** Nodemon, Concurrently (run client + server together), dotenv

## Project Structure

```
.
├── client/                # React frontend
│   └── src/
│       ├── components/    # Reusable UI, layout, routes, forms
│       ├── context/       # Auth, cart, and search context providers
│       ├── hooks/         # Custom hooks (e.g. useCategory)
│       ├── pages/         # Route-level pages (Home, Cart, Auth, Admin, User)
│       └── styles/        # Page-specific CSS
├── config/                # Database connection
├── controllers/           # Express route handlers (auth, product, category)
├── helpers/                # Auth helper (password hashing)
├── middlewares/           # JWT auth middleware
├── models/                # Mongoose schemas (User, Product, Category, Order)
├── routes/                # Express route definitions
└── server.js              # Express app entry point
```

## Getting Started

### Prerequisites
- Node.js (v16+)
- A MongoDB database (local or [MongoDB Atlas](https://www.mongodb.com/atlas))
- A [Braintree](https://www.braintreepayments.com/) sandbox account (for payments)
- A [SendGrid](https://sendgrid.com/) API key (for transactional email, if used)

### Installation

1. Clone the repo
   ```bash
   git clone https://github.com/<your-username>/ecommerce-mern-stack.git
   cd ecommerce-mern-stack
   ```

2. Install server dependencies
   ```bash
   npm install
   ```

3. Install client dependencies
   ```bash
   cd client
   npm install
   cd ..
   ```

4. Create a `.env` file in the project root:
   ```env
   PORT=8080
   DEV_MODE=development
   MONGO_URL=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   BRAINTREE_MERCHANT_ID=your_braintree_merchant_id
   BRAINTREE_PUBLIC_KEY=your_braintree_public_key
   BRAINTREE_PRIVATE_KEY=your_braintree_private_key
   ```

5. Run the app (starts both server and client concurrently)
   ```bash
   npm run dev
   ```

   Or run them separately:
   ```bash
   npm run server   # backend on http://localhost:8080
   npm run client   # frontend on http://localhost:3000
   ```

## API Overview

| Route | Description |
|---|---|
| `/api/v1/auth` | Register, login, forgot password, user/admin auth |
| `/api/v1/category` | Create, read, update, delete product categories |
| `/api/v1/product` | Create, read, update, delete products; search and filter |

## What I'd Improve Next

- Add automated tests (Jest/React Testing Library, Supertest)
- Add image upload to cloud storage instead of local storage
- Improve accessibility (ARIA labels, keyboard navigation)
- Add pagination on the admin dashboard tables

## License

MIT
