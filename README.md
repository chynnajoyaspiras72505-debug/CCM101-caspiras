# Laboratory 07 - Cloud Operations Engineer

## Mission Overview

This mission focuses on monitoring a containerized web application and using operational tools to observe system and container health. It includes establishing a host baseline, generating web traffic, reviewing application logs, and monitoring container resource usage.

## Objectives

- Establish a baseline for host memory and disk resources.
- Deploy and test an Nginx web server container.
- Generate successful and failed HTTP requests.
- Inspect application logs for troubleshooting.
- Monitor CPU and memory usage of the container.

## Monitoring Commands Executed

```bash
free -h
df -h /
top
docker run -d -p 8080:80 --name client-website nginx
curl http://localhost:8080/
curl http://localhost:8080/
curl http://localhost:8080/
curl http://localhost:8080/hidden-admin-page
docker logs client-website
docker stats --no-stream
