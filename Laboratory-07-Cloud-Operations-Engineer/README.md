# Laboratory 07 - Cloud Operations Engineer

## Mission Overview

This mission focuses on monitoring a containerized web application and using operational tools to observe system and container health. It includes establishing a host performance baseline, generating web traffic, reviewing application logs, and monitoring container resource usage.

## Objectives

- Utilize Linux command-line tools to monitor host CPU, memory, and disk capacity.
- Deploy an Nginx web container and monitor its real-time performance using Docker metrics.
- Generate successful and failed HTTP requests and analyze application access logs.
- Document system performance and observability data using Markdown.
- Continue expanding a professional GitHub Cloud Computing portfolio.

## Skills Learned
- Establishing a baseline for Linux host resources. 
- Deploying and testing an Nginx container with Docker.
- Generating HTTP traffic and intentionally testing a 404 error.
- Reading Docker application logs for troubleshooting.
- Monitoring container CPU and memory usage.
- Using Markdown to document cloud operations and observability results.

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



