# 🚀 ML Performance Observatory

[![GitHub stars](https://img.shields.io/github/stars/vishakha2121/ml-performance-observatory)](https://github.com/vishakha2121/ml-performance-observatory/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/vishakha2121/ml-performance-observatory)](https://github.com/vishakha2121/ml-performance-observatory/network)
[![GitHub issues](https://img.shields.io/github/issues/vishakha2121/ml-performance-observatory)](https://github.com/vishakha2121/ml-performance-observatory/issues)
[![License](https://img.shields.io/github/license/vishakha2121/ml-performance-observatory)](https://github.com/vishakha2121/ml-performance-observatory/blob/main/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

> **AI Model Performance Monitoring Dashboard** - Real-time metrics, drift detection, fairness analysis, and SHAP explanations.

---

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

**ML Performance Observatory** is a comprehensive monitoring dashboard designed to track, analyze, and optimize machine learning models in production. It provides real-time insights into model performance, data drift, fairness metrics, and business impact.

### Why This Project?
- 🔍 **Monitor** ML models in real-time
- 📊 **Detect** data drift and performance degradation
- ⚖️ **Ensure** fairness and reduce bias
- 🔮 **Explain** predictions with SHAP
- 💼 **Track** business KPIs and ROI

---

## ✨ Features

### 📊 Performance Metrics
- Real-time latency monitoring (P50, P95, P99)
- Throughput tracking (requests/sec)
- Error rate detection
- Resource utilization (CPU/Memory)
- Inference cost calculation

### 🔍 Data Drift Detection
- Statistical drift detection (KS-test, PSI)
- Feature-wise drift analysis
- Automatic drift alerts
- Root cause identification

### ⚖️ Fairness Monitoring
- Demographic parity analysis
- Equal opportunity tracking
- Disparate impact assessment
- Group-wise performance comparison

### 🔮 Model Explainability
- SHAP feature importance
- Individual prediction explanations
- Summary plots and dependence plots
- Interactive visualization

### 💼 Business KPIs
- Revenue impact tracking
- User satisfaction metrics
- Cost savings analysis
- Model ROI calculation

---

## 🛠️ Tech Stack

### Backend
| Technology | Purpose |
|------------|---------|
| **FastAPI** | High-performance API framework |
| **Python 3.9+** | Core programming language |
| **SQLAlchemy** | ORM for database operations |
| **SQLite/PostgreSQL** | Database storage |
| **MLflow** | Model tracking and registry |
| **SHAP** | Model explainability |
| **Alibi-detect** | Drift detection |
| **Fairlearn** | Fairness metrics |
| **Celery** | Background tasks |
| **Redis** | Caching and task queue |

### Frontend
| Technology | Purpose |
|------------|---------|
| **React 18** | UI framework |
| **Tailwind CSS** | Styling |
| **Recharts** | Data visualization |
| **Socket.io** | Real-time updates |
| **Axios** | HTTP client |
| **Framer Motion** | Animations |

### Infrastructure
| Technology | Purpose |
|------------|---------|
| **Docker** | Containerization |
| **Prometheus** | Metrics collection |
| **Grafana** | Visualization |
| **GitHub Actions** | CI/CD |

---

## 📐 Architecture

---

## 🚀 Installation

### Prerequisites
- Python 3.9+
- Node.js 16+
- Git
- Docker (optional)

### Step 1: Clone Repository
```bash
git clone https://github.com/vishakha2121/ml-performance-observatory.git
cd ml-performance-observatory
# Navigate to backend
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows
venv\Scripts\activate
# Mac/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Setup environment variables
cp .env.example .env

# Initialize database
python scripts/init_db.py

# Load sample data
python scripts/load_sample_data.py

# Train sample model
python scripts/train_sample_model.py

# Start backend server
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# Open new terminal
cd frontend

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env

# Start frontend
npm run dev