## Project Overview

For my CoderCo Networking assignment, I deployed an NGINX web server on an AWS EC2 instance and connected it to my personal domain, subeyda.co.uk, using Cloudflare DNS.

The goal was to understand how DNS, public IP addresses, cloud servers, and HTTP work together to make a website accessible through a domain name.

## Technologies Used

- AWS EC2 (Ubuntu 24.04 LTS)
- NGINX
- Cloudflare DNS
- Linux
- HTTP (Port 80)
## Step 1: Launch an AWS EC2 Instance

I launched an EC2 instance using the following configuration:

- Region: Europe (London) - eu-west-2
- Operating System: Ubuntu 24.04 LTS
- Instance Type: t3.micro
- Instance Name: networking-nginx

I configured the security group to allow:
- HTTP (Port 80) to make the website publicly accessible.
- SSH (Port 22) for remote administration using EC2 Instance Connect.

I then connected to the instance using the browser-based EC2 Instance Connect terminal.

## Step 2: Install and Start NGINX

After connecting to my Ubuntu EC2 instance, I updated the package list:

```bash
sudo apt update
```

I then installed NGINX:

```bash
sudo apt install nginx -y
```

Next, I enabled and started the NGINX service:

```bash
sudo systemctl enable --now nginx
```

Finally, I checked that NGINX was running:

```bash
sudo systemctl status nginx
```

The service showed **active (running)**, confirming that NGINX was successfully installed and running.

I tested the EC2 public IP address in my browser and saw the default NGINX welcome page.

