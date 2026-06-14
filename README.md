# React Todo App - Dockerized

A React Todo application containerized using Docker with a production-ready multi-stage build and Nginx.

## Project Overview

This project demonstrates how to package a React application into a lightweight production Docker image using a multi-stage build. The application is served with Nginx and can be run either as a standalone container or with Docker Compose.

## Features

* React Todo application
* Multi-stage Docker build
* Nginx production server
* Docker Compose support
* Optimized image build using `.dockerignore`
* Production-ready container setup

---

## Tech Stack

* React
* Docker
* Docker Compose
* Nginx

---

## Project Structure

```text
react-todo-app/
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
├── nginx.conf
├── package.json
├── public/
├── src/
└── README.md
```

---

## Build the Docker Image

```bash
docker build -t react-todo-app:2.0 .
```

---

## Run the Container

```bash
docker run -d \
  --name react-todo-app \
  -p 8080:80 \
  react-todo-app:2.0
```

Open your browser:

```
http://localhost:8080
```

---

## Run with Docker Compose

Start:

```bash
docker compose up -d
```

Stop:

```bash
docker compose down
```

View logs:

```bash
docker compose logs
```

---

## Inspect the Image

Show image size:

```bash
docker images react-todo-app
```

Inspect image layers:

```bash
docker history react-todo-app:2.0
```

Open a shell inside the container:

```bash
docker run -it react-todo-app:2.0 sh
```

Explore the Nginx files:

```bash
ls
ls /usr/share/nginx/html
```

---

## Docker Concepts Practiced

* Multi-stage Docker builds
* Image optimization
* Docker image layers
* Docker caching
* `.dockerignore`
* Nginx container
* Port mapping
* Docker Compose
* Container inspection

---

## Git History

| Commit    | Description                                                      |
| --------- | ---------------------------------------------------------------- |
| `7b429f1` | Added `.dockerignore` for build optimization                     |
| `51c7b37` | Added Docker Compose configuration                               |
| `3fa1e59` | Containerized React app using multi-stage Docker build and Nginx |
| `ffd8a63` | Initialized React Todo App project                               |

---

## Learning Outcomes

Through this project, I learned how to:

* Containerize a React application
* Create efficient multi-stage Docker images
* Serve static files using Nginx
* Reduce Docker build context using `.dockerignore`
* Use Docker Compose for application management
* Inspect Docker image layers
* Explore running containers

---

## Author

**Saeed Asif**

BSCS Student | Aspiring Junior DevOps / Cloud Engineer

Linkedin : https://www.linkedin.com/in/saeedasif-devops/
