1.SSH Configuration and Management
This project contains Bash scripts and configuration files for SSH connection management. The tasks focus on setting up secure SSH access, including:

Creating and using SSH key pairs
Configuring SSH client settings
Managing server access with public keys
Using Puppet for SSH configuration automation

Files

0-use_a_private_key: Script to connect to server using private key
1-create_ssh_key_pair: Script to create RSA key pair
2-ssh_config: SSH client configuration file
100-puppet_ssh_config.pp: Puppet manifest for SSH client configuration

Environment

Ubuntu LTS
Bash scripting
OpenSSH
Puppet (for advanced task)

Requirements

Private key location: ~/.ssh/school
Key bits: 4096
Default user: ubuntu
