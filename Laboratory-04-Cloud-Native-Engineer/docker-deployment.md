# Docker Deployment Documentation

## Overview
This document records the Docker deployment of an Nginx web server using Ubuntu and Docker.

## Check Docker Version
```bash
docker --version
```
Docker was successfully installed and verified.

## Pull Nginx Image
```bash
docker pull nginx
```
The latest Nginx image was successfully downloaded.

## Run Nginx Container
```bash
docker run -d --name my-nginx -p 8080:80 nginx
```
The Nginx container was deployed with host port 8080 mapped to container port 80.

## Verify Container
```bash
docker ps
```
The my-nginx container was confirmed to be running.

## Test Nginx
```bash
curl http://localhost:8080
```
The Welcome to nginx page was returned successfully.

## Stop Container
```bash
docker stop my-nginx
```
The container was successfully stopped.

## Remove Container
```bash
docker rm my-nginx
```
The stopped container was successfully removed.

## Conclusion
Docker was successfully used to pull, deploy, test, stop, and remove an Nginx container.
