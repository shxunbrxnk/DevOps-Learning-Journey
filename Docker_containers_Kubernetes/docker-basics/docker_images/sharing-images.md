# Sharing Docker Images

## Goal

The main goal of using Docker is to create reliable and reproducible environments.

This is important when:
- Multiple developers are working on the same project
- Applications need to run the same way on different machines

---

## Key Concepts

- A container is a running instance of an image
- Containers cannot be shared directly
- Docker images can be shared

Anyone who has the image can create a container from it.

---

## Ways to Share Docker Images

### 1. Share Dockerfile and Source Code

You can share:
- Dockerfile
- Application source code
- Dependencies

This allows someone else to build the image themselves.

---

### 2. Push Image to Docker Hub

You can build the image once and push it to Docker Hub.

Others can then pull the image and run it without rebuilding.

---

## Steps to Push an Image to Docker Hub

### 1. Build the image

docker build -t oldimage .
docker tag oldimage username/newimage
docker push username/newimage
