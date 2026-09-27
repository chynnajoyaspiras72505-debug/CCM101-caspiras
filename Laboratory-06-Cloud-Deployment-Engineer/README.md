# Laboratory 06 - Cloud Deployment Engineer

## Mission Overview

This laboratory focused on deploying a multi-tier private cloud storage application using Docker Compose. The deployment used Nextcloud as the web application tier and MariaDB as the database tier. Both services were defined in a YAML configuration file and deployed as a multi-container application.

## Objectives

- Understand multi-tier application architecture.
- Understand the purpose and structure of Docker Compose.
- Create and edit YAML configuration files using Linux.
- Deploy Nextcloud and MariaDB using Docker Compose.
- Apply Infrastructure as Code concepts.
- Document the deployment process using Markdown.

## Commands Executed

- `mkdir nextcloud-deployment`
- `cd nextcloud-deployment`
- `nano docker-compose.yml`
- `docker-compose up -d`
- `docker-compose ps`
- `docker-compose down`

## Skills Learned

During this laboratory, I learned how to create and deploy a multi-container application using Docker Compose. I gained experience writing YAML configuration files, configuring environment variables, mapping ports, and connecting a Nextcloud application container to a MariaDB database container. I also learned how Infrastructure as Code makes deployments easier to reproduce, document, and manage.
