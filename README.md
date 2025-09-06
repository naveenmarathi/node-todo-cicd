# node-todo-cicd
📝 Node.js To-Do Application – CI/CD with Jenkins & Docker
This project is a Node.js based To-Do List application designed to showcase CI/CD automation using Jenkins and containerization with Docker.
It demonstrates how to build, test, and deploy a Node.js app inside Docker containers, fully automated via Jenkins pipelines.

🚀 Features
✅ Simple To-Do list web app using Node.js & Express.js
✅ Dockerized for seamless deployments
✅ Jenkins CI/CD pipeline to automate build, test, and deploy
✅ Unit tests with Jest
✅ Easy setup for local development with Docker Compose

🛠️ Tech Stack
Backend: Node.js, Express.js
Containerization: Docker, Docker Compose
CI/CD: Jenkins
Testing: Jest

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
This project includes a Jenkinsfile for pipeline automation:
Build Stage – Install Node.js dependencies & build the app
Test Stage – Run unit tests (test.js)
Docker Build & Push – Build Docker image & push to registry
Deploy Stage – Run container using latest image

📸 Project Architecture
🔹 CI/CD Pipeline Flow
🔹 Dockerized Node.js App
