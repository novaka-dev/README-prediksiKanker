---
📖 This README is also available in [Bahasa Indonesia](./README.id.md)
---

# 🫁 Lung Cancer Detection Web App

A web-based application to help users detect potential lung cancer through a symptom and risk-factor questionnaire. Predictions are generated by a Machine Learning model integrated via API.

---

## 📁 Table of Contents

- [📝 Project Description](#-project-description)
- [🚀 Main Features](#-main-features)
- [🧠 System Architecture](#-system-architecture)
- [🧰 Technologies Used](#-technologies-used)
- [💻 Getting Started](#-getting-started)
  - [📂 Clone Repositories](#-clone-repositories)
  - [🤖 Machine Learning Service](#-machine-learning-service)
  - [🔧 Backend API](#-backend-api)
  - [🌐 Frontend (Next.js)](#-frontend-nextjs)
- [⚙️ Command Scripts](#️-command-scripts)
- [📄 Environment Variables](#-environment-variables)
- [💬 Contact / Team](#-contact--team)
- [🤝 Contribution](#-contribution)
- [📄 License](#-license)

---

## 📝 Project Description

This web app serves as an early lung cancer detection tool. Users fill out a questionnaire, which is then processed and sent through the backend to a ML model that returns prediction results and probabilities.

---

## 🚀 Main Features

- 🔐 User authentication (Login & Register)
- 📋 Symptom & habit questionnaire form
- 🤖 Lung cancer prediction (result + probability)
- 📈 Interactive result visualization

---

## 🧠 System Architecture

```
[Frontend (Next.js)]
       ↓
[Backend API (Express.js)]
       ↓
[ML API (FastAPI / Flask - Python)]
       ↓
[Prediction Model]
```

---

## 🧰 Technologies Used

| Component        | Technology                       |
| ---------------- | -------------------------------- |
| Frontend         | Next.js, Tailwind CSS, Shadcn UI |
| Backend          | Express.js (Node.js)             |
| Machine Learning | FastAPI / Flask, scikit-learn    |
| Database         | MongoDB                          |

---

## 💻 Getting Started

### 📂 Clone Repositories

```bash
git clone https://github.com/RaiStillLearning/projek-analisis-kanker.git
git clone https://github.com/RaiStillLearning/BE_kanker.git
git clone https://github.com/crbsdndr/cancer_detection
```

---

### 🤖 Machine Learning Service

```bash
cd cancer_detection
pip install -r requirements.txt

# Start ML API
uvicorn main:app --reload
```

### 🔧 Backend API

```bash
cd BE_kanker
npm install

# Run server
npm run dev
```

### 🌐 Frontend (Next.js)

```bash
cd projek-analisis-kanker
npm install

# Start Next.js
npm run dev
```

---

## ⚙️ Command Scripts

### Frontend Scripts

```bash
npm run dev       # Run development server
npm run build     # Build for production
npm run lint      # Run linter
```

### Backend Scripts

```bash
npm run dev
npm run start       # Start backend server in development mode
```

---

## 📄 Environment Variables

### Frontend (.env.local)

```env
NEXTAUTH_SECRET=your-secret-key
NEXTAUTH_URL=http://localhost:3000
MONGO_URL=your-mongodb-url
AUTH_GITHUB_ID=your-github-oauth-client-id
AUTH_GITHUB_SECRET=your-github-oauth-client-secret
NEXT_PUBLIC_API_KEY=your-frontend-api-key
```

**How to Get the Values:**

- `NEXTAUTH_SECRET`: Generate a secure string (e.g. using `openssl rand -base64 32`)
- `AUTH_GITHUB_ID` & `AUTH_GITHUB_SECRET`: [Register an OAuth app on GitHub](https://github.com/settings/developers)
- `MONGO_URL`: From your MongoDB provider (e.g., MongoDB Atlas)
- `NEXT_PUBLIC_API_KEY`: This is optional; use it for public API access (if needed)

### Backend (.env)

```env
MONGO_URL=your-mongodb-url
API_KEY=your-backend-api-key
ML_API_URL=https://machine-learning-dendra-production.up.railway.app/
```

**How to Get the Values:**

- `MONGO_URL`: From your MongoDB provider (e.g., MongoDB Atlas)
- `API_KEY`: Secret key used to validate requests between FE & BE (should match with `NEXT_PUBLIC_API_KEY` if needed)
- `ML_API_URL`: The endpoint where your ML model is deployed (e.g. Railway, Vercel, etc.)

---

## 💬 Contact / Team

- [Novaka Saputra](https://github.com/novaka-dev) – Frontend Developer
- [Rakha Arkhana](https://github.com/RaiStillLearning) – Backend
- [Dendra](https://github.com/crbsdndr) – ML Engineer

---

## 🤝 Contribution

We welcome contributions from everyone! Feel free to fork this repo, create a new branch, and submit a pull request.

---

## 📄 License

This project is open-source and licensed under the [MIT License](LICENSE).
