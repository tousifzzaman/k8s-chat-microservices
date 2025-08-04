# 💬 Real-Time Chat Application

Welcome to the **Full Stack Realtime Chat App** – a scalable, secure, and containerized chat application built using the modern web stack. Designed for real-time communication, this project also reflects strong **DevOps practices** with Docker and Kubernetes.

---

## 📚 Table of Contents

- [Introduction](#-introduction)  
- [Features](#-features)  
- [Tech Stack](#-tech-stack)  
- [Getting Started](#-getting-started)  
- [Environment Configuration](#-environment-configuration)  
- [Docker Setup](#-docker-setup)  
- [Kubernetes Deployment](#️-kubernetes-deployment-implemented-)  
- [Contributing](#-contributing)  
- [Future Plans](#-future-plans)  
- [License](#-license)

---

## 📝 Introduction

This project delivers a real-time chat experience with user authentication, secure messaging, and modular UI design. More importantly, it demonstrates containerized deployments, orchestration, and infrastructure best practices using DevOps tools.

---

## ✨ Features

- 🔴 **Real-time Messaging** with Socket.io  
- 🔐 **User Authentication & Authorization** using JWT  
- 🧩 **Modular & Scalable Architecture**  
- 🐳 **Dockerized Setup** ready for deployment  
- ☸️ **Kubernetes Deployment** with proper resource management  
- 🔄 **CI/CD Ready** (can integrate with GitHub Actions or Jenkins)  

---

## 🛠️ Tech Stack

- **Backend:** Node.js, Express, MongoDB, Socket.io  
- **DevOps Tools:** Docker, Docker Compose, Kubernetes, Nginx  
- **Version Control:** Git + GitHub  
- **Authentication:** JWT  
- **Infrastructure As Code:** Kubernetes YAML manifests (`k8s/` directory)

---
## 🖼️ Demo Screenshots

### 🧑‍💻 Login Page
![Login Screen](./screenshots/Screenshot 2025-08-02 225756)
### 💬 Chat Dashboard
![Chat Dashboard](./screenshots/Screenshot 2025-08-02 230325)
![Chat Dashboard](./screenshots/Screenshot 2025-08-02 230347)

---


## 🚀 Getting Started

### 🔧 Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)  
- [Docker](https://www.docker.com/) & Docker Compose  
- [Kubernetes](https://kubernetes.io/) (Minikube, kind, or any local cluster)  
- [Git](https://git-scm.com/)  

---

## 📝 Environment Configuration

Create a `.env` file in the backend root directory with the following:

```env
# MongoDB
MONGODB_URI=mongodb://root:admin@mongo:27017/chatApp?authSource=admin&retryWrites=true&w=majority

# JWT Secret
JWT_SECRET=your_jwt_secret_key

# App Config
PORT=5001
NODE_ENV=production
```

---

## 🐳 Docker Setup

### 📦 Build and Run (Locally)

```bash
# Build images
docker-compose build

# Start containers
docker-compose up
```

This will spin up:

- Backend service  
- MongoDB (with credentials)  
- Any additional services as defined in docker-compose.yml  

---

## ☸️ Kubernetes Deployment (Implemented ✅)

This project includes complete Kubernetes manifests under the `k8s/` directory. These enable container orchestration, persistence, and traffic routing.

### 🔧 Kubernetes Resources

- **Deployments**: For backend app  
- **Services**: For app & database exposure  
- **PersistentVolume/Claim**: Data persistence for MongoDB  
- **Ingress Controller**: (Nginx-based) for external access  
- **Secrets & ConfigMaps**: Store sensitive values and configurations  
- **Namespace**: Logical isolation of resources  

### 🚀 Steps to Deploy

```bash
# 1. Apply namespace
kubectl apply -f k8s/namespace.yml

# 2. Deploy remaining components
kubectl apply -f k8s/
```

### ✅ Verify

```bash
kubectl get all -n chatapp
```

You should see pods, services, ingress, and volumes running correctly.

---

## 🤝 Contributing

If you're a DevOps engineer or backend enthusiast, feel free to improve the Dockerfiles, enhance the CI/CD workflow, or optimize Kubernetes manifests!

---

## 🔭 Future Plans

- CI/CD with GitHub Actions  
- Kubernetes Helm Charts  
- MongoDB ReplicaSet setup  
- Monitoring with Prometheus + Grafana  
- Auto-scaling (HPA)  

---


## 📄 License

This project is licensed under the MIT License.

Developed with ❤️ for learning & deployment practice
