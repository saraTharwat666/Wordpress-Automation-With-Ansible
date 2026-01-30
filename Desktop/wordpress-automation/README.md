# 🚀 Automated WordPress Infrastructure (LAMP Stack)

![WordPress Project Banner](https://raw.githubusercontent.com/ansible/logos/master/logos-png/ansible-logo-600px.png)

## 🎯 Project Overview
This project demonstrates **Infrastructure as Code (IaC)** by automating the deployment of a complete WordPress environment on a Linux VM using **Ansible Roles**. 

## 🏗️ The Architecture (LAMP)
- **L**inux: Target Virtual Machine.
- **A**pache: Web Server.
- **M**ariaDB: Database for content storage.
- **P**HP: Scripting language for WordPress logic.

## 📁 Directory Structure
```text
.
├── inventory.ini        # Target VM details
├── playbook.yml         # Main entry point
└── roles/
    └── wordpress/       # Modular WordPress role
        ├── tasks/       # Installation & Configuration steps
        ├── handlers/    # Service restart logic
        ├── templates/   # Jinja2 wp-config template
        └── vars/        # Sensitive & common variables
```

🚀 How to Use
Configure: Update inventory.ini with your VM details.

Execute: Run the following command:
```
Bash
ansible-playbook -i inventory.ini playbook.yml
Verify: Access http://<your-vm-ip> in your browser.
```
