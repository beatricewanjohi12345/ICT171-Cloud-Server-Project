 # TROUBLESHOOTING DOCUMENTATION

## Introduction

During the implementation of the cloud server project, several technical issues were encountered and resolved.

This document explains the troubleshooting steps used throughout the project.

---

# SSH Connection Issues

## Problem

The server initially failed to connect through SSH.

## Solution

The following checks were performed:

- Verified the correct public IP address
- Confirmed SSH port 22 was enabled in Azure Network Security Group
- Confirmed the virtual machine was running
- Verified the correct username was used

Example SSH command:

```bash
ssh azureuser@20.5.139.113
```

---

# NGINX Not Displaying Website

## Problem

The website changes did not appear after editing the HTML file.

## Solution

NGINX was restarted using:

```bash
sudo systemctl restart nginx
```

Browser cache was also refreshed using:

```text
CTRL + F5
```

---

# DNS Propagation Delay

## Problem

The domain name did not immediately connect to the server.

## Solution

Time was allowed for DNS propagation after configuring the A records.

The DNS configuration was verified using:

```bash
ping bettyzen.online
```

and

```bash
nslookup bettyzen.online
```

---

# Permission Issues

## Problem

Permission denied errors occurred while editing website files.

## Solution

Administrative privileges were used with sudo:

```bash
sudo nano /var/www/html/index.html
```

---

# SSL Certificate Issues

## Problem

HTTPS was not initially enabled.

## Solution

Certbot and Let's Encrypt were installed and configured:

```bash
sudo certbot --nginx
```

The NGINX configuration was automatically updated to support HTTPS.

---

# Conclusion

The troubleshooting process helped improve understanding of Linux server administration, cloud deployment, DNS configuration and web server management.
