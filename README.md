FastAPI CI/CD Demo

A simple REST API built with Python and FastAPI, with automated tests, Docker containerization, and a CI/CD pipeline using GitHub Actions.

This project demonstrates a basic software delivery workflow: testing the application, building a Docker image, and publishing the image to Docker Hub.

Technologies :

* Python 3.11 — Programming language

* FastAPI — REST API framework

* Pytest — Automated testing

* Docker — Application containerization

* GitHub Actions — Continuous Integration and Continuous Delivery (CI/CD)

* Docker Hub — Docker image registry

Features:

* GET / — Returns a welcome message.

* GET /health — Returns the API health status.

* Automated tests for both endpoints.

* Docker image built through GitHub Actions.

* Automated image publishing to Docker Hub when changes are pushed to the main branch.

Getting Started

Prerequisites

To run the Docker image, you need:

1. Docker Desktop or Docker Engine.

2. An internet connection to download the image.

2. Run with Docker

* You do not need to install Python or the application dependencies when using the published Docker image.

1. Pull the image from Docker Hub:
    
    docker pull cavila85/ci-cd-demo:latest

2. Start the container:

    docker run --rm -p 8000:8000 cavila85/ci-cd-demo:latest

3. Open the following URLs in your browser:

    API root: http://localhost:8000/

    Health check: http://localhost:8000/health

    Interactive API documentation: http://localhost:8000/docs

    Alternative API documentation: http://localhost:8000/redoc


Example Responses

GET /

{
  "message": "Hello from the pipeline CI/CD!"
}

GET /health

{
  "status": "healthy"
}

Run Tests Locally

To run the tests from the source code, you need Python 3.11 or a compatible version.

Clone the GitHub repository:
Enter in the URL to have acces to the repository.
git clone -> [GITHUB_REPOSITORY_URL](https://github.com/ChristopherAvila/ci-cd-demo.git)

Get to the directory.
cd ci-cd-demo

Create and activate a virtual environment:

* python -m venv .venv

Windows PowerShell:

* .\.venv\Scripts\Activate.ps1

Linux or macOS:

* source .venv/bin/activate

Install the project dependencies:

* python -m pip install -r requirements.txt

Run the automated tests:

* pytest

CI/CD Pipeline

The project uses GitHub Actions to automate the following steps:

1. Check out the source code.

2. Set up Python.

3. Install dependencies.

4. Run automated tests.

5. Build the Docker image.

6. Authenticate with Docker Hub.

7. Publish the Docker image when code is pushed to main.

8. The pipeline helps detect problems before publishing a new image.

Project Goals

This project was created to practice and demonstrate:

1. REST API development.

2. Automated testing.

3. Docker image creation and distribution.

4. CI/CD workflow configuration.

5. Basic application health checks.

--Author--

Christopher Ávila Castillo

GitHub: [https://github.com/ChristopherAvila]

Docker Hub: [https://hub.docker.com/u/cavila85]