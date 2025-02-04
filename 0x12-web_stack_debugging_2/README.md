# Web Stack Debugging #2

## Overview
This project focuses on debugging and securing web stack configurations, particularly working with user permissions and Nginx configurations in Ubuntu 20.04 LTS. The tasks involve running processes as non-root users and configuring Nginx to run with limited privileges.

## Project Requirements
- All files interpreted on Ubuntu 20.04 LTS
- Files must end with a new line
- All Bash script files must be executable
- Scripts must pass Shellcheck without any error
- First line of all Bash scripts: `#!/usr/bin/env bash`
- Second line of all Bash scripts: Comment explaining script functionality

## Tasks

### 0. Run Software as Another User
**File:** `0-iamsomeoneelse`
- Script that accepts one argument
- Runs the `whoami` command under the user passed as argument
- Demonstrates the ability to run commands as different users

Example usage:
```bash
./0-iamsomeoneelse www-data
```

### 1. Run Nginx as Nginx
**File:** `1-run_nginx_as_nginx`
- Configures Nginx to run as the `nginx` user
- Ensures Nginx is listening on all active IPs on port 8080
- Improves security by avoiding root user privileges
- Cannot use `apt-get remove`

### 2. 7 Lines or Less (Advanced)
**File:** `100-fix_in_7_lines_or_less`
- Short version of task #1
- Script must be 7 lines or less
- Must include a new line at end of file
- Cannot use `;`, `&&`, or `wget`
- Cannot execute the previous answer file

## Testing
Scripts can be tested using the following commands:
```bash
# Task 0
./0-iamsomeoneelse www-data

# Task 1 & 2
ps auxff | grep nginx    # Verify nginx user
nc -z 0 8080            # Check port 8080
```

## Security Note
Running web servers as root is a security risk. This project demonstrates best practices by:
- Running processes as non-root users
- Configuring services with minimum required privileges
- Implementing security-focused configurations

## Repository
- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x12-web_stack_debugging_2`
