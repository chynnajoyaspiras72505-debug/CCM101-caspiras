# Laboratory 08 - Cloud Security Engineer

## Mission Overview

This mission focuses on securing an Ubuntu web server using a host-based firewall. The activity demonstrates defense in depth by deploying a web application, configuring UFW, enforcing a Default Deny policy, and allowing only the network traffic required by the application.

## Objectives

- Understand the Attack Surface and Principle of Least Privilege.
- Perform a basic security audit of active network ports.
- Configure UFW with a Default Deny policy.
- Allow SSH and HTTP traffic on the required ports.
- Document firewall rules and security practices using Markdown.

## Commands Executed

```bash
docker run -d -p 8080:80 --name secure-web-app nginx
curl http://localhost:8080

sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose

sudo ufw allow 8080/tcp
sudo ufw status numbered
curl http://localhost:8080
Skills Learned
Through this mission, I learned how to apply basic cloud security principles to a Linux server. I learned the Principle of Least Privilege (PoLP), which means providing users and services only the permissions they need. I also learned how the Attack Surface represents possible entry points that can be used to access or affect a server.
I learned how a Default Deny firewall policy blocks incoming traffic unless it is specifically allowed. I practiced configuring UFW (Uncomplicated Firewall) and learned how to allow SSH before enabling the firewall to avoid losing administrative access. I also learned how to allow only the required TCP port 8080 for the Nginx web application while keeping other incoming traffic blocked.
I gained practical experience deploying an Nginx web server container with Docker, mapping port 8080, and verifying the application using curl. I learned how to check the firewall status using sudo ufw status verbose and verify individual firewall rules using sudo ufw status numbered.
This mission improved my understanding of attack surface reduction, granular port management, host-based firewall protection, and defense in depth. I also improved my Linux command-line skills, Docker usage, security troubleshooting, Markdown documentation, screenshot-based evidence collection, and GitHub portfolio management.
