# 💬 Real-Time Chat Application

Welcome to the **Full Stack Realtime Chat App** – a scalable, secure, and containerized chat application built using the modern web stack. Designed for real-time communication, this project also reflects strong DevOps practices with Docker and Kubernetes.

## 📚 Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Backend Configuration](#backend-configuration)
- [Running the Application](#running-the-application)
- [Contributing](#contributing)
- [Future Plans](#future-plans)
- [License](#license)

---

## 📝 Introduction

This project delivers a real-time chat experience with user authentication, secure messaging, and modern UI design. It's built to demonstrate both **full-stack development** and **DevOps orchestration** techniques.

---

## ✨ Features

- 🔴 **Real-time Messaging** with Socket.io  
- 🔐 **User Authentication & Authorization** using JWT  
- 🧩 **Modular & Scalable Architecture**  
- 🎨 **Modern UI with TailwindCSS**  
- 👤 **Profile Uploads** and Online Status  
- 🐳 **Dockerized Setup** ready for deployment  
- ☸️ **Kubernetes Ready** (under progress)

---

## 🛠️ Tech Stack

- **Backend:** Node.js, Express, MongoDB, Socket.io  
- **Frontend:** React, TailwindCSS, Zustand, DaisyUI  
- **Authentication:** JWT  
- **DevOps:** Docker, Kubernetes, Nginx  
- **Version Control:** Git + GitHub

---

## 🚀 Getting Started

### 🔧 Prerequisites

- Node.js (v14 or higher)  
- Docker & Docker Compose  
- Git (for cloning)

### 📝 Environment Configuration

Create a `.env` file in the root directory with the following values:

```env
# MongoDB Connection
MONGODB_URI=mongodb://root:admin@mongo:27017/chatApp?authSource=admin&retryWrites=true&w=majority

# JWT
JWT_SECRET=your_jwt_secret_key

# App Config
PORT=5001
NODE_ENV=production
