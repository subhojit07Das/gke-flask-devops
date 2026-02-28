# gke-flask-devops ���

A Production-Ready Flask Application deployed on Google Kubernetes Engine (GKE) with a GitOps workflow using GitHub.

## About

A simple Flask REST API containerized with Docker, designed for deployment on GKE. Built as a hands-on DevOps project to learn containerization, Kubernetes, and real-world Git branching strategies.

## Project Structure

```
gke-flask-devops/
├── app/
│   ├── app.py              # Flask application
│   └── requirements.txt    # Python dependencies
├── Dockerfile              # Container build instructions
├── .dockerignore           # Files excluded from Docker build
└── .gitignore              # Files excluded from Git
```

## API Endpoints

| Endpoint  | Description                              |
|-----------|------------------------------------------|
| `/`       | Returns greeting message and hostname    |
| `/health` | Health check with service metadata       |

## Branching Strategy

```
main                        → production-ready
  └── develop               → integration branch
        └── feature/*       → active development
```

## Getting Started

### Run Locally

```bash
pip install flask
python app.py
```

Test it:
```bash
curl http://localhost:8080/
curl http://localhost:8080/health
```

### Build Docker Image

```bash
docker build -t gke-flask-devops .
docker run -p 8080:8080 gke-flask-devops
```

## Tech Stack

- **Python / Flask** — REST API
- **Docker** — Containerization
- **GitHub** — Version control with GitOps workflow
- **GKE (Google Kubernetes Engine)** — Deployment target (coming soon)

## Status

- [x] Flask app created
- [x] Dockerized
- [x] Git branching strategy set up
- [x] Pushed to GitHub
- [ ] GKE deployment (in progress)

