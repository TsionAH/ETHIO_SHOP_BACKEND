# **📦 Ethio Shop Backend – REST API**

A production-ready backend API for the **Ethio Shop** e-commerce platform, supporting **authentication, products, orders, ratings, loyalty tiers, and payments**.

---

## **🚀 Live API (Render Deployment)**

Replace with your actual Render link:

```
https://ethio-shop-backend.onrender.com
```

Use the base URL above when testing in **Postman**, **Insomnia**, or integrating with a frontend.

---

## **📌 Table of Contents**

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Environment Variables](#environment-variables)
- [Installation (Local Setup)](#installation-local-setup)
- [Running with Docker](#running-with-docker)
- [API Endpoints](#api-endpoints)

  - [Users API](#1-users-api)
  - [Products API](#2-products-api)
  - [Orders API](#3-orders-api)
  - [Ratings API](#4-ratings-api)
  - [Loyalty Tiers API](#5-loyalty-tiers-api)
  - [Payments API](#6-payments-api)

- [Testing with Postman](#testing-with-postman)
- [Deployment](#deployment)
- [Author](#author)

---

# **📖 Overview**

Ethio Shop Backend is a fully documented REST API powering an online shopping system.
It handles:

- User authentication
- Product & inventory management
- Order creation & tracking
- Rating and reviews
- Loyalty tier rewards
- Payment processing

The API is production-ready, easy to test, and built with industry best practices.

---

# **⭐ Features**

### 🔐 **Authentication**

- Register
- Login
- JWT-based protection
- Update user info

### 🛒 **Product Management**

- Add products (Admin)
- Update / Delete products
- Filter products
- Manage stock

### 📦 **Order Handling**

- Create order
- View orders
- Admin order management

### ⭐ **Ratings**

- Submit rating
- Fetch product ratings

### 🎁 **Loyalty Tiers**

- Tier listing
- Admin management

### 💳 **Payments**

- Record payments
- Get payment details

---

# **🛠 Tech Stack**

| Component         | Technology                                  |
| ----------------- | ------------------------------------------- |
| Backend Framework | Node.js + Express                           |
| Database          | PostgreSQL                                  |
| ORM / Query       | Native SQL / Knex / Sequelize (your choice) |
| Auth              | JWT                                         |
| Deployment        | Render                                      |
| Dev Tools         | Nodemon, Postman                            |
| Containerization  | Docker                                      |

---

# **📁 Project Structure**

```
ethio-shop-backend/
│── src/
│    ├── controllers/
│    ├── routes/
│    ├── models/
│    ├── middleware/
│    └── app.js
│
│── Dockerfile
│── package.json
│── README.md
│── .env   (not included in GitHub)
```

---

# **🔧 Environment Variables**

Create a `.env` file:

```
PORT=5000
DATABASE_URL=your_postgres_connection_string
JWT_SECRET=your_secret_key
```

---

# **🧩 Installation (Local Setup)**

### **1. Clone the repository**

```
git clone https://github.com/YourUsername/ethio-shop-backend.git
cd ethio-shop-backend
```

### **2. Install dependencies**

```
npm install
```

### **3. Start the server (development)**

```
npm run dev
```

The server will run on:

```
http://localhost:5000
```

---

# **🐳 Running with Docker**

### **1. Build the image**

```
docker build -t ethio-backend .
```

### **2. Run the container**

```
docker run -p 5000:5000 ethio-backend
```

Backend will run at:

```
http://localhost:5000
```

---

# **🔗 API Endpoints**

---

## **1) Users API**

### **Register**

```
POST /products/users/register
```

### **Login**

```
POST /products/users/login
```

### **Get User Profile (Auth required)**

```
GET /products/users/:id
```

### **Update User Profile**

```
PUT /products/users/:id
```

---

## **2) Products API**

### **Get All Products**

```
GET /products/products
```

### **Get Product by ID**

```
GET /products/products/:id
```

### **Create Product (Admin only)**

```
POST /products/products
```

### **Update Product (Admin only)**

```
PUT /products/products/:id
```

### **Delete Product (Admin only)**

```
DELETE /products/products/:id
```

---

## **3) Orders API**

### **Create Order**

```
POST /products/orders
```

### **Get All Orders (Admin)**

```
GET /products/orders
```

### **Get Order by ID**

```
GET /products/orders/:id
```

### **Update Order Status (Admin)**

```
PUT /products/orders/:id
```

### **Cancel Order**

```
DELETE /products/orders/:id
```

---

## **4) Ratings API**

### **Submit Rating**

```
POST /products/ratings
```

### **Get Ratings for Product**

```
GET /products/products/:id/ratings
```

---

## **5) Loyalty Tiers API**

### **List Tiers**

```
GET /products/loyalty-tiers
```

### **Admin: Create Tier**

```
POST /products/loyalty-tiers
```

### **Admin: Update Tier**

```
PUT /products/loyalty-tiers/:id
```

### **Admin: Delete Tier**

```
DELETE /products/loyalty-tiers/:id
```

---

## **6) Payments API**

### **Record Payment**

```
POST /products/payments
```

### **Get Payment Details**

```
GET /products/payments/:id
```

---

# **🧪 Testing with Postman**

### **1. Open Postman**

### **2. Set Base URL:**

```
https://ethio-shop-backend.onrender.com
```

### **3. Start with:**

- Register → `POST /products/users/register`
- Login → `POST /products/users/login`

### **4. Copy JWT Token**

Add to:

```
Authorization → Bearer Token
```

### **5. Test protected endpoints**

---

# **🚀 Deployment (Render)**

This backend is deployed on **Render** using:

- Dockerfile
- Auto-deploy from GitHub
- Environment variables stored in dashboard

Each push triggers an automatic redeploy.

---

# **👩‍💻 Author**

**Tsion Alemu Handiso**
Backend Developer | API Engineer | E-Commerce Systems
GitHub: [https://github.com/TsionAH](https://github.com/TsionAH)

---

# **🎉 Thank You for Using Ethio Shop API**
