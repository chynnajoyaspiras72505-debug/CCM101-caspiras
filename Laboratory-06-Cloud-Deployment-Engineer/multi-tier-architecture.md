# Multi-Tier Architecture

## Two-Tier Architecture

A two-tier architecture separates an application into two main parts: the application tier and the database tier. In this laboratory, the architecture consists of a Nextcloud web application container and a MariaDB database container. The two containers work together while performing different responsibilities.

## Web/Application Tier

The Web/Application Tier provides the interface that users interact with. In this laboratory, Nextcloud serves as the application tier. It handles HTTP requests from users, displays the web interface, and communicates with the database whenever information needs to be stored or retrieved.

## Database Tier

The Database Tier is responsible for storing and managing persistent application data. MariaDB serves as the database tier for Nextcloud. It stores information such as user accounts, credentials, application settings, and file metadata required by the Nextcloud application.

## Why Separate Them?

Keeping the web application and database in separate containers makes the system easier to manage, maintain, and troubleshoot. Each service can be updated or restarted independently, and separating their responsibilities also makes the architecture more flexible than placing both services inside a single container.
