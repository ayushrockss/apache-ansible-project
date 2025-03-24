# Apache Web Server Setup using Ansible

This is a beginner DevOps project to install and configure an Apache Web Server on a target EC2 instance using Ansible automation.

## 🔧 Tools Used:
- AWS EC2
- Ubuntu Server
- Ansible
- Linux & Shell
- Git & GitHub

## 📂 Project Files:
- `inventory.ini`: Ansible inventory file
- `playbook.yml`: Ansible playbook to install Apache and deploy custom HTML
- `index.html`: Custom web page served via Apache
- `.gitignore`: To avoid pushing sensitive files

## 💡 How it works:
1. Ansible control node connects to target server using SSH.
2. Apache web server is installed via Ansible.
3. Custom `index.html` is deployed.
4. Access your webpage using public IP of the target server.

---

### 🚫 Note:
- Private IPs and `.pem` keys are not shared here for security reasons.

