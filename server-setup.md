# SERVER SETUP DOCUMENTATION

## Introduction

This document explains the process used to create and configure the ICT171 cloud server project using Microsoft Azure Infrastructure as a Service (IaaS).

The server was manually configured using Ubuntu Linux, SSH remote access and NGINX web server software.

---

# Creating the Azure Virtual Machine

The virtual machine was created through the Microsoft Azure Portal.

Configuration used:

| Component | Configuration |
|---|---|
| Cloud Provider | Microsoft Azure |
| Region | Australia East |
| Operating System | Ubuntu Linux |
| Authentication Type | SSH Public Key |
| Public IP | Enabled |
| Ports Allowed | HTTP (80), HTTPS (443), SSH (22) |

---

# Connecting to the Server Using SSH

The server was remotely accessed using SSH from the terminal.

Example command used:

```bash
ssh azureuser@20.5.139.113
```

SSH allowed secure remote administration of the Linux server.

---

# Updating Ubuntu Linux

The following commands were used to update the operating system packages:

```bash
sudo apt update
sudo apt upgrade -y
```

These commands ensured the server was updated with the latest security patches and software updates.

---

# Installing NGINX Web Server

NGINX was installed using the following command:

```bash
sudo apt install nginx -y
```

The web server service was then started and enabled:

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

---

# Testing NGINX

The following command was used to confirm the NGINX service was running:

```bash
sudo systemctl status nginx
```

The default NGINX page successfully displayed through the public IP address.

---

# Website Deployment

The website files were stored inside:

```bash
/var/www/html
```

The main webpage file used was:

```bash
index.html
```

The file was edited using Nano text editor:

```bash
sudo nano /var/www/html/index.html
```

---

# Restarting NGINX

After making changes to the website files, NGINX was restarted using:

```bash
sudo systemctl restart nginx
```

This allowed the updated website content to display publicly.

---

# Conclusion

The server was successfully configured as a cloud-hosted Linux web server using Microsoft Azure. The website was publicly accessible using the configured domain name and NGINX web server.
