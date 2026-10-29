# Experiment 7: Develop a Simple Containerized Application Using Docker

## Aim
To develop and run a simple web application inside a Docker container.

## Objectives
1. To understand application containerization.
2. To create a simple web application.
3. To write a Dockerfile for the application.
4. To build a Docker image.
5. To run and test the application inside a Docker container.

## Software Requirements
- Docker Engine or Docker Desktop
- GitHub account
- Text editor
- Web browser

## Introduction
Docker is a containerization platform that packages an application and its dependencies into a container. Containers provide a consistent environment for running applications across different systems. A Dockerfile contains instructions for building a Docker image, which is used to create and run containers.

## Procedure
1. Create a project directory named `docker-app`.
2. Create an `index.html` file containing the web application.
3. Create a Dockerfile to configure the web server.
4. Build a Docker image using the Docker build command.
5. Run a container from the generated image.
6. Open the application in a web browser.
7. Verify that the application is accessible.

## Source Code

### 1. index.html

```html
<!DOCTYPE html>
<html>
<head>
    <title>Docker Application</title>
</head>
<body>
    <h1>Hello from Docker!</h1>
    <p>My first containerized web application.</p>
</body>
</html>
```

### 2. Dockerfile

```dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
```

## Docker Commands

- `docker --version` – Checks the Docker version.
- `docker build -t docker-app .` – Builds a Docker image using the Dockerfile in the current directory.
- `docker images` – Lists available Docker images.
- `docker run -d -p 8080:80 --name myapp docker-app` – Runs the application in a container.
- `docker ps` – Lists running containers.
- `docker logs myapp` – Displays the container logs.
- `docker stop myapp` – Stops the container.
- `docker rm myapp` – Removes the stopped container.

## Expected Output
When the container is running, open `http://localhost:8080` in a web browser.

The page displays:

Hello from Docker!

My first containerized web application.

## Result
Successfully developed a simple web application, built a Docker image, and prepared it to run inside a container.

## Applications
- Application deployment
- Software testing
- Development environment setup
- Microservices architecture
- DevOps automation
