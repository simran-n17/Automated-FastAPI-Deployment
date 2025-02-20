# 🚀 FastAPI Docker Deployment with GitHub Actions

Welcome to the **FastAPI Docker Deployment** project! This repository demonstrates how to automate the creation and deployment of a Dockerized FastAPI application using **GitHub Actions**. Whether you're a DevOps enthusiast or a developer looking to streamline your CI/CD pipeline, this project is for you!

---

## 🌟 Features

- **FastAPI Server**: A lightweight Python web server that responds with JSON data.
- **Dockerized Application**: Containerized using Docker for easy deployment and scalability.
- **GitHub Actions Workflow**: Automates the build and push process to Docker Hub on every `push` event.
- **Continuous Delivery**: Ensures seamless deployment with automated workflows.

---

## 🛠️ Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://www.docker.com/)
- [Git](https://git-scm.com/)
- A [Docker Hub](https://hub.docker.com/) account
- A [GitHub](https://github.com/) account
- Python (version 3.7+ recommended)

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/devops-assignment.git
cd devops-assignment
```

### 2. Run the FastAPI Server Locally
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Start the server:
   ```bash
   uvicorn main:app --host 0.0.0.0 --port 8000 --reload
   ```
3. Access the server at: [http://localhost:8000](http://localhost:8000)

---

## 🐳 Docker Setup

### 1. Build the Docker Image
```bash
docker build -t your-dockerhub-username/fastapi-app:latest .
```

### 2. Run the Docker Container
```bash
docker run -p 8000:8000 your-dockerhub-username/fastapi-app:latest
```

### 3. Access the FastAPI Server
Open your browser and go to: [http://localhost:8000](http://localhost:8000)

---

## 🤖 GitHub Actions Workflow

This project uses GitHub Actions to automate the build and deployment process. Here's how it works:

1. **Trigger**: The workflow runs on every `push` event to the `main` branch.
2. **Steps**:
   - Check out the repository.
   - Log in to Docker Hub using a secret token.
   - Build the Docker image.
   - Push the image to Docker Hub.

### View the Workflow File
Check out the workflow file: [`.github/workflows/docker-deploy.yml`](.github/workflows/docker-deploy.yml)

---

## 🔐 Docker Hub Token Setup

To push the Docker image to Docker Hub, you need to set up a **Personal Access Token**:

1. Go to [Docker Hub](https://hub.docker.com/) → **Account Settings** → **Security** → **Access Tokens**.
2. Generate a new token and copy it.
3. Add the token as a secret in your GitHub repository:
   - Go to **Settings** → **Secrets and variables** → **Actions**.
   - Add a new secret named `DOCKERHUB_TOKEN` and paste the token value.

---

## 📦 Docker Hub Image

The Docker image for this project is available on Docker Hub. You can pull it using:

```bash
docker pull your-dockerhub-username/fastapi-app:latest
```

**Docker Hub URL**: [https://hub.docker.com/repository/docker/your-dockerhub-username/fastapi-app](https://hub.docker.com/repository/docker/your-dockerhub-username/fastapi-app)

**My Docker Hub URL**: [https://hub.docker.com/repository/docker/simrannegi/fastapi-app](https://hub.docker.com/repository/docker/simrannegi/fastapi-app)
---

## 📂 Project Structure

```
devops-assignment/
├── .github/
│   └── workflows/
│       └── docker-deploy.yml  # GitHub Actions workflow
├── main.py                    # FastAPI server code
├── requirements.txt           # Python dependencies
├── Dockerfile                 # Docker configuration
└── README.md                  # Project documentation
```

---

## 🛠️ Built With

- [FastAPI](https://fastapi.tiangolo.com/) - Python web framework
- [Docker](https://www.docker.com/) - Containerization platform
- [GitHub Actions](https://github.com/features/actions) - CI/CD automation

---

Happy Coding! 🎉
