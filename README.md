# 🛒 E-Commerce Product Manager — Spring Boot + React

A full-stack e-commerce web application built with **React** (frontend) and **Spring Boot** (backend) to manage products and handle cart operations via RESTful APIs.

![Java](https://img.shields.io/badge/Java-Spring%20Boot-green?logo=springboot)
![React](https://img.shields.io/badge/Frontend-React.js-blue?logo=react)
![H2](https://img.shields.io/badge/Database-H2-lightgrey)

---

## 📌 Overview

A clean, functional e-commerce product management system that demonstrates full-stack development with proper separation of concerns — React handles the UI, Spring Boot exposes REST APIs, and Axios bridges them together. Supports complete CRUD operations on products and an add-to-cart flow.

---

## ✨ Features

- 📦 **View Products** — Browse the full list of available products
- ➕ **Add Product** — Create new product entries with details
- ✏️ **Edit Product** — Update existing product information
- 🗑️ **Delete Product** — Remove products from the system
- 🛒 **Add to Cart** — Add products to a temporary cart for purchase
- 🔌 **REST API Integration** — Fully connected React + Spring Boot via Axios
- 🌐 **CORS Handling** — Configured for local dev (React: 5173, Spring Boot: 8080)

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| React.js | UI library |
| Vite | Build tool & dev server |
| Axios | HTTP requests to backend REST API |
| CSS | Styling |

### Backend
| Technology | Purpose |
|------------|---------|
| Java + Spring Boot | REST API server |
| Spring Data JPA | ORM & database interaction |
| H2 Database | In-memory database (no setup needed) |
| Spring Web | REST controller & CORS config |

---

## 📁 Project Structure

```
Ecom-project-using-springboot/
│
├── frontend/                          # React App
│   ├── src/
│   │   ├── components/
│   │   │   ├── ProductList.jsx        # Display all products
│   │   │   ├── AddProduct.jsx         # Add new product form
│   │   │   ├── EditProduct.jsx        # Edit product form
│   │   │   └── Cart.jsx              # Cart component
│   │   ├── api/
│   │   │   └── axiosConfig.js        # Axios base URL config
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── index.html
│   ├── vite.config.js
│   └── package.json
│
└── backend/                           # Spring Boot App
    └── src/main/java/com/ecom/
        ├── controller/
        │   └── ProductController.java  # REST endpoints
        ├── model/
        │   └── Product.java           # Product entity
        ├── repository/
        │   └── ProductRepository.java # JPA repository
        ├── service/
        │   └── ProductService.java    # Business logic
        └── EcomApplication.java       # Main entry point
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ and npm
- Java 17+
- Maven

> No database setup needed — H2 runs in-memory automatically.

---

### Backend Setup (Spring Boot)

```bash
# Clone the repository
git clone https://github.com/SMSanthoshkumar/Ecom-project-using-springboot.git
cd Ecom-project-using-springboot/backend

# Run the Spring Boot server
mvn spring-boot:run
```

Backend runs on `http://localhost:8080`

H2 Console available at `http://localhost:8080/h2-console`

---

### Frontend Setup (React)

```bash
cd frontend
npm install
npm run dev
```

Frontend runs on `http://localhost:5173`

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/products` | Fetch all products |
| GET | `/api/products/{id}` | Fetch a single product |
| POST | `/api/products` | Add a new product |
| PUT | `/api/products/{id}` | Update an existing product |
| DELETE | `/api/products/{id}` | Delete a product |

---

## 🔄 How It Works

```
React UI (port 5173)
       ↓  Axios HTTP request
Spring Boot REST API (port 8080)
       ↓  Spring Data JPA
H2 In-Memory Database
       ↓  Response
React UI updates state & re-renders
```

CORS is configured in Spring Boot to allow requests from `http://localhost:5173` during local development.

---

## 🛒 Cart Flow

```
User clicks "Add to Cart" on a product
          ↓
Product added to temporary cart state (React context / useState)
          ↓
Cart page displays selected products
          ↓
User reviews cart before purchase
```

> Cart is session-based (in-memory React state) — data resets on page refresh.

---

## 🔮 Future Enhancements

- [ ] User authentication — login/register with JWT
- [ ] Persistent cart — save cart to database per user
- [ ] Order placement — checkout flow with order summary
- [ ] Product search & filter by category/price
- [ ] Image upload for products
- [ ] Payment gateway integration

---

## 🙋‍♂️ Author

**Santhoshkumar S M**

- GitHub: [@SMSanthoshkumar](https://github.com/SMSanthoshkumar)
- LinkedIn: [smsanthoshkumar07](https://www.linkedin.com/in/smsanthoshkumar07)
- Email: smsanthoshkumar2910@gmail.com

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

> ⭐ If you found this useful, drop a star on the repo!
