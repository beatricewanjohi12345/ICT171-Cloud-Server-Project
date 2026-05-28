# Server Setup Documentation

## Creating the Azure Virtual Machine

1. Logged into Microsoft Azure Portal
2. Created a new Ubuntu Linux Virtual Machine
3. Selected Australia East region
4. Configured authentication using SSH
5. Allowed HTTP and HTTPS traffic
6. Generated a public IP address

## Connecting to the Server Using SSH

SSH command used:

```bash
ssh azureuser@20.5.139.113
```

**UPDATING THE SERVER**

```bash
sudo apt update
sudo apt upgrade -y
```

**INSTALLING THE NGINX**

```bash
sudo apt install nginx -y
```

**STARTING NGINX**

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```
