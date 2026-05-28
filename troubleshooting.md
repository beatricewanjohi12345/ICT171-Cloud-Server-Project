# Troubleshooting Documentation

## SSH Connection Issues

### Problem
The server initially failed to connect through SSH.

### Cause
Incorrect IP address and firewall configuration.

### Solution

The following were checked:
- Correct public IP address
- NSG inbound rules
- SSH port 22 access
- Correct username

SSH connection command used:

```bash
ssh azureuser@20.5.139.113
```

---

## NGINX Service Issues

### Problem
The website did not load correctly after installation.

### Cause
NGINX service was not running.

### Solution

The following commands were used:

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
sudo systemctl status nginx
```

---

## DNS Propagation Delay

### Problem
The domain name did not immediately connect to the server.

### Cause
DNS propagation delay after configuring A records.

### Solution

Waited for DNS propagation and verified DNS settings through the domain registrar panel.

---

## SSL Certificate Errors

### Problem
HTTPS initially failed during SSL setup.

### Cause
DNS records were not fully propagated before running Certbot.

### Solution

SSL was reconfigured using:

```bash
sudo certbot --nginx -d bettyzen.online -d www.bettyzen.online
```

---

## Permission Errors

### Problem
Scripts could not execute properly.

### Cause
Execute permissions were missing.

### Solution

```bash
chmod +x testscript
```

---

## Cron Job Issues

### Problem
The backup script did not execute automatically.

### Cause
Incorrect cron formatting and file path configuration.

### Solution

The crontab file was corrected using:

```bash
sudo nano /etc/crontab
```

Correct cron configuration:

```bash
0 * * * * ubuntu /usr/bin/testscript
```

---

## Lessons Learned

- Importance of proper DNS configuration
- Importance of Linux permissions
- Importance of automation using cron jobs
- Importance of server troubleshooting skills
- Importance of documentation during deployment
