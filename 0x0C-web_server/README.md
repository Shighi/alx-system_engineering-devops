# ALX Web Server Setup

This repository contains scripts and configurations to set up and manage a web server using Nginx, along with various tasks that enhance server management.

## Tasks Overview

### 0. Transfer a File to Your Server
**Script:** `0-transfer_file`
- A Bash script to transfer files to a remote server using `scp`.
- **Requirements:**
  - Accepts 4 parameters: the path to the file, the server's IP, the username for SSH, and the path to the SSH private key.
  - Disables strict host key checking for `scp`.
  - Transfers the file to the user's home directory (`~/`).
- **Usage:**  
  ```bash
  Usage: 0-transfer_file PATH_TO_FILE IP USERNAME PATH_TO_SSH_KEY

1. Install Nginx Web Server
Script: 1-install_nginx_web_server

Install Nginx and configure it to listen on port 80.
Requirements:
Ensure Nginx returns the message "Hello World!" at the root URL.
The script should not use systemctl for restarting Nginx.

2. Setup a Domain Name
File: 2-setup_a_domain_name

Register a .tech domain for free via GitHub Student Pack.
Requirements:
Provide the domain name (e.g., myschool.tech).
Set up DNS records with an A entry pointing to your server's IP.
Ensure the domain is configured correctly by checking the whois response.

3. Configure a Redirection
Script: 3-redirection

Set up an Nginx redirection from /redirect_me to another page using HTTP 301 (Moved Permanently).
Requirements:
Configure Nginx to perform a 301 redirect when visiting /redirect_me.
Use a Bash script to configure the server.

4. Custom 404 Page
Script: 4-not_found_page_404

Create a custom 404 page that displays "Ceci n'est pas une page" when visiting a non-existent page.
Requirements:
Configure Nginx to return a 404 error with the custom message.

5. Install Nginx with Puppet (Advanced)
File: 7-puppet_install_nginx_web_server.pp

Use Puppet to install and configure Nginx with the same requirements as in Task 1.

Additional Requirements:
Include a 301 redirect for /redirect_me.
Ensure the server is listening on port 80 and returns the "Hello World!" message.
