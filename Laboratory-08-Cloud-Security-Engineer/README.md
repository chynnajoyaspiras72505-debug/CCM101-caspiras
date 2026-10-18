# Laboratory 08 - Cloud Security Engineer

## Mission Overview

This mission focuses on securing a Linux server using a host-based firewall. The server is audited for open ports, and UFW is configured using a Default Deny policy while allowing only the services required by the application.

## Objectives

- Understand the Principle of Least Privilege and Attack Surface.
- Perform a basic security audit of active network ports.
- Configure UFW with a Default Deny policy.
- Allow SSH and Port 8080 traffic.
- Document firewall rules and security practices.

## Commands Executed

```bash
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw allow 8080/tcp
sudo ufw status numbered

## Skills Learned

- Understanding the Principle of Least Privilege.
- Identifying a server's attack surface.
- Configuring a Linux host-based firewall using UFW.
- Applying a Default Deny security policy.
- Managing network ports based on required services.
- Verifying firewall rules using Linux commands.

