# CloudNova Technologies — Enterprise Cloud Architect

## 1. System Overview

CloudNova is a cloud infrastructure project that uses Ubuntu Server, Docker, Nextcloud, MariaDB, UFW, Bash, and Cron.

The system is hosted inside an Ubuntu Server virtual machine running on Oracle VM VirtualBox. Nextcloud provides the file-sharing application, while MariaDB stores the application database.

## 2. Host Machine

| Configuration | Details |
|---|---|
| Host Machine | ASUS TUF Gaming A15 |
| Host OS | Windows 11 Home Single Language |
| Host RAM | 8 GB |
| Hypervisor | Oracle VM VirtualBox |

## 3. Ubuntu Server Configuration

| Configuration | Details |
|---|---|
| Operating System | Ubuntu Server 24.04.5 LTS |
| Hostname | cloudnova |
| Username | cloudadmin |
| vCPU | 3 |
| RAM | 2304 MB |
| Disk | 25 GB |
| Network Mode | Bridged Adapter |
| Server IP | 192.168.1.78 |

Useful commands:

    hostnamectl
    hostname -I
    free -h

SSH access:

    ssh cloudadmin@192.168.1.78

Enable SSH service:

    sudo systemctl enable --now ssh

## 4. Docker and Docker Compose

Docker Engine and Docker Compose are used to deploy and manage the Nextcloud and MariaDB containers.

The application files are stored in:

    /opt/nextcloud

A private `.env` file stores the database credentials and VM IP configuration.

Validate the Compose configuration:

    docker compose config --quiet

Start the application:

    docker compose up -d

Check the containers:

    docker compose ps

The main containers are:

- `nc-app` — Nextcloud application
- `nc-db` — MariaDB database

## 5. Nextcloud and MariaDB

Nextcloud is exposed through port **8080**.

MariaDB uses the internal Docker network and is not directly exposed to the host.

Nextcloud access:

    http://192.168.1.78:8080

The Docker Compose configuration uses persistent volumes:

- `nc_data` → `/var/www/html`
- `db_data` → `/var/lib/mysql`

These volumes preserve application and database data.

Avoid using:

    docker compose down -v

because the `-v` option removes the persistent volumes.

## 6. Firewall Security

UFW is configured using a default-deny incoming policy.

Configure the firewall:

    sudo ufw default deny incoming
    sudo ufw default allow outgoing
    sudo ufw allow 22/tcp
    sudo ufw allow 8080/tcp
    sudo ufw enable

Check the firewall:

    sudo ufw status verbose

Port 22 is used for SSH access, while port 8080 is used for Nextcloud.

## 7. Database Backup Automation

The backup script is stored at:

    /opt/nextcloud/automation-script.sh

The script creates compressed MariaDB database backups and stores them in:

    /opt/backups

The script uses the database password from the private `.env` file.

Make the script executable:

    chmod +x /opt/nextcloud/automation-script.sh

The backup file is created using the following naming format:

    nextcloud-db-YYYY-MM-DD_HH-MM-SS.sql.gz

Backups older than seven days are automatically removed.

## 8. Cron Scheduling

Cron is used to run the database backup automatically.

The scheduled job runs every day at **2:00 AM Philippine time**.

Cron entry:

    0 2 * * * /bin/bash /opt/nextcloud/automation-script.sh >> /opt/backups/cron.log 2>&1

Verify the Cron configuration:

    crontab -l

## 9. Maintenance Procedures

Start the application:

    cd /opt/nextcloud
    docker compose up -d

Check containers:

    docker compose ps

View container logs:

    docker compose logs

Restart the application:

    docker compose restart

Check firewall status:

    sudo ufw status verbose

Check available disk space:

    df -h

## 10. Troubleshooting

### Nextcloud cannot be accessed

Check the VM IP:

    hostname -I

Check the containers:

    docker compose ps

Check the application logs:

    docker compose logs app

Verify that port 8080 is allowed:

    sudo ufw status verbose

### MariaDB container is not running

Check the database container:

    docker compose ps

View database logs:

    docker compose logs db

### SSH connection fails

Check the SSH service:

    sudo systemctl status ssh

Check the VM IP:

    hostname -I

Verify that port 22 is allowed:

    sudo ufw status verbose

### Backup is not generated

Check the script:

    ls -lh /opt/nextcloud/automation-script.sh

Run it manually:

    /opt/nextcloud/automation-script.sh

Check the backup directory:

    ls -lh /opt/backups

Check Cron:

    crontab -l

## 11. Data Persistence

Persistent Docker volumes are used to protect application and database data.

The following volumes are required:

- `nc_data`
- `db_data`

After restarting the Ubuntu Server, start the containers again and verify that previously stored Nextcloud data is still available.

## 12. References

- Docker Documentation — https://docs.docker.com/
- Nextcloud Administration Manual — https://docs.nextcloud.com/server/latest/admin_manual/
- Ubuntu Server Documentation — https://documentation.ubuntu.com/server/
- Oracle VirtualBox Documentation — https://www.virtualbox.org/wiki/Documentation
