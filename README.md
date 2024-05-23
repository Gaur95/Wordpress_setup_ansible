# WordPress Setup with Ansible

This project provides Ansible playbooks and configuration files to set up a WordPress site on an Ubuntu 22.04 server. The playbooks install and configure MySQL, Apache, PHP, and WordPress, including setting up the database and user for WordPress.

## Prerequisites

- Ansible installed on your control machine. If not installed, you can install it using pip:

```
  pip install ansible
```
# Setup Instructions
## Clone the Repository
```
git clone  https://github.com/Gaur95/Wordpress_setup_ansible.git
cd Wordpress_setup_ansibl
```
## Update Inventory File
+ Edit the **hosts** file to include your target host: path- /etc/ansible/hosts 
```
[web]
your_target_host ansible_user=your_user
```
## Update Variables
+ Edit the **var.yaml** file to set your MySQL root password, WordPress database name, user, and password:
```
mysql_root_password: "your_root_password_here"
wp_db_name: "wordpress"
wp_db_user: "wp_user"
wp_db_password: "your_wp_password_here"
```
## Run the Playbook
```
ansible-playbook wordpress.yaml
```
