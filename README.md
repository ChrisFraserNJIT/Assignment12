# FastAPI User & Calculation App

This FastAPI application provides user authentication and calculation management endpoints with secure password handling (bcrypt), JWT authentication, and full CRUD functionality for calculations. The app is containerized with Docker and uses GitHub Actions for CI/CD.

---

## Features

- **User Routes**: Register, login, JWT token generation  
- **Calculation Routes (BREAD)**: Browse, Read, Edit, Add, Delete calculations  
- **Testing & CI/CD**: Integration tests with `pytest`, automated GitHub Actions workflow, Docker deployment

---

## Running the Application Locally

1. **Create a virtual environment and activate it**

python3 -m venv venv
source venv/bin/activate
Install dependencies


pip install --upgrade pip
pip install -r requirements.txt
Run the app


uvicorn app.main:app --reload --port 8001
Access the API documentation
Open your browser and go to http://127.0.0.1:8001/docs to interact with the endpoints using Swagger UI.

Running Tests
Run all tests locally using pytest:


pytest
This will execute integration tests for user registration/login and calculation routes.

Docker
Build and run locally


docker build -t chrisfraser286/module12:latest .
docker run -p 8001:8001 chrisfraser286/module12:latest
Pull from Docker Hub


docker pull chrisfraser286/module12:latest
docker run -p 8001:8001 chrisfraser286/module12:latest
CI/CD
GitHub Actions workflow automatically:

Builds the Docker image

Runs tests for user and calculation routes

Deploys the Docker image to Docker Hub

## Links
GitHub Repository: https://github.com/ChrisFraserNJIT/Assignment12

Docker Hub Repository: https://hub.docker.com/repository/docker/chrisfraser286/module12/

## Reflection
Developing this application provided hands-on experience with FastAPI, secure password handling using bcrypt, JWT authentication, Docker containerization, and CI/CD with GitHub Actions.

Challenges included configuring bcrypt correctly to handle password length restrictions and ensuring all integration tests pass in the CI/CD workflow. Working through these challenges strengthened understanding of production-ready backend development, API design, testing, and deployment practices. Accidently made the access token for Docker Hub Read-Only which broke the github actions.

