# linux-web-server-deployment
**A complete, hands-on implementation of a LAMP stack (Linux, Apache, MySQL, PHP) with WordPress, demonstrating production-grade system administration and troubleshooting skills.**
---
## Table of Contents

- [Project Overview](#project-overview)
- [System Architecture](#system-architecture)
- [Technologies Used](#technologies-used)
- [Project Outcomes](#project-outcomes)
- [Installation & Setup](#installation--setup)
- [Key Learnings](#key-learnings)
- [Screenshots](#screenshots)
- [Relevant to SFU FCAT Role](#relevant-to-sfu-fcat-role)

## Project Overview

- What I Built
A fully functional LAMP stack running on Ubuntu Server in VirtualBox, with WordPress content management system installed and operational.

- Skills Demonstrated

  - Linux system administration (users, permissions, services)
  - Web server configuration (Apache)
  - Database design and management (MySQL)
  - Server-side scripting (PHP)
  - Application deployment (WordPress)
  - Systematic troubleshooting and debugging




## System Architecture

```text
┌──────────────────────────────────────────────────────────────┐
│                     MacBook Host (macOS)                     │
│──────────────────────────────────────────────────────────────│
│                                                              │
│  • Terminal (SSH Client)                                     │
│                                                              │
│                                                              │
└──────────────────────────────┬───────────────────────────────┘
                               │
                       SSH (Port 22)
                               │
                               ▼
┌──────────────────────────────────────────────────────────────┐
│            VMware Fusion Pro Virtualization Layer            │
│──────────────────────────────────────────────────────────────│
│  Virtual Network Adapter (NAT / Bridged Mode)                │
│                                                              │
│  Routes traffic from macOS → VM                              │
└──────────────────────────────┬───────────────────────────────┘
                               │
                               ▼
┌──────────────────────────────────────────────────────────────┐
│                 Ubuntu Server 26.04 (VM)                     │
│──────────────────────────────────────────────────────────────│
│                                                              │
│  ┌────────────────────────────────────────────────────────┐  │
│  │                 OpenSSH Server                         │  │
│  │────────────────────────────────────────────────────────│  │
│  │                                                        │  │
│  │  • Listening on Port 22                                │  │
│  │  • Handles SSH authentication                          │  │
│  │  • Remote shell access                                 │  │
│  │                                                        │  │
│  └────────────────────────────────────────────────────────┘  │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

---

## Technologies Used

### Operating System
- **Ubuntu Server 26.04 LTS** - Professional Linux distribution

### Web Server
- TBD

### Database
- TBD

### Server-Side Language
- TBD

### Database Administration
- TBD

### Content Management System
- TBD

### Infrastructure
- **VMware Fusion Professional 25H2** - Virtualization platform
- **systemd** - Service management
- **SSH** - Remote terminal access

### Linux Administration Skills
- User and group management
- File permissions (chmod, chown)
- Service management (systemctl)
- Package management (apt)

---

## Project Outcomes

By completing this project, I can confidently:

### ✅ System Administration
- [x] Install and configure Ubuntu Server from scratch
- [x] Manage Linux users, groups, and permissions
- [x] Control services with systemctl
- [x] Manage packages with apt package manager
- [x] Understand boot processes and service dependencies

### ✅ Web Server Administration
- [ ] Install and configure Apache web server
- [ ] Create virtual hosts (multiple websites on one server)
- [ ] Enable and disable Apache modules
- [ ] Understand HTTP and port concepts
- [ ] Configure document root and file serving
- [ ] Read and interpret Apache logs

### ✅ Database Administration
- [ ] Install and secure MySQL database
- [ ] Create databases and users
- [ ] Manage user privileges and access control
- [ ] Back up and restore databases
- [ ] Use phpMyAdmin for database management

### ✅ Application Deployment
- [ ] Deploy PHP applications
- [ ] Configure PHP-MySQL integration
- [ ] Install and configure WordPress
- [ ] Manage WordPress users and content
- [ ] Understand application-server-database architecture

### ✅ Troubleshooting & Debugging
- [ ] Systematically diagnose service failures
- [ ] Interpret system logs (Apache, MySQL, systemd)
- [ ] Resolve permission and connectivity issues
- [ ] Recover from configuration mistakes
- [ ] Test and validate fixes

### ✅ Infrastructure Concepts
- [x] Understand virtualization (VMware)
- [x] Configure networking (IP addresses, ports, SSH)
- [ ] Understand DNS basics
- [ ] Implement security best practices
- [ ] Document infrastructure professionally

---

## Installation & Setup

### Prerequisites
- VMware Fusion Professional 25H2 installed on your machine
- Ubuntu Server 26.04 LTS ISO (~4.5 GB)
- 50+ GB free disk space
- 8+ GB RAM (4+ GB for VM)
- Stable internet connection

### Quick Start

**1. Create Virtual Machine in VirtualBox**
```bash
# Name: Ubuntu 64-bit Arm Server 26.04
# RAM: 4096 MB
# Disk: 20 GB (dynamic)
# CPU: 4 cores
```

**2. Install Ubuntu Server**
- Attach Ubuntu ISO to VM
- Install with default settings
- Create user: `q`
- Enable OpenSSH during installation

**3. Enable SSH Access**
```bash
sudo apt update
sudo apt install openssh-server -y
sudo systemctl start ssh
sudo systemctl enable ssh
ip addr show 
```

**4. Connect from Host Machine**
```bash
ssh admin@192.168.220.131
```


---

## Key Learnings

### System Administration
✅ Linux OS installation and configuration  
✅ User and permission management  
✅ Service management with systemd  
✅ Package management with apt  
✅ Understanding boot processes  

### Real-World Skills
✅ Documentation and knowledge transfer  
✅ Professional communication  
✅ Problem-solving under constraints  
✅ Learning independently from errors  
✅ Translating concepts to practice  

---

## Screenshots

### 1. VirtualBox VM Running
![VM Running](screenshots/01-vm-running.png)
*Ubuntu Server 26.04 LTS running in VMware with 4GB RAM*

### 2. Terminal Commands
![Terminal](screenshots/07-terminal-commands.png)
*MacOS terminal showing key administrative commands*

---

## Relevant to SFU FCAT Role

This project directly addresses the **SFU FCAT Research Assistant** job requirements:

| Requirement | Demonstrated |
|------------|--------------|
| Linux VM/Web Server Setup | ✅ Complete from scratch |
| Documentation | ✅ Comprehensive guides included |

**This project demonstrates I can:**
- Work independently on complex systems
- Learn new technologies quickly
- Document work professionally
- Troubleshoot multi-component systems
- Support faculty/research computing needs

---

## What I'd Do Differently in Production

This project is a learning foundation. For production systems, I would:

- [ ] Containerize with Docker for isolation and scalability
- [ ] Implement load balancing for redundancy
- [ ] Use managed databases (AWS RDS) to reduce ops burden
- [ ] Enable SSL/TLS (HTTPS) with Let's Encrypt
- [ ] Implement automated backups (encrypted, off-site)
- [ ] Set up monitoring and alerting (Prometheus, Grafana)
- [ ] Use Infrastructure as Code (Terraform, Ansible)
- [ ] Implement CI/CD pipeline (GitHub Actions)
- [ ] Database replication for disaster recovery
- [ ] Implement comprehensive security scanning

---

## Resources Used

### Documentation
- [Ubuntu Server Guide](https://ubuntu.com/server/docs)
- [Apache HTTP Server Documentation](https://httpd.apache.org/docs/2.4/)
- [MySQL Official Documentation](https://dev.mysql.com/doc/)
- [PHP Official Documentation](https://www.php.net/docs.php)
- [WordPress Developer Documentation](https://developer.wordpress.org/)
- [DigitalOcean Community Tutorials](https://www.digitalocean.com/community/tutorials)

### Learning Resources
- Boot.dev Linux CLI Course
- Learn Linux TV (YouTube)
- tutoriaLinux (YouTube)
- DigitalOcean LAMP Stack Guides

---

## License

This project is for educational purposes. Free to fork and modify for learning.

---

## About This Project

**Project Duration:** 2/10 days  
**Created:** May 2026  
**Last Updated:** May 2026  
**Status:** in progress

---

## Questions or Feedback?

This project demonstrates my ability to:
- Learn independently
- Document thoroughly  
- Troubleshoot systematically
- Communicate technically
  
---

**[Back to top](#linux-web-server-deployment-project)**

