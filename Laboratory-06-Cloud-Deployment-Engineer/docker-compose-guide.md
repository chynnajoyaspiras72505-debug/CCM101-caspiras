# Docker Compose Guide

## What does the `services:` block do?

The `services:` block in a Docker Compose file defines the containers that make up the application. In this laboratory, it defines two services: `database`, which runs MariaDB, and `app`, which runs Nextcloud. Each service contains its own configuration such as the Docker image, environment variables, and ports.

## How does the Nextcloud app container find the database container?

The Nextcloud container finds the MariaDB container through the `MYSQL_HOST` environment variable. In the Compose file, `MYSQL_HOST` is set to `database`, which is the service name of the MariaDB container. Docker Compose creates a shared network for the services and allows the service name `database` to be used as the hostname, so Nextcloud can communicate with MariaDB without manually specifying an IP address.

## What is the difference between `docker run` and `docker-compose up -d`?

The `docker run` command is commonly used to create and start an individual container by providing its configuration directly in the command. In comparison, `docker-compose up -d` reads the configuration from the `docker-compose.yml` file and can create and start multiple related containers together. The `-d` option runs the containers in detached mode or in the background. Using Docker Compose makes a multi-container application easier to deploy and manage because its configuration is stored in one YAML file.
