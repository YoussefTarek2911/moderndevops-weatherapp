# Getting Started App 🚀

This is a simple Node.js application designed to demonstrate Docker-based CI/CD using **GitHub Actions** and **GitHub Container Registry (GHCR)**.

---

## 🛠️ Tech Stack

- **Node.js** (18-alpine)
- **Docker**
- **GitHub Actions**
- **GitHub Container Registry (GHCR)**
- **CI/CD pipeline** with Docker image build & push on every `main` branch update

---

## 📦 Project Structure

```bash
.
├── src/
│   └── index.js         # Entry point for the app
├── Dockerfile           # Docker image definition
├── .github/
│   └── workflows/
│       └── docker.image.yml  # GitHub Actions pipeline
├── package.json
├── yarn.lock
└── README.md
