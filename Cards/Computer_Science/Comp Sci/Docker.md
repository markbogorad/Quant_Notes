up:: [[Computer Science MOC]]
tags:: #Programming  
# Docker
- A [[Containerization Tools]]

**Key Concepts**
- **Docker Images**:
    - A Docker image is a read-only template that contains the application code, runtime, libraries, and dependencies needed to run an application. Images are built from a Dockerfile, which contains instructions for creating the image.
- **Docker Containers**:
    - A container is a runnable instance of a Docker image. Containers are created from images and can be started, stopped, moved, and deleted.
- **Dockerfile**:
    - A Dockerfile is a text file that contains a series of instructions for building a Docker image. It specifies the base image to use, application code, dependencies, and configuration settings.
- **Docker Hub**:
    - Docker Hub is a cloud-based registry service for storing and sharing Docker images. Developers can pull pre-built images from Docker Hub or push their own images for others to use.
- **Docker Compose**:
    - Docker Compose is a tool for defining and running multi-container Docker applications. It uses a YAML file to configure the application's services, networks, and volumes.
## Basic Commands
- **Build an Image**:
	- `docker build -t myimage .`
- **Run a Container**:
	- `docker run -d -p 80:80 myimage`
- **List Running Containers**:
	- `docker ps`
- **Stop a Container**:
	- `docker stop <container_id>`