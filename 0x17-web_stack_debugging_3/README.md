# Web Stack Debugging #3

## Overview
This project focuses on debugging a web stack using `strace` to diagnose and fix a 500 Internal Server Error caused by Apache. The issue is resolved and automated using Puppet.

## Requirements
### General
- All files will be interpreted on **Ubuntu 14.04 LTS**.
- All files should end with a new line.
- A `README.md` file at the root of the project folder is mandatory.
- Puppet manifests must pass `puppet-lint` version **2.1.1** without any errors.
- Puppet manifests must run without errors.
- The first line of each Puppet manifest must be a comment explaining what it does.
- Puppet manifest files must end with the `.pp` extension.
- Files will be checked with **Puppet v3.4**.

### Install `puppet-lint`
To ensure compliance, install `puppet-lint` using the following commands:
```bash
apt-get install -y ruby
gem install puppet-lint -v 2.1.1
```

## Tasks
### 0. Strace is your friend
#### Mandatory Task
Using `strace`, diagnose why Apache is returning a `500 Internal Server Error`. Once the root cause is identified, implement a fix using **Puppet** instead of manually applying a Bash script.

#### Helpful Hints
- `strace` can attach to a running process to observe system calls.
- `tmux` can be used to run `strace` in one window and `curl` in another for debugging.

### Puppet Implementation
- The `0-strace_is_your_friend.pp` file must contain valid Puppet code.
- Any appropriate Puppet resource type may be used to fix the issue.

#### Example Output
Before applying the fix:
```bash
curl -sI 127.0.0.1
HTTP/1.0 500 Internal Server Error
```
After applying Puppet fix:
```bash
puppet apply 0-strace_is_your_friend.pp
curl -sI 127.0.0.1:80
HTTP/1.1 200 OK
```

### Repository
- **GitHub Repository:** `alx-system_engineering-devops`
- **Directory:** `0x17-web_stack_debugging_3`
- **File:** `0-strace_is_your_friend.pp`

---
By following these steps, you will successfully debug and automate the fix for Apache's `500 Internal Server Error` using Puppet.


