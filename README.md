# Automated CI/CD Pipeline

A complete DevOps project demonstrating automated CI/CD deployment using GitHub, GitHub Actions, Jenkins, Docker, Ansible and AWS EC2.

## Project Overview

This project demonstrates how a web application can be automatically built, tested, containerized and deployed using modern DevOps tools.

## Technology Stack

- GitHub
- GitHub Actions
- Jenkins
- Docker
- Ansible
- AWS EC2
- Nginx
- HTML
- Git

## CI/CD Workflow

Developer
↓
GitHub
↓
GitHub Actions
↓
Jenkins
↓
Docker
↓
Docker Registry
↓
Ansible
↓
AWS EC2
↓
Live Application

## Project Structure

automated-cicd-pipeline/

├── app/
│   └── index.html

├── docker/
│   └── Dockerfile

├── ansible/
│   ├── inventory
│   └── deploy.yml

├── jenkins/
│   └── Jenkinsfile

├── .github/
│   └── workflows/
│       └── ci.yml

├── .gitignore

└── README.md

## Run Locally

Build the Docker image:

docker build -f docker/Dockerfile -t automated-cicd-pipeline .

Run the container:

docker run -d -p 8080:80 --name cicd-app automated-cicd-pipeline

Open:

http://localhost:8080

## CI/CD Pipeline

The pipeline performs the following tasks:

1. Developer pushes code to GitHub.
2. GitHub Actions validates the Docker build.
3. Jenkins checks out the latest code.
4. Jenkins builds the Docker image.
5. Docker container is tested.
6. Docker image is pushed to a container registry.
7. Ansible connects to AWS EC2.
8. Ansible deploys the Docker container.
9. The application becomes available through the EC2 public IP.

## Future Improvements

- Docker Hub integration
- Jenkins webhook
- AWS EC2 deployment
- HTTPS using SSL
- AWS CloudFormation
- Terraform infrastructure
- Monitoring with Prometheus and Grafana
