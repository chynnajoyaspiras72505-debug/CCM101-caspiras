# Laboratory 09 - Cloud Automation Engineer

## Mission Overview

This mission focuses on automating cloud operations using Bash scripting and Linux Cron. A backup script was created to compress application data, and a Cron job was configured to run the backup automatically every day at 2:00 AM.

## Objectives

- Understand Bash scripting and variables.
- Create and execute an automated backup script.
- Modify Linux file permissions using chmod.
- Configure a Linux Cron job for scheduled automation.
- Document automation tasks using Markdown.

## Commands Executed

mkdir app-data
echo "This is critical client data." > app-data/data.txt
chmod +x backup.sh
./backup.sh
ls -l backups/
crontab -l
env EDITOR=nano crontab -e

## Skills Learned

- Writing Bash scripts.
- Using variables in automation scripts.
- Compressing files using tar.
- Modifying file permissions using chmod.
- Scheduling automated tasks using Cron.
- Documenting cloud automation work using Markdown.

