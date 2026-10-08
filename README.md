# Git and Docker Starter Application

This repository contains a small Python web application used to practice Git, GitHub, and Docker workflows.

## Application

The application listens on port 8000 and returns a text response when accessed over HTTP.

## Verification

The application can be verified from the Docker host by running curl against localhost on port 8080, which maps to port 8000 in the container.

## Usage

Build the Docker image:

```bash
docker build -t git-docker-app:test .
```

Run the application:

```bash
docker run -d --name app-test -p 8080:8000 git-docker-app:test
```

Verify the application:

```bash
curl http://localhost:8080
```

Stop and remove the container:

```bash
docker stop app-test
docker rm app-test
```
