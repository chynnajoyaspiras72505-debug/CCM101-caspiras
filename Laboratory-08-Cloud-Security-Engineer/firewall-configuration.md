# Firewall Configuration

## Allow SSH

```bash
sudo ufw allow sshThis allows SSH access so administrators can continue managing the server remotely.
Default Deny Policy
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose

The Default Deny policy blocks incoming traffic unless a specific firewall rule allows it, while outgoing traffic remains allowed.
Allow Port 8080
sudo ufw allow 8080/tcp
sudo ufw status numbered

This allows TCP traffic on port 8080 so users can access the Nginx web application.
SSH Warning
If sudo ufw enable is run before sudo ufw allow ssh, the SSH connection may be blocked and the administrator could be locked out of the server.
