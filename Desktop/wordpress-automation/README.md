# 🚀 Automated WordPress Infrastructure (LAMP Stack)

## 🎯 Overview
This project demonstrates the power of **Infrastructure as Code (IaC)** by automating the deployment of a complete WordPress environment on a Linux VM using **Ansible Roles**. Instead of manual configuration, a single command sets up the entire web stack.

## 🏗️ Architecture (LAMP Stack)
- **L**inux: Target Virtual Machine (CentOS/Ubuntu).
- **A**pache: High-performance HTTP Server.
- **M**ariaDB: Reliable relational database for content storage.
- **P**HP: Server-side scripting for dynamic content.

## 📁 Project Structure
- `inventory.ini`: Contains VM connection details.
- `playbook.yml`: The main entry point that calls the WordPress role.
- `roles/wordpress/`: Contains all logic:
    - `tasks/`: Installation steps for Apache, MySQL, PHP, and WordPress.
    - `templates/`: Dynamic `wp-config.php` file using Jinja2.
    - `handlers/`: Automates service restarts.

## 🚀 Usage
1. Update `inventory.ini` with your VM's IP address and SSH credentials.
2. Run the playbook:
   ```bash
   ansible-playbook -i inventory.ini playbook.yml