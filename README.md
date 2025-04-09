# 🌦️ Weather App — Microservices with Docker Compose

A fully containerized microservices-based weather application built with a modern DevOps mindset. This project demonstrates how to build a modular, scalable, and portable system using **Docker**, **Go**, **Flask**, **MySQL**, and a **JavaScript frontend**.

---

## 📌 Table of Contents

- [Overview](#overview)
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

This application allows users to log in and view real-time weather updates using a clean UI. It’s split into modular microservices:

- `auth`: User authentication service (Go)
- `weather`: Weather data fetcher (Flask)
- `ui`: Frontend interface (React or Vanilla JS)
- `db`: MySQL database service

All are containerized using Docker and orchestrated with Docker Compose.

---

## 🛠️ Tech Stack

| Layer        | Tech                                  |
|--------------|----------------------------------------|
| Frontend     | JavaScript (React or Vanilla JS)       |
| Auth Service | Go + MySQL driver                      |
| Weather API  | Python Flask                           |
| Database     | MySQL 8.0                              |
| Containers   | Docker, Docker Compose                 |

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


# 1. Clone the repository
git clone https://github.com/your-username/modern-devops-weatherapp.git
cd modern-devops-weatherapp

# 2. Create the .env file
notepad .env

# 3. Build and run the services
docker-compose up --build -d
