# 🚀 Ecommerce Microservices

This repository contains a **microservices-based** e-commerce system using **FastAPI** and **Node.js**, following best practices for scalability and maintainability.

## 📌 Project Overview

### **🛠 Tech Stack:**
- **FastAPI (Python)** → Auth & Order services
- **Node.js (Express)** → Product & Notification services
- **PostgreSQL** → Relational database (FastAPI services)
- **MongoDB** → NoSQL database (Node.js services)
- **RabbitMQ/Kafka** → Event-driven communication
- **Redis** → Caching for faster responses
- **NGINX** → API Gateway
- **Docker & Docker Compose** → Containerization & orchestration

## 📂 Folder Structure
```
ecommerce-microservices/
│── backend/                  # All backend services
│   ├── node-services/        # Node.js services
│   │   ├── product-service/  # Product Management
│   │   ├── notification-service/ # Order Notifications
│   ├── fastapi-services/     # FastAPI services
│   │   ├── auth-service/     # Authentication & User Management
│   │   ├── order-service/    # Order Processing
│── infrastructure/           # DevOps & Deployment
│   ├── api-gateway/          # NGINX Reverse Proxy
│   ├── docker/               # Docker setup
│   ├── database/             # Database init scripts
│── tests/                    # Integration tests
│── docker-compose.yml        # Multi-service deployment
│── README.md                 # Project documentation
```

## 🚀 Getting Started

### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/YOUR_GITHUB_USERNAME/ecommerce-microservices.git
cd ecommerce-microservices
```

### **2️⃣ Install Dependencies**
Run the setup script to install dependencies for both FastAPI and Node.js services:
```sh
chmod +x install-dependencies.sh
./install-dependencies.sh  # For Linux/macOS
install-dependencies.bat   # For Windows
```

### **3️⃣ Run the Project with Docker**
```sh
docker-compose up --build
```
This will:
- Start **PostgreSQL & MongoDB**
- Run **FastAPI & Node.js services**
- Set up **API Gateway (NGINX)**

### **4️⃣ Running Services Manually (Without Docker)**
#### **Run FastAPI Auth Service**
```sh
cd backend/fastapi-services/auth-service
source venv/bin/activate  # (Windows: venv\Scripts\activate)
uvicorn app.main:app --host 0.0.0.0 --port 8001 --reload
```
#### **Run Node.js Product Service**
```sh
cd backend/node-services/product-service
npm start
```

## 🛠 API Endpoints
### **Auth Service (FastAPI)**
| Endpoint       | Method | Description |
|--------------|--------|-------------|
| `/register`  | POST   | User Registration |
| `/login`     | POST   | User Login |

### **Product Service (Node.js)**
| Endpoint       | Method | Description |
|--------------|--------|-------------|
| `/products`  | GET    | Get All Products |
| `/products`  | POST   | Create a Product |

## ✅ Task Management
- Issues are tracked in the **[GitHub Project Board](https://github.com/YOUR_GITHUB_USERNAME/ecommerce-microservices/projects)**
- Feature requests & bug reports should be submitted as **GitHub Issues**

## 📜 License
This project is open-source and available under the **MIT License**.

---

🎯 **Next Steps:**
1. **[ ] Add Authentication Middleware (JWT)**
2. **[ ] Implement RabbitMQ for Order Processing**
3. **[ ] Deploy with Kubernetes (K8s)**

💡 **Contributions are welcome!** 🚀
