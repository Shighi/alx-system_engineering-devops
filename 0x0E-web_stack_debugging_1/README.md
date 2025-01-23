# Web Stack Debugging 1

This repository contains Bash scripts to fix common issues with web servers, specifically Nginx, in a Docker container.

## Tasks

### 0. Nginx likes port 80
In this task, we identify and fix the issue preventing Nginx from listening on port 80. The script automates the necessary steps to get Nginx running on the expected port.

### 1. Make it sweet and short
This task refines the previous script to make it shorter (5 lines or less) while ensuring it fixes the issue effectively.

## Requirements
- All scripts are written in Bash.
- The scripts must be executable and pass Shellcheck without errors.
- The server should be running Nginx and listening on port 80.
- The scripts should meet the specified guidelines without using certain commands like `wget`, `;`, or `&&`.

## How to Run
1. Clone the repository.
2. Navigate to the appropriate directory.
3. Run the scripts:
    ```bash
    ./0-nginx_likes_port_80
    ./1-debugging_made_short
    ```

## Author
Daisy Mwambi

