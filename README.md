# Apache Web Server Setup using Ansible

This is a beginner-friendly DevOps project that automates the installation and configuration of an Apache Web Server on a remote EC2 instance using Ansible.

## Tools & Technologies Used
- AWS EC2
- Ubuntu Server
- Ansible
- Linux & Shell Scripting
- Git & GitHub

## Project Files
- inventory.ini
- playbook.yml
- index.html
- .gitignore
- README.md

## What This Project Does
- Installs Apache2 on a remote EC2 server
- Deploys a custom webpage
- Starts and enables Apache service using Ansible

## Setup Instructions
### Step 1: Launch EC2 Instances
- One control node and one target server (Ubuntu)
- Allow HTTP(80) and SSH(22) ports

### Step 2: Setup SSH Key Authentication
- Generate SSH Key: ssh-keygen
- Copy key: ssh-copy-id or manually paste in ~/.ssh/authorized_keys

### Step 3: Clone this Repo
git clone https://github.com/your-username/apache-ansible-project.git

### Step 4: Edit inventory.ini
Replace 'your_target_server_ip' with actual IP

### Step 5: Run Playbook
ansible-playbook -i inventory.ini playbook.yml

### Step 6: Open your Public IP in browser

## index.html Example
<!DOCTYPE html>
<html>
<head><title>My First DevOps Project</title></head>
<body><h1>Hello from Apache Web Server - Automated using Ansible!</h1></body>
</html>

## Notes
- Don't upload .pem or IPs to GitHub
- Use .gitignore to protect private files

