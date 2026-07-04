# Linux Health Check Automation using Ansible Roles

## Project Overview

This project automates Linux server health checks using Ansible Roles. It collects health information from managed Linux servers and generates a health check report on the Ansible control node using a Jinja2 template. The playbook can also be scheduled using Cron for automatic execution.

## Features

- Collects Hostname
- Collects IP Address
- Collects System Uptime
- Collects Disk Usage
- Collects Memory Usage
- Collects CPU Information
- Collects Kernel Version
- Checks Nginx Service Status
- Displays Logged-in Users
- Displays Last Boot Time
- Generates Health Check Report using Jinja2 Template
- Uses Ansible Roles
- Supports Cron Scheduling

## Technologies Used

- Linux
- Ansible
- Jinja2
- Cron
- Git
- GitHub

## Project Structure

```
healthcheck-project/
├── inventory
├── site.yml
├── README.md
└── roles/
    └── healthcheck/
        ├── tasks/
        │   └── main.yml
        └── templates/
            └── report.j2
```

## How to Run

```bash
ansible-playbook -i inventory site.yml


## Cron Scheduling

```cron
0 8 * * * /usr/bin/ansible-playbook -i inventory site.yml


This schedules the playbook to run automatically every day at 8:00 AM.

## Author

Nimala H B

