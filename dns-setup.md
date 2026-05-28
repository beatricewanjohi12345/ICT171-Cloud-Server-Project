# DNS CONFIGURATION DOCUMENTATION

## Introduction

This document explains the DNS configuration process used to connect the custom domain name to the Microsoft Azure cloud server.

The domain used for this project was:

```text
bettyzen.online
```

---

# Purpose of DNS

DNS (Domain Name System) is used to translate human-readable domain names into IP addresses that computers use to communicate over the Internet.

Without DNS, users would need to access the website using the public IP address directly.

---

# Azure Public IP Address

The Microsoft Azure virtual machine was configured with the following public IP address:

```text
20.5.139.113
```

---

# Domain Configuration

The custom domain name was configured to point to the Azure virtual machine using DNS records.

The following DNS record type was used:

| Record Type | Purpose |
|---|---|
| A Record | Maps the domain name to the public IP address |

---

# DNS Record Configuration

The A record was configured as follows:

| Hostname | Type | Value |
|---|---|---|
| @ | A | 20.5.139.113 |
| www | A | 20.5.139.113 |

---

# DNS Propagation

After configuring the DNS records, time was required for DNS propagation across global DNS servers.

Once propagation completed, the website became accessible through:

```text
https://www.bettyzen.online
```

---

# Testing DNS Configuration

The following methods were used to verify DNS functionality:

## Browser Test

The website was successfully accessed through the domain name.

## Ping Test

```bash
ping bettyzen.online
```

## NSLookup Test

```bash
nslookup bettyzen.online
```

These commands confirmed that the domain correctly resolved to the Azure server IP address.

---

# Conclusion

The DNS configuration was successfully completed, allowing the custom domain name to connect publicly to the Microsoft Azure Linux web server.



