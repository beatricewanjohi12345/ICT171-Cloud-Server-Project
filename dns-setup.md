# DNS Configuration Documentation

## Domain Name Configuration

A custom domain name was configured to allow public access to the cloud server through a user-friendly web address.

Domain Name:

```text
bettyzen.online
```

Public IP Address:

```text
20.5.139.113
```

---

## DNS Provider Configuration

The DNS records were configured through the domain registrar’s DNS management panel.

An A Record was created to point the domain name to the Azure Virtual Machine public IP address.

---

## DNS Record Used

```text
Type: A
Host: @
Value: 20.5.139.113
TTL: Default
```

---

## WWW Subdomain Configuration

An additional DNS record was configured for the www version of the domain.

```text
Type: CNAME
Host: www
Value: bettyzen.online
```

---

## DNS Verification

The DNS configuration was tested by entering the domain name into a web browser to confirm that the website successfully resolved to the Azure server.

The website became publicly accessible through:

```text
https://www.bettyzen.online
```
