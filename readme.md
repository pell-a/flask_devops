# 🔐 DevSecOps Flask App with GitHub Actions

This is a minimal **Flask application** built to demonstrate secure CI/CD practices using **GitHub Actions**.  
The goal is not the complexity of the app, but the strength and automation of the pipeline around it.

---

## 🚀 What This Project Shows

- ✅ Flask web app
- ✅ CI/CD pipeline using GitHub Actions (`ci.yml`)
- ✅ Python code linting with **Flake8**
- ✅ Code security scanning with **Bandit**
- ✅ Docker image vulnerability scanning with **Trivy**
- ✅ Dockerized application with **Dockerfile**

---

## ⚙️ CI/CD Pipeline Overview

The `.github/workflows/ci.yml` file automates the following steps on each push:

1. **Set up Python environment**
2. **Install dependencies** (`pip install -r requirements.txt`)
3. **Run Flake8** for linting
4. **Run Bandit** to detect Python security issues
5. **Build Docker image**
6. **Run Trivy** to scan the Docker image for vulnerabilities

This ensures your app is checked for code quality and security every time you push changes.

---

## 🐳 Dockerfile

The Flask app is containerized using a simple `Dockerfile` that exposes port `5000` and binds to `0.0.0.0`.  
Bandit will flag this as a medium-severity issue (`B104`), which is expected behavior in containerized apps.

---

## 🧪 Tests

This version does not include unit tests — the focus here is on pipeline security and automation.

---

## 📁 Project Structure
flask_devops/
├── app/
│   └── main.py
│   └──__init__.py
├── .github/
│   └── workflows/
│       └── ci.yml
├── Dockerfile
├── requirements.txt
└── README.md

---

## 🛠 Tools Used

| Tool         | Purpose                                 |
|--------------|------------------------------------------|
| Git & GitHub | Version control and remote repo          |
| GitHub Actions | CI/CD pipeline automation             |
| Bandit       | Python static code security scanner     |
| Trivy        | Docker image vulnerability scanning     |
| Docker       | Containerize the Flask app              |

---

This project is part of a larger DevSecOps learning journey — focused on embedding security directly into development workflows using automation.