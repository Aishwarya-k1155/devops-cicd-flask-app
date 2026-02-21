# CI/CD Pipeline using GitHub Actions and Docker
## Project Overview

### This project demonstrates the implementation of a complete CI/CD pipeline using GitHub Actions and Docker. The objective was to automate the process of building and publishing a Docker image whenever changes are pushed to the main branch.

### The application used in this project is a simple Flask-based service that exposes a health check endpoint.

## Architecture

Source Code → GitHub Repository
Push to main → GitHub Actions Triggered
GitHub Actions → Build Docker Image
GitHub Actions → Push Image to Docker Hub
Docker Hub → Pull and Run Container

## Technology Stack

Python (Flask)

Docker

GitHub Actions

Docker Hub

Git

## CI/CD Workflow

### The workflow is configured to trigger automatically on every push to the main branch.

### Workflow file location:

.github/workflows/docker.yml

### Pipeline Steps:

Checkout source code

Log in to Docker Hub using GitHub Secrets

Build Docker image from Dockerfile

Push Docker image to Docker Hub

### This ensures that every code update results in a new container image build and deployment to the image registry.

## Docker Image

### Docker Hub Repository:

https://hub.docker.com/r/aishwaryakopulwar1155/devops-cicd-flask-app

### Tag used:

latest

### The image is automatically updated whenever changes are pushed to the repository.

## Running the Application

### Pull the image:

docker pull aishwaryakopulwar1155/devops-cicd-flask-app:latest

### Run the container:

docker run -p 5000:5000 aishwaryakopulwar1155/devops-cicd-flask-app

### Access the application in the browser:

http://localhost:5000/health

### Expected response:

{"status":"OK"}

## Key Outcomes

Implemented automated CI/CD pipeline using GitHub Actions

Integrated secure authentication using GitHub Secrets

Containerized a Flask application using Docker

Automated Docker image build and push process

Validated end-to-end container deployment locally
