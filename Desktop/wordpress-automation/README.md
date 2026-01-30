# 🚀 Automated WordPress Infrastructure (LAMP Stack)

![DigitalOcean Ansible Tutorial Banner](https://raw.githubusercontent.com/ansible/logos/master/logos-png/ansible-logo-600px.png)

## 🎯 Project Overview

This project demonstrates **Infrastructure as Code (IaC)** by automating the deployment of a complete WordPress environment on a Linux VM using **Ansible Roles**.  

Inspired by DigitalOcean’s Ansible WordPress LAMP tutorial. :contentReference[oaicite:2]{index=2}

---

## 🏗️ Architecture (LAMP)

This setup uses a classic **LAMP stack**:

- **L**inux: Target Virtual Machine (Ubuntu)
- **A**pache: Web Server
- **M**ariaDB/MySQL: Database
- **P**HP: Backend language for WordPress

---

## 📁 Directory Structure

```text
.
├── inventory.ini         # Target VM details
├── playbook.yml          # Main playbook
└── roles/
    └── wordpress/        # Modular WordPress role
        ├── tasks/        # Installation + configuration
        ├── handlers/     # Service restarts
        ├── templates/    # Jinja2 configuration templates
        └── vars/         # Role variables
```

🛠️ How to Use
1. Configure

Edit inventory.ini with your target VM’s SSH and host details.

2. Run Playbook
```
ansible-playbook -i inventory.ini playbook.yml
```


4. Verify

Open your browser and visit:
```
http://<your-vm-ip>
```

