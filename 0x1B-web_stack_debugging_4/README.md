# Web Stack Debugging 4

## Overview
This project focuses on debugging a web stack configuration that uses Nginx as the web server. The goal is to optimize the server under heavy load and resolve user session limitations.

## Tasks

### 0. Sky is the Limit, Let's Bring That Limit Higher
**File:** `0-the_sky_is_the_limit_not.pp`

In this task, we analyze the performance of an Nginx web server under load using ApacheBench. The initial benchmark results show a high failure rate of 943 failed requests out of 2000. To fix this issue, we apply a Puppet script that optimizes the Nginx configuration, ensuring all requests are successfully processed.

#### Benchmark Before Fix:
```
Failed requests:        943
Non-2xx responses:      1057
```

#### Benchmark After Fix:
```
Failed requests:        0
Requests per second:    6650.99 [#/sec] (mean)
```

### 1. User Limit
**File:** `1-user_limit.pp`

This task resolves an issue where the `holberton` user cannot log in due to a "Too many open files" error. By modifying the OS configuration using a Puppet script, we increase the file descriptor limit, allowing the user to log in and execute commands without errors.

#### Issue Before Fix:
```
-su: /etc/profile: Too many open files
-su: start_pipeline: pgrp pipe: Too many open files
```

#### After Applying the Fix:
```
holberton@079b7269ec1b:~$ head /etc/passwd
```
(User is able to open files without errors.)

## Repository Structure
```
|-- 0x1B-web_stack_debugging_4/
    |-- 0-the_sky_is_the_limit_not.pp
    |-- 1-user_limit.pp
    |-- README.md
```

## Usage
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/alx-system_engineering-devops.git
   cd alx-system_engineering-devops/0x1B-web_stack_debugging_4
   ```
2. Apply the Puppet scripts:
   ```sh
   sudo puppet apply 0-the_sky_is_the_limit_not.pp
   sudo puppet apply 1-user_limit.pp
   ```

## Author
-SHIGHI

## License
This project is open-source and follows the ALX SE program guidelines.


