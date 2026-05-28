# Linux Backup Script Documentation

## Script Overview

A Bash backup automation script was developed on the Ubuntu Linux server.

The purpose of the script was to:
- backup files from the Documents directory,
- compress the backup into a zip archive,
- automatically include the current date in the filename,
- and automate execution using cron scheduling.

This scripting task demonstrates Linux automation, file management, and server administration skills.

---

## Creating Test Files

The following commands were used to create sample files and directories for testing the backup process.

```bash
touch file1
touch file2
touch file3
touch file4
touch file5

mkdir testfolder
cd testfolder

touch file11
touch file22
touch file33
touch file44
touch file55
```

---

## Bash Script Code

```bash
#!/bin/bash

now=$(date +"%d_%m_%y")

cp -R /home/ubuntu/Documents/* /home/ubuntu/backup/

zip -r $now.zip /home/ubuntu/backup/*

cp $now.zip /home/ubuntu/

scp -i /home/ubuntu/key.pem $now.zip ubuntu@20.5.139.113:/home/ubuntu/
```

---

## Script Explanation

The script performs the following tasks:

1. Creates a variable containing the current date
2. Copies files from the Documents directory into the backup directory
3. Compresses the backup into a zip archive
4. Saves the zip archive using the current date
5. Transfers the backup file to the cloud server using SCP

---

## Making the Script Executable

The following command was used to provide execute permissions.

```bash
chmod +x testscript
```

The script was then executed using:

```bash
./testscript
```

---

## Cron Job Automation

The cron scheduler was configured to automatically execute the script every hour.

The crontab file was edited using:

```bash
sudo nano /etc/crontab
```

The following cron entry was added:

```bash
0 * * * * ubuntu /usr/bin/testscript
```

---

## Script Benefits

- Automates server backups
- Reduces manual administration
- Improves disaster recovery capability
- Demonstrates Linux scripting skills
- Demonstrates task scheduling using cron

---

## Verification

The script execution was verified through:
- successful zip archive creation,
- automated backup generation,
- and successful file transfer operations.
