# Python CI/CD Pipeline using Git, Docker & Jenkins

## Project Overview
This project demonstrates a complete CI/CD pipeline for a Python Flask application using GitHub, Docker, and Jenkins.

## Tech Stack
- Python (Flask)
- Git & GitHub
- Docker
- Jenkins

## Features
- Flask web app with health endpoint
- Dockerized application
- Jenkins pipeline for build & deploy

## How It Works
1. Developer pushes code to GitHub
2. Jenkins pulls the latest code
3. Jenkins builds a Docker image
4. Jenkins runs the container

## Run Locally

```bash
git clone https://github.com/<your-username>/python-ci-cd-project.git
cd python-ci-cd-project
docker build -t python-cicd-app .
docker run -d -p 5000:5000 python-cicd-app

