# Kanesea

Kanesea is a modern and premium full-stack eCommerce platform designed to deliver a seamless online shopping experience with a strong focus on performance, scalability, and elegant UI/UX.

The platform allows users to browse products, search items, manage carts, place orders, and securely complete payments, while administrators can manage products, inventory, and orders through an intuitive dashboard.

---

## Features

### User Features
- JWT Authentication & Authorization
- User Registration & Login
- User Registration & Login with Google
- Add to Cart functionality
- Wishlist support
- Product Search & Filtering
- Detailed Product Pages
- Secure Checkout System
- Secure Guest Checkout System
- Razorpay Payment Integration
- Sell With Us functionality
- Coupons & Discounts
- Email Notifications
- Product Recommendation System
- Fully Responsive Design
- Order Management
- Order Tracking

### Admin Features
- Admin Dashboard
- Add Products
- Edit Products
- Delete Products
- Inventory Management
- Manage Orders
- Manage seller submissions

---

## Tech Stack

### Frontend
- React.js
- Tailwind CSS
- React Router
- Axios

### Backend
- Node.js
- Express.js
- JWT Authentication
- Multer

### DevOps
- Docker
- Docker Compose
- GitHub Actions
- Docker Hub
- Prometheus
- Grafana
- cAdvisor

### Database
- MongoDB

### Payment Gateway
- Razorpay

---

# DevOps Implementation

This project was enhanced with DevOps practices to improve portability, automation, and observability.

## Containerization
- Dockerized the frontend (React + Nginx).
- Dockerized the backend (Node.js + Express).
- Created separate Docker images for frontend and backend services.

### Docker Images
- `kanesea-frontend`
- `kanesea-backend`

### Docker Hub Repositories
The application images are published to Docker Hub and can be pulled using:

```bash
docker pull sakeenabi/kanesea-frontend
docker pull sakeenabi/kanesea-backend
```

---

## Multi-Container Orchestration

Docker Compose was used to orchestrate multiple services:

- Frontend Container
- Backend Container
- Monitoring Stack

Services can be started using:

```bash
docker compose up -d
```

---

## Continuous Integration (CI)

GitHub Actions was configured to automate the build process.

### CI Pipeline Tasks

- Backend dependency installation.
- Frontend dependency installation.
- Frontend production build verification.
- Docker image build automation.
- Automatic publishing of Docker images to Docker Hub.

The pipeline is triggered automatically on every push to the `main` branch.

---

## Monitoring and Observability

A monitoring stack was integrated to provide visibility into container health and performance.

### Monitoring Components

- **cAdvisor** – Collects Docker container metrics.
- **Prometheus** – Scrapes and stores metrics.
- **Grafana** – Visualizes metrics using dashboards.

Metrics monitored include:

- CPU utilization
- Memory utilization
- Network activity
- Container health and status

---

## Installation

### Clone Repository

```bash
git clone https://github.com/sakeenabi03/kanesea.git
```

Move into project folder:

```bash
cd kanesea
```

---

### Backend Setup

```bash
cd backend

npm install
```

Create a `.env` file:

```env
PORT=8000

MONGODB_URL=your_mongodb_connection_string

JWT_SECRET=your_strong_jwt_secret

BCRYPT_SALT_ROUNDS=10

EMAIL=your_email_address

PASS=your_google_app_password

RAZORPAY_KEY_ID=your_razorpay_key_id

RAZORPAY_KEY_SECRET=your_razorpay_key_secret

SHIPROCKET_EMAIL=your_shiprocket_api_email

SHIPROCKET_PASSWORD=your_shiprocket_api_password
```

> Note:
> To send emails using Gmail, enable 2-Factor Authentication and generate a Google App Password instead of using your actual Gmail password.

Run backend:

```bash
npm run dev
```

---

### Frontend Setup

```bash
cd frontend

npm install

```

Create a `.env` file:

```env

VITE_SERVER_URL=http://localhost:8000

VITE_FIREBASE_APIKEY=your_firebase_api_key

VITE_RAZORPAY_KEY_ID=your_razorpay_key_id
```

Run frontend:

```bash
npm run dev
```

---

## Screenshots

### Homepage
<img src="./screenshots/1.png" width="800"/>

### Products Page
<img src="./screenshots/2.png" width="800"/>

### Product Page
<p align="center">
  <img src="./screenshots/3.png" width="45%">
  <img src="./screenshots/3(1).png" width="45%">
</p>

### Cart Page
<img src="./screenshots/4.png" width="800"/>

### Checkout Page
<img src="./screenshots/5.png" width="800"/>

### Checkout Page
<img src="./screenshots/5.png" width="800"/>

### Sell With Us Page
<p align="center">
  <img src="./screenshots/6.png" width="45%">
  <img src="./screenshots/6(1).png" width="45%">
</p>

### Admin Panel
<img src="./screenshots/7.png" width="800"/>

### Add Category Page
<img src="./screenshots/8.png" width="800"/>

### Add Product Page
<img src="./screenshots/9.png" width="800"/>

### Add Discout Codes Page
<img src="./screenshots/10.png" width="800"/>

### View Seller Forms
<img src="./screenshots/11.png" width="800"/>

---

# DevOps Screenshots

## Docker Hub Images

The following images were successfully built and published to Docker Hub.

### Backend Docker Image

<img src="./screenshots/docker-backend.png" width="800"/>

### Frontend Docker Image

<img src="./screenshots/docker-frontend.png" width="800"/>

---

## cAdvisor Monitoring

cAdvisor was used to monitor Docker container resource consumption.

### Container Resource Overview

<img src="./screenshots/cadvisor-overview.png" width="800"/>

### CPU and Memory Metrics

<img src="./screenshots/cadvisor-metrics.png" width="800"/>

---

## Prometheus Monitoring

Prometheus was configured to scrape metrics exposed by cAdvisor.

### Prometheus Targets

<img src="./screenshots/prometheus-targets.png" width="800"/>

---

## Grafana Dashboards

Grafana dashboards were configured to visualize infrastructure metrics.

### CPU and Memory Dashboard

<img src="./screenshots/grafana-cpu-memory.png" width="800"/>

### Network and Container Dashboard

<img src="./screenshots/grafana-network-containers.png" width="800"/>

---

# DevOps Highlights

- Implemented Docker-based containerization for frontend and backend services.
- Designed multi-container environments using Docker Compose.
- Automated build workflows using GitHub Actions.
- Published container images to Docker Hub.
- Integrated Prometheus and Grafana for monitoring and observability.
- Monitored container-level CPU, memory, and network metrics using cAdvisor.

## Author

**Sakeena Bi**

LinkedIn: https://www.linkedin.com/in/sakeenabi

GitHub: https://github.com/sakeenabi03
