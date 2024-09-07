# Node.js Web Application with CI/CD Pipeline deploy on AWS ECS
This repository contains a Node.js web application with a fully automated CI/CD pipeline using GitHub Actions. The pipeline is configured to build a Docker image, push it to Amazon ECR (Elastic Container Registry), and deploy it to Amazon ECS (Elastic Container Service).

# Project Overview
Application: A simple Node.js web application served using Nginx as a reverse proxy.
CI/CD Pipeline: Automates the process from building the Docker image to deploying it in the cloud, ensuring high efficiency and reliability.

# Key Features
1) Automated Build and Deployment:
GitHub Actions pipeline checks out the code, builds a Docker image using a multi-stage build, and pushes the image to Amazon ECR.

3) ECS Deployment:
The pipeline deploys the image to an ECS service using a task definition.

4) Rollback Functionality:
If the deployment or integration tests fail, the pipeline automatically rolls back to the previous version to ensure availability.

# Technology Stack
Node.js: Backend application
Docker: Containerization of the application
Nginx: Used as a reverse proxy to serve the app
Amazon ECR: Docker image registry
Amazon ECS: For containerized deployment
GitHub Actions: CI/CD pipeline

# How It Works
Code Checkout: The pipeline starts by checking out the latest code from this repository.

Build Docker Image: A multi-stage Docker build is used to create an optimized image of the application.

Push to Amazon ECR: The built Docker image is pushed to a private ECR repository.

Deploy to ECS: The pipeline updates the ECS task definition with the new image and deploys it to the ECS service.
