# Laboratory 04 - Cloud Native Engineer

## Mission Overview

This laboratory introduced the fundamentals of cloud-native engineering by comparing virtualization and containerization and by deploying an Nginx web server using Docker. The activity demonstrated how containers provide a lightweight and efficient way to package and run applications.

## Objectives

- Understand the difference between virtual machines and containers.
- Identify the advantages and limitations of containerization.
- Verify the Docker environment.
- Pull a container image from Docker Hub.
- Deploy and test an Nginx web server using Docker.
- Manage the lifecycle of a Docker container.
- Document the commands and observations from the activity.

## Docker Commands Executed

The following Docker commands were used during the laboratory:

```bash
docker --version
docker info
docker pull nginx
docker run -d --name my-nginx -p 8080:80 nginx
docker ps
curl http://localhost:8080
docker stop my-nginx
docker ps
docker rm my-nginx
