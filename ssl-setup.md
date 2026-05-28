# SSL/TLS Configuration Documentation

## SSL/TLS Overview

SSL/TLS was configured to secure communication between users and the web server.

HTTPS encryption was implemented to improve website security and protect data transmitted between the client browser and the server.

---

## Installing Certbot

The following commands were used to install Certbot and the NGINX SSL plugin.

```bash
sudo apt update
sudo apt install certbot python3-certbot-nginx -y
```

---

## Generating the SSL Certificate

The following command was used to automatically configure SSL for the website domain.

```bash
sudo certbot --nginx -d bettyzen.online -d www.bettyzen.online
```

---

## SSL Verification

The SSL certificate was successfully installed and HTTPS was enabled.

The website could then be securely accessed using:

```text
https://www.bettyzen.online
```

---

## Automatic Certificate Renewal

Certbot automatic renewal was enabled to ensure the SSL certificate renews before expiration.

The following command was used to test automatic renewal:

```bash
sudo certbot renew --dry-run
```

---

## Security Benefits of SSL/TLS

- Encrypts communication between the user and server
- Improves website trust and security
- Prevents interception of sensitive data
- Enables HTTPS secure browsing
