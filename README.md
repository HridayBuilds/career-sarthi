<p align="center">
  <img src="https://img.shields.io/badge/Career-Saarthi-blue?style=for-the-badge&logo=graduation-cap" alt="Career Saarthi"/>
</p>

<h1 align="center">🎓 Career Saarthi</h1>

<p align="center">
  <strong>AI-Powered Career Intelligence Platform</strong>
  <br/>
  <em>Your personalized guide to career success in Healthcare, Agriculture & Smart City domains</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-19.2.0-61DAFB?style=flat-square&logo=react"/>
  <img src="https://img.shields.io/badge/Spring_Boot-4.0.1-6DB33F?style=flat-square&logo=spring-boot"/>
  <img src="https://img.shields.io/badge/FastAPI-0.104-009688?style=flat-square&logo=fastapi"/>
  <img src="https://img.shields.io/badge/Python-3.9+-3776AB?style=flat-square&logo=python"/>
  <img src="https://img.shields.io/badge/Java-21-ED8B00?style=flat-square&logo=openjdk"/>
  <img src="https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square&logo=mysql"/>
</p>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [1. Generate ML Models](#1-generate-ml-models-important)
  - [2. Backend Setup](#2-backend-setup)
  - [3. ML Services Setup](#3-ml-services-setup)
  - [4. Frontend Setup](#4-frontend-setup)
- [API Endpoints](#-api-endpoints)
- [Screenshots](#screenshots)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌟 Overview

**Career Saarthi** is a comprehensive AI-powered career intelligence platform designed to help professionals navigate their career paths in emerging technology sectors. The platform combines machine learning models with an intuitive dashboard to provide:

- **Skill Gap Analysis** - Identify missing skills for your target role
- **Personalized Learning Paths** - Get course and project recommendations
- **Career Insights** - AI-generated actionable career advice
- **Progress Tracking** - Monitor your skill development journey

### Target Domains
- 🏥 **Healthcare Technology** - EHR, Medical Imaging, Telemedicine
- 🌾 **Agricultural Sciences** - Precision Agriculture, IoT, Drone Operations
- 🏙️ **Urban/Smart City Planning** - GIS, Smart Grid, Traffic Management

---

## ✨ Features

### 🎯 Core Features

| Feature | Description |
|---------|-------------|
| **Skill Gap Prediction** | ML model predicts your skill gap score (0-100) based on your profile |
| **Time to Readiness** | Estimates months needed to become job-ready |
| **Missing Skill Detection** | Identifies the most critical skill you need to develop |
| **Course Recommendations** | Personalized course suggestions based on target role |
| **Project Recommendations** | Hands-on project suggestions to build practical skills |
| **AI Career Insights** | GPT-powered actionable career advice |

### 🔐 Authentication & Security

- JWT-based authentication
- Google OAuth2 integration
- Email verification
- Password reset via email
- Protected routes

### 📊 Dashboard Features

- Interactive skill radar charts
- Career pathway timeline
- Progress tracking
- Learning resource management

---

## Architecture

```
┌─────────────────────────────────────────────────────────────────────────┐
│                              FRONTEND                                   │
│                        React + Vite + TailwindCSS                       │
│                           (Port: 5173)                                  │
└─────────────────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                              BACKEND                                    │
│                    Spring Boot 4 + Spring Security                      │
│                      JWT + OAuth2 (Port: 8080)                          │
│                                                                         │
│  ┌─────────────┐  ┌──────────────┐  ┌────────────┐  ┌──────────────┐    │
│  │ Auth        │  │ User         │  │ Profile    │  │ Dashboard    │    │
│  │ Controller  │  │ Controller   │  │ Controller │  │ Controller   │    │
│  └─────────────┘  └──────────────┘  └────────────┘  └──────────────┘    │
└─────────────────────────────────────────────────────────────────────────┘
                                    │
                    ┌───────────────┼───────────────┐
                    ▼               ▼               ▼
┌─────────────────────┐ ┌─────────────────────┐ ┌─────────────────────┐
│   ML Model 1        │ │   ML Model 2        │ │   ML Model 3        │
│   Skill Intelligence│ │   Recommendations   │ │   Career Insights   │
│   (Port: 8001)      │ │   (Port: 8002)      │ │   (Port: 8003)      │
│                     │ │                     │ │                     │
│ • Skill Gap Score   │ │ • Course Matching   │ │ • AI-Powered        │
│ • Time to Ready     │ │ • Project Matching  │ │   Insights          │
│ • Missing Skills    │ │ • Role-First Logic  │ │ • GPT Integration   │
└─────────────────────┘ └─────────────────────┘ └─────────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
   ┌──────────┐          ┌──────────────┐         ┌──────────┐
   │ .pkl     │          │ Knowledge    │         │ OpenAI   │
   │ Models   │          │ Base (JSON)  │         │ API      │
   └──────────┘          └──────────────┘         └──────────┘
```

---

## Tech Stack

### Frontend
- **React 19.2** - UI framework
- **Vite 7** - Build tool
- **TailwindCSS 4** - Styling
- **React Router 7** - Navigation
- **Recharts** - Data visualization
- **Framer Motion** - Animations
- **React Hook Form + Zod** - Form validation

### Backend
- **Spring Boot 4.0.1** - Java framework
- **Spring Security** - Authentication
- **Spring Data JPA** - Database ORM
- **MySQL 8** - Database
- **JWT** - Token authentication
- **OAuth2** - Google login

### ML Services
- **FastAPI** - Python API framework
- **Scikit-learn** - ML models
- **LiteLLM** - LLM integration
- **OpenAI GPT** - AI insights

---

## 📁 Project Structure

```
Career-Saarthi/
├── 📂 Frontend/                    # React Frontend
│   ├── src/
│   │   ├── components/            # Reusable UI components
│   │   │   ├── common/            # Shared components
│   │   │   ├── dashboard/         # Dashboard widgets
│   │   │   ├── insights/          # AI insights components
│   │   │   ├── layout/            # Layout components
│   │   │   └── onboarding/        # Onboarding flow
│   │   ├── context/               # React context (Auth)
│   │   ├── pages/                 # Page components
│   │   └── services/              # API services
│   ├── package.json
│   └── vite.config.js
│
├── 📂 Backend/                     # Spring Boot Backend
│   ├── src/main/java/com/hackathon/securestarter/
│   │   ├── config/                # Configuration classes
│   │   ├── controller/            # REST controllers
│   │   ├── dto/                   # Data Transfer Objects
│   │   ├── entity/                # JPA entities
│   │   ├── repository/            # Data repositories
│   │   ├── security/              # JWT & OAuth2 security
│   │   └── service/               # Business logic
│   └── pom.xml
│
├── 📂 ML/                          # Machine Learning Services
│   ├── model1_skill_recommendation/
│   │   └── backend/
│   │       ├── main.py            # FastAPI app (Port 8001)
│   │       ├── models/            # 🔴 PKL files go here
│   │       └── requirements.txt
│   │
│   ├── model2_recommendation_system/
│   │   ├── main.py                # FastAPI app (Port 8002)
│   │   ├── knowledge_base/        # courses.json, projects.json
│   │   └── requirements.txt
│   │
│   └── model3_suggestions/
│       ├── app/main.py            # FastAPI app (Port 8003)
│       └── requirements.txt
│
├── 📓 model1_training.ipynb        # ⚠️ RUN THIS TO GENERATE MODELS
├── 🔧 start_project.sh            # Start all services (Linux/Mac)
├── 🔧 stop_project.sh             # Stop all services
├── 📄 .env.example                # Environment variables template
└── 📄 README.md                   # You are here!
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed:

| Tool | Version | Download |
|------|---------|----------|
| **Node.js** | 18+ | [nodejs.org](https://nodejs.org/) |
| **Java** | 21 | [adoptium.net](https://adoptium.net/) |
| **Python** | 3.9+ | [python.org](https://python.org/) |
| **Maven** | 3.9+ | [maven.apache.org](https://maven.apache.org/) |
| **MySQL** | 8.0+ | [mysql.com](https://mysql.com/) |

---

### 1. Generate ML Models (IMPORTANT)

The ML models (`.pkl` files) are **not included** in this repository due to size constraints. You must generate them first!

#### Step 1: Open the Training Notebook

```bash
# Navigate to the project root
cd Career-Saarthi
```

Open `model1_training.ipynb` in Jupyter Notebook or VS Code.

#### Step 2: Run All Cells

The notebook will:
1. Load synthetic training data
2. Train ensemble ML models (RandomForest + GradientBoosting)
3. Save 6 `.pkl` files to `ML/model1_skill_recommendation/backend/models/`

#### Step 3: Verify Models Were Created

```bash
ls ML/model1_skill_recommendation/backend/models/
```

You should see:
```
feature_order.pkl
label_encoders.pkl
scaler.pkl
skill_classifier.pkl      # ~285 MB
skill_gap_model.pkl       # ~13 MB
time_model.pkl            # ~5 MB
```

> **Note**: The `skill_classifier.pkl` is large (~285 MB). This is expected due to the RandomForest + GradientBoosting ensemble.

---

### 2. Backend Setup

#### Step 1: Create MySQL Database

```sql
CREATE DATABASE Career_Saarthi;
```

#### Step 2: Configure Environment

```bash
cd Backend/src/main/resources

# Copy example config
cp application.properties.example application.properties

# Edit with your values
nano application.properties
```

Update these values:
```properties
# Database
spring.datasource.username=YOUR_DB_USERNAME
spring.datasource.password=YOUR_DB_PASSWORD

# JWT Secret (generate with: openssl rand -base64 64)
jwt.secret=YOUR_JWT_SECRET

# Google OAuth2 (from Google Cloud Console)
spring.security.oauth2.client.registration.google.client-id=YOUR_GOOGLE_CLIENT_ID
spring.security.oauth2.client.registration.google.client-secret=YOUR_GOOGLE_CLIENT_SECRET

# Email (Gmail App Password)
spring.mail.username=YOUR_EMAIL
spring.mail.password=YOUR_APP_PASSWORD
```

#### Step 3: Run Backend

```bash
cd Backend
mvn spring-boot:run
```

✅ Backend running at: `http://localhost:8080`

---

### 3. ML Services Setup

#### Model 1 - Skill Intelligence (Port 8001)

```bash
cd ML/model1_skill_recommendation/backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run service
uvicorn main:app --host 0.0.0.0 --port 8001
```

#### Model 2 - Recommendations (Port 8002)

```bash
cd ML/model2_recommendation_system

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
echo "OPENAI_API_KEY=your_openai_key" > .env

# Run service
uvicorn main:app --host 0.0.0.0 --port 8002
```

#### Model 3 - Career Insights (Port 8003)

```bash
cd ML/model3_suggestions

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
echo "OPENAI_API_KEY=your_openai_key" > .env

# Run service
uvicorn app.main:app --host 0.0.0.0 --port 8003
```

---

### 4. Frontend Setup

```bash
cd Frontend

# Install dependencies
npm install

# Run development server
npm run dev
```

✅ Frontend running at: `http://localhost:5173`

---

## 🔗 Quick Start (All Services)

For Linux/Mac users, use the convenience scripts:

```bash
# Start all services
./start_project.sh

# Stop all services
./stop_project.sh
```

### Service Ports Summary

| Service | Port | URL |
|---------|------|-----|
| Frontend | 5173 | http://localhost:5173 |
| Backend | 8080 | http://localhost:8080 |
| ML Model 1 (Skills) | 8001 | http://localhost:8001 |
| ML Model 2 (Recommendations) | 8002 | http://localhost:8002 |
| ML Model 3 (Insights) | 8003 | http://localhost:8003 |

---

## 📡 API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | Login user |
| GET | `/api/auth/verify-email` | Verify email token |
| POST | `/api/auth/forgot-password` | Request password reset |
| POST | `/api/auth/reset-password` | Reset password |

### User & Profile
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/user/me` | Get current user |
| PUT | `/api/user/profile` | Update profile |
| POST | `/api/onboarding/submit` | Submit onboarding data |

### Dashboard
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/dashboard/overview` | Get dashboard data |
| GET | `/api/dashboard/skills` | Get skill analysis |
| GET | `/api/dashboard/recommendations` | Get recommendations |

### ML Services
| Method | Endpoint | Port | Description |
|--------|----------|------|-------------|
| POST | `/predict` | 8001 | Predict skill gap |
| POST | `/recommendations` | 8002 | Get course/project recommendations |
| POST | `/api/v1/insights` | 8003 | Generate AI insights |

---

## Screenshots

<details>
<summary>Click to expand screenshots</summary>

### Landing Page
> Modern landing page with animated background

### Dashboard Overview
> Quick stats, skill gap score, and time to readiness

### Skill Progression
> Interactive radar chart showing skill levels

### Career Pathway
> Timeline view of recommended learning path

### AI Insights
> GPT-powered personalized career advice

</details>

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 👨‍💻 Authors

- **Vraj Priyadarshi** - [GitHub](https://github.com/Vraj-Priyadarshi)
- **Hriday Mulchandani** - [GitHub](https://github.com/HridayBuilds)
- **Tanish Jha** 
- **Jil Patel** - [GitHub](https://github.com/JilPatel51)

---

## Acknowledgments

- OpenAI for GPT integration
- Spring Boot team for the excellent framework
- FastAPI for the blazing fast Python APIs
- All open-source contributors

---

<p align="center">
  Made with ❤️ for the future of career development
</p>

<p align="center">
  <a href="#-career-saarthi">⬆️ Back to Top</a>
</p>


