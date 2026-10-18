# Backup Script Guide

## Full Backup Script

#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

mkdir -p $BACKUP_DIR
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"

## File Permissions

The `chmod +x backup.sh` command adds execute permission to the backup script. This allows the script to be executed directly using `./backup.sh`.

## Cron Schedule

0 2 * * * /root/backup.sh

### Cron Field Breakdown

- Minute: 0 — runs at minute 0.
- Hour: 2 — runs at 2 AM.
- Day of Month: * — runs every day of the month.
- Month: * — runs every month.
- Day of Week: * — runs every day of the week.

The complete cron expression means that `/root/backup.sh` runs automatically every day at 2:00 AM.

