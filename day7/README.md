🚀 AWS EC2 + Docker + Jenkins CI/CD Deployment

📖 Project Overview

This project demonstrates how to deploy a Flask web application using AWS EC2, Docker, Docker Hub, and Jenkins Pipeline. The project covers the complete CI/CD workflow from infrastructure setup to automated deployment.

---

🛠️ Technologies Used

- Amazon EC2
- AWS Security Groups
- Ubuntu Linux
- Docker
- Docker Hub
- Jenkins
- Git & GitHub
- Flask (Python)

---

📋 Project Workflow

Step 1: Create AWS EC2 Instance

- Launched an Ubuntu EC2 instance.
- Configured the required instance settings.

Screenshot

"EC2 Instance" (screenshots/01-launch-ec2-instance.png)

---

Step 2: Configure Security Group

Opened the required inbound ports:

- SSH (22)
- HTTP (80)
- Jenkins (8080)
- Custom Application Port (5000)

Screenshot

"Security Group" (screenshots/02-create-security-group.png)

---

Step 3: Connect to EC2 Instance

Connected to the EC2 instance using SSH and verified the connection.

Screenshot

"EC2 Connection" (screenshots/03-connect-ec2.png)

---

Step 4: Install Docker

Installed Docker and verified the installation.

Screenshot

"Docker Installation" (screenshots/04-install-docker.png)

---

Step 5: Docker Hub Login

Logged in to Docker Hub from the EC2 instance.

Screenshot

"Docker Hub Login" (screenshots/05-dockerhub-login.png)

---

Step 6: Build and Run Docker Container

Built the Docker image and started the Flask application container.

Screenshot

"Docker Build" (screenshots/06-docker-build.png)

---

Step 7: Install Jenkins

Installed Jenkins and started the Jenkins service.

Screenshot

"Jenkins Installation" (screenshots/07-install-jenkins.png)

---

Step 8: Unlock Jenkins and Create Admin User

Completed the Jenkins initial setup and created the administrator account.

Screenshot

"Jenkins Admin" (screenshots/08-jenkins-admin.png)

---

Step 9: Configure Jenkins Credentials

Added:

- GitHub Credentials
- Docker Hub Credentials

Screenshot

"Jenkins Credentials" (screenshots/09-jenkins-credentials.png)

---

Step 10: Create Jenkins Pipeline

Created a Jenkins Pipeline job and connected it to the GitHub repository.

Screenshot

"Pipeline" (screenshots/10-pipeline.png)

---

Step 11: Build and Deploy

Executed the Jenkins Pipeline to:

- Clone the GitHub repository
- Build the Docker image
- Push the image to Docker Hub
- Deploy the application

Screenshot

"Pipeline Success" (screenshots/11-build-success.png)

---

Step 12: Application Output

Successfully deployed the Flask Hospital application.

Screenshot

"Website Output" (screenshots/12-website-output.png)

---

📌 Project Architecture

GitHub Repository
⬇️

Jenkins Pipeline
⬇️

Docker Build
⬇️

Docker Hub
⬇️

Deploy on AWS EC2
⬇️

Flask Web Application

---

 Key Learning Outcomes

- Launching AWS EC2 instances
- Configuring Security Groups
- Connecting to EC2 using SSH
- Installing and managing Docker
- Building Docker images
- Using Docker Hub
- Installing and configuring Jenkins
- Managing Jenkins credentials
- Creating Jenkins Pipeline jobs
- Automating CI/CD deployments
- Deploying a Flask application on AWS

---
