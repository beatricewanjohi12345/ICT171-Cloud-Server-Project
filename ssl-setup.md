# SSL/TLS CONFIGURATION DOCUMENTATION

## Introduction

SSL/TLS was configured to secure the website connection and enable HTTPS encryption.

SSL helps protect communication between the web server and users by encrypting transmitted data.

The website domain used was:

```text
bettyzen.online
```

---

# Purpose of SSL/TLS

SSL/TLS provides:

- Secure encrypted communication
- Improved website security
- HTTPS browser support
- User trust and authentication
- Protection against data interception

---

# Installing Certbot

Certbot was installed to generate and manage SSL certificates from Let's Encrypt.

The following commands were used:

```bash
sudo apt update
sudo apt install certbot python3-certbot-nginx -y
```

---

# Generating SSL Certificate

The SSL certificate was generated using:

```bash
sudo certbot --nginx
```

During the setup process:

- The domain name was selected
- HTTPS redirection was enabled
- The certificate was automatically configured within NGINX

---

# HTTPS Verification

After SSL configuration, the website became accessible securely using:

```text
https://www.bettyzen.online
```

The browser displayed a secure padlock icon confirming successful SSL configuration.

---

# Testing SSL Configuration

The following checks were performed:

## Browser Verification

The website loaded successfully using HTTPS.

## Certificate Verification

The SSL certificate was verified through the browser certificate information.

## Automatic HTTPS Redirection

HTTP traffic was redirected automatically to HTTPS.

---

# Auto Renewal

Certbot automatic renewal was enabled to maintain certificate validity.

The following command was used to test renewal:

```bash
sudo certbot renew --dry-run
```

---

# Conclusion

SSL/TLS was successfully configured on the Microsoft Azure Linux server using Let's Encrypt and Certbot, allowing secure HTTPS communication for the website.
