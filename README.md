# 🌦️ Weather App — Microservices with Docker Compose

A fully containerized microservices-based weather application built with a modern DevOps mindset. This project demonstrates how to build a modular, scalable, and portable system using **Docker**, **Go**, **Flask**, **MySQL**, and a **JavaScript frontend**.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Environment Variables](#environment-variables)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Troubleshooting](#troubleshooting)
- [Future Improvements](#future-improvements)
- [License](#license)

---

## 🚀 Overview

This application lets users log in and view real-time weather updates using a user-friendly UI. It’s split into three main microservices:

- `auth`: User authentication service written in Go
- `weather`: Flask-based microservice that fetches weather data
- `ui`: Frontend app (React or Vanilla JS)
- `db`: MySQL database

All services are containerized and orchestrated via **Docker Compose**.

---

## 🧱 Architecture

                    ┌───────────────┐
                    │    Browser    │
                    └──────┬────────┘
                           │
                   ┌───────▼────────┐
                   │     UI (3000)  │
                   └──────┬─────────┘
         ┌───────────────┼───────────────┐
         │                               │
  ┌──────▼──────┐                 ┌──────▼──────┐
  │  Auth (8080)│                 │ Weather (5000)│
  └──────┬──────┘                 └──────┬───────┘
         │                               │
         ▼                               ▼
    ┌────────┐                     ┌────────────┐
    │  MySQL │                     │ Weather API│
    └────────┘                     └────────────┘

---

## 🛠️ Tech Stack

| Layer        | Tech                                  |
|--------------|----------------------------------------|
| Frontend     | JavaScript (React or Vanilla JS)       |
| Auth Service | Go, MySQL driver                       |
| Weather API  | Python Flask                           |
| Database     | MySQL 8.0                              |
| Containerization | Docker, Docker Compose            |

---

## 📁 Project Structure


---

## ⚙️ Environment Variables

Create a `.env` file in the root directory:

```env
# Database
DB_HOST=db
DB_USER=root
DB_PASSWORD=my-secret-pw
DB_NAME=authdb

# Auth API
AUTH_HOST=auth
AUTH_PORT=8080

# Weather API
WEATHER_HOST=weather
WEATHER_PORT=5000
APIKEY=your-weather-api-key
# 1. Clone the repo
git clone https://github.com/your-username/modern-devops-weatherapp.git
cd modern-devops-weatherapp

# 2. Create the .env file
notepad .env
# (Paste the environment variables shown above)

# 3. Build and start the app
docker-compose up --build -d

# 4. Open the app
http://localhost:3000


