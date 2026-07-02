# Flask CI/CD Pipeline using Jenkins and GitHub Actions

## Project Overview

This project demonstrates Continuous Integration and Continuous Deployment (CI/CD) for a simple Flask application using:

- Jenkins Pipeline
- GitHub Actions
- Pytest for unit testing
- GitHub Repository
- AWS EC2 (Ubuntu 24.04)

---

## Technologies Used

- Python 3.12
- Flask
- Pytest
- Jenkins
- GitHub Actions
- Git
- Ubuntu 24.04
- AWS EC2

---

## Jenkins CI/CD Pipeline

The Jenkins pipeline consists of the following stages:

1. Build
   - Creates a Python virtual environment
   - Installs dependencies using pip

2. Test
   - Executes unit tests using pytest

3. Deploy
   - Starts the Flask application after successful tests

The pipeline is automatically triggered whenever changes are pushed to the **main** branch.

Email notifications are configured using Gmail SMTP.

---

## GitHub Actions Workflow

The GitHub Actions workflow performs:

- Checkout Repository
- Setup Python
- Install Dependencies
- Run Tests
- Build Application
- Deploy to Staging (staging branch)
- Deploy to Production (Git tag)

Repository Secrets used:

- DEPLOY_KEY

---

## Repository Structure

```
.
├── .github/
│   └── workflows/
│       └── ci-cd.yml
├── Jenkinsfile
├── app.py
├── requirements.txt
├── test_app.py
└── README.md
```

---

## How to Run Locally

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
pytest -v
python3 app.py
```

---

## Jenkins Pipeline Stages

- Build
- Test
- Deploy

---

## GitHub Actions Jobs

- Test & Build
- Deploy to Staging
- Deploy to Production

---

## Screenshots

The repository includes screenshots demonstrating:

- Jenkins Pipeline Execution
- Jenkins Email Notification
- GitHub Actions Workflow
- Staging Deployment
- Production Deployment

---

## Author

Kaushik
