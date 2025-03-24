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
- Allow HTTP(80) and SSH(22) ports in security group

### Step 2: Setup SSH Key Authentication
- Generate SSH Key: `ssh-keygen`
- Copy key using `ssh-copy-id` or manually paste public key in target server's `~/.ssh/authorized_keys`

### Step 3: Clone this Repo
```bash
git clone https://github.com/ayushrockss/apache-ansible-project.git
cd apache-ansible-project
```

### Step 4: Edit inventory.ini
```ini
[targetserver]
<PRIVATE_IP_OF_TARGET_SERVER> ansible_user=ubuntu
```
🔸 Replace `<PRIVATE_IP_OF_TARGET_SERVER>` with the private IP address of your target EC2 server.  
👉 This private IP is used by Ansible to connect to the target server.

### Step 5: Run Playbook
```bash
ansible-playbook -i inventory.ini playbook.yml
```

### Step 6: Access the Website
Open your **target server’s public IP address** in a web browser:
```
http://<PUBLIC_IP_OF_TARGET_SERVER>
```

## index.html Example
```html
<!DOCTYPE html>
<html>
<head><title>My First DevOps Project</title></head>
<body><h1>Hello from Apache Web Server - Automated using Ansible!</h1></body>
</html>
```

## Notes
- Do **not** upload `.pem` files or your real IP addresses to GitHub.
- `.gitignore` is already added to ignore private keys and sensitive files.
