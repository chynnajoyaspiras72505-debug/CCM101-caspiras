# Firewall Configuration

## SSH Access

Command used to allow SSH:
sudo ufw allow ssh

This allows SSH traffic so administrators can remotely manage the server.

## Default Deny Policy

Commands used:
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable

The Default Deny policy blocks incoming traffic unless a specific service is explicitly allowed.

## Allow Port 8080

Command used:
sudo ufw allow 8080/tcp

This allows TCP traffic on port 8080 for the web application.

## Security Note

If sudo ufw enable were run before sudo ufw allow ssh, SSH access could be blocked because incoming connections would be denied before the SSH rule was added.

