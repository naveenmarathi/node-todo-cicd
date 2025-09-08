
# 🚀 To-Do Application Deployment-CI/CD with Jenkins & Docker 

## 📄 Project Description

This project is a Node.js based To-Do List application designed to showcase CI/CD automation using Jenkins and containerization with Docker.
It demonstrates how to build, test, and deploy a Node.js app inside Docker containers, fully automated via Jenkins pipelines.

- Developers push code to GitHub.
- Jenkins Master on EC2 triggers the pipeline and delegates tasks to Jenkins Agent.
- Docker image is built, tested, and pushed to Docker Hub.
- The latest Docker image is deployed using Docker Compose.

🚀 Features

✅ Simple To-Do list web app using Node.js & Express.js

✅ Dockerized for seamless deployments

✅ Jenkins CI/CD pipeline to automate build, test, and deploy

✅ Easy setup for local development with Docker Compose

## 🛠️ Tools & Technologies

- **Jenkins** – CI/CD automation server (master/agent setup)

- **Docker** – Containerization of the application

-  **Docker Hub** – Container registry for image storage
 
- **GitHub** – Source code repository

- **EC2 (AWS)** – Hosting Jenkins master and agent nodes
  
📂 Repository Structure
node-todo-cicd/
│── app.js               # Main application file  
│── views/               # Frontend UI  
│── test.js              # Test cases  
│── Dockerfile           # Docker build instructions  
│── docker-compose.yaml  # Compose file for local setup  
│── Jenkinsfile          # Jenkins pipeline script  
│── README.md            # Documentation  

⚡ Local Setup

# Install dependencies

npm install

# Run the app

node app.js


Access at: http://localhost:3000

🐳 Run with Docker

# Build Docker image

docker build -t node-todo-app .

# Run container

docker run -p 3000:3000 node-todo-app


Or use Docker Compose:

docker-compose up --build

🔄 Jenkins CI/CD

- This project includes a Jenkinsfile for pipeline automation.

- Build Stage - Install Node.js dependencies & build the app.

- Test stage - Run unit tests (test.js).

- Docker Build & Push – Build Docker image & push to registry.

- Deploy Stage – Run container using latest image.

📸 Project Architecture

🔹 CI/CD Pipeline Flow

🔹 Dockerized Node.js App

✅ Conclusion

This project demonstrates how a simple Node.js To-Do application can be enhanced with modern DevOps practices. By integrating Jenkins CI/CD pipelines and Docker containerization, the app moves seamlessly from code commit → build → test → containerization → deployment with minimal manual effort.

- It highlights the following key skills:

- Building and containerizing applications using Docker.

- Automating software delivery with Jenkins pipelines.

- Ensuring reliability with automated testing.

- Running consistent environments using Docker Compose.

🚀 This project serves as a practical example of CI/CD automation and provides a solid foundation for scaling into more advanced DevOps workflows such as Kubernetes orchestration and cloud deployments.
