Cloud Computing Training - Day 5

Topics Covered

Docker Containerization

- Creating and editing application files using "vim"
- Building Docker Images
- Running Docker Containers
- Hosting a Simple Python Website using Docker

Commands Practiced

vim app.py
docker build -t mywebsite .
docker images
docker run -d -p 80:80 mywebsite
docker ps

Jenkins Installation

- Installed Java (OpenJDK 21)
- Added Jenkins Repository
- Installed Jenkins
- Started Jenkins Service
- Configured Jenkins on EC2
- Accessed Jenkins Dashboard through Browser

Commands Practiced

sudo apt update
sudo apt install openjdk-21-jdk -y
sudo apt install jenkins -y
sudo systemctl start jenkins
sudo systemctl status jenkins
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

Outcome

- Successfully deployed a website using Docker.
- Learned how to edit files using Vim.
- Installed and configured Jenkins on an AWS EC2 instance.
- Accessed the Jenkins web interface and completed initial setup.
