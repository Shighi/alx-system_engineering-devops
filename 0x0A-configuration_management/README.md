# Configuration Management Project

## Background Context

This project is inspired by a real-world incident at SlideShare where an auto-remediation tool called Skynet had a bug that accidentally terminated 75% of the document conversion infrastructure. Thanks to configuration management with Puppet, the infrastructure was restored to normal operation in under 1 hour, demonstrating the importance of automated configuration management in modern infrastructure.

## Project Description

This project contains Puppet manifests for basic system configuration management tasks. It serves as an introduction to using Puppet for infrastructure automation.

## Requirements

### Environment
- Ubuntu 20.04 LTS
- Puppet 5.5 (pre-installed)
- puppet-lint 2.1.1

### Installation Requirements
```bash
# Install Ruby and dependencies
apt-get install -y ruby=1:2.7+1 --allow-downgrades
apt-get install -y ruby-augeas
apt-get install -y ruby-shadow
apt-get install -y puppet

# Install puppet-lint
gem install puppet-lint
```

### General Requirements
- All files must end with a new line
- All Puppet manifests must pass puppet-lint version 2.1.1 without errors
- All Puppet manifests must run without error
- All Puppet manifests' first line must be a comment explaining the manifest's purpose
- All Puppet manifest files must end with the extension .pp

## Tasks

### 0. Create a file
- **File:** `0-create_a_file.pp`
- Creates a file in `/tmp` with specific requirements:
  - Path: `/tmp/school`
  - Permission: 0744
  - Owner: www-data
  - Group: www-data
  - Content: "I love Puppet"

### 1. Install a package
- **File:** `1-install_a_package.pp`
- Installs Flask from pip3
- Requirements:
  - Version must be 2.1.0

### 2. Execute a command
- **File:** `2-execute_a_command.pp`
- Creates a manifest that kills a process named killmenow
- Requirements:
  - Must use the exec Puppet resource
  - Must use pkill

## Repository Information

- **GitHub repository:** alx-system_engineering-devops
- **Directory:** 0x0A-configuration_management

## Resources

- [Introduction to Configuration Management](https://www.digitalocean.com/community/tutorials/an-introduction-to-configuration-management)
- [Puppet resource type: file](https://puppet.com/docs/puppet/5.5/types/file.html)
- [Puppet's Declarative Language: Modeling Instead of Scripting](https://puppet.com/blog/puppet-declarative-language-modeling-instead-of-scripting/)
- [Puppet lint](http://puppet-lint.com/)
- [Puppet emacs mode](https://github.com/voxpupuli/puppet-mode)
