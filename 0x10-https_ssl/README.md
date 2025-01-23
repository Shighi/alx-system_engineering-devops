 and SSL Termination

## Description
This project focuses on configuring subdomains, enabling SSL termination with HAProxy, and enforcing HTTPS traffic.

## Requirements
- Ubuntu 16.04 LTS
- Bash scripts must be executable and pass **Shellcheck** (version 0.3.7).
- HAProxy version 1.5+.
- A `README.md` file is mandatory.

## Tasks
### 0. World Wide Web
- Configure subdomains (`www`, `lb-01`, `web-01`, `web-02`) to point to respective IPs.
- Write a Bash script (`0-world_wide_web`) to audit subdomains.
- Must use `awk` and a Bash function.

### 1. HAProxy SSL Termination
- Configure HAProxy to handle SSL traffic on port 443.
- Serve encrypted traffic for the `www` subdomain.
- The root page must display "ALX".
- Configuration file: `1-haproxy_ssl_termination`.

### 2. Enforce HTTPS
- Redirect all HTTP traffic to HTTPS with a 301 status code.
- Configuration file: `100-redirect_http_to_https`.

## Usage
Run the scripts and test HAProxy configurations using tools like `dig`, `curl`, and `openssl`.

## Author
Daisy Mwambi


