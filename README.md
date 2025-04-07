# 🌍 Node.js App: Build & Ship with Docker + GitHub Actions

Welcome! This repository showcases how to effortlessly containerize a Node.js web application and automate its deployment to Docker Hub using GitHub Actions.

---

## 🚦 What This Does

Every time code is pushed to the `main` branch, a powerful automation pipeline kicks in:

✅ Lint and analyze the codebase with SonarQube  
🐳 Build a fresh Docker image from the source  
🏷️ Tag the image with useful metadata (like commit SHA, branch, etc.)  
🚀 Push the image to Docker Hub for global availability

No manual steps. No guesswork. Just clean automation.

---

## 🧰 Stack in Action

| Tool          | Purpose                              |
|---------------|--------------------------------------|
| **Node.js**   | The web application runtime          |
| **Docker**    | Containerization & portability       |
| **GitHub Actions** | Continuous integration & delivery |
| **SonarQube** | Code quality and security scanning   |

---

## 🔐 Required GitHub Secrets

To make the pipeline work securely, these secrets should be configured in your repo:

- `SONAR_TOKEN` → SonarQube authentication token  
- `SONAR_HOST_URL` → URL to your SonarQube server  
- `DOCKER_USERNAME` → Your Docker Hub username  
- `DOCKER_PASSWORD` → Your Docker Hub password or access token

---

## 📦 Using the Docker Image

Once the image is pushed, you can easily pull and run it from anywhere:

```bash
docker pull your-dockerhub-username/node-js:latest
docker run -p 3000:3000 your-dockerhub-username/node-js
