# Active Directory & Networking Home Lab

## Overview

This home lab was built to simulate a real-world enterprise IT environment using Windows Server, Active Directory, Group Policy, networking services, Linux, SSH, and PowerShell automation.

The lab focused on hands-on system administration, troubleshooting, identity management, infrastructure management, and automation tasks commonly performed in Help Desk, IT Support, and System Administrator roles.

---

# Technologies Used

- Windows Server
- Active Directory Domain Services (AD DS)
- Group Policy Management
- DNS & DHCP
- PowerShell
- Windows 11 Virtual Machines
- Ubuntu Server
- SSH
- NGINX
- VMware

---

# Active Directory Lab

## Domain Controller Deployment

- Installed and configured Active Directory Domain Services (AD DS)
- Promoted Windows Server to a Domain Controller
- Created and managed a custom domain environment
- Configured Organizational Units (OUs)
- Created and managed users and security groups

### Skills Practiced

- Active Directory administration
- User and group management
- Authentication management
- OU structure management
- Account lifecycle management

---

# Group Policy Administration

## Group Policy Configuration

Configured and tested multiple Group Policy Objects (GPOs) to simulate enterprise workstation management and security controls.

### Policies Implemented

- Desktop wallpaper policies
- Control Panel restrictions
- USB/device restrictions
- Password complexity policies
- Account lockout policies
- Drive mapping via GPO
- User vs Computer policies
- Loopback processing concepts

### Troubleshooting Tools

```powershell
gpresult /r
rsop.msc
```

### Skills Practiced

- GPO deployment
- Policy inheritance and precedence
- GPO troubleshooting
- Security policy management
- LSDOU processing

---

# Networking Services

## DNS & DHCP

Configured core networking services required for domain functionality.

### Tasks Completed

- Configured DNS for Active Directory name resolution
- Verified domain connectivity
- Installed and configured DHCP
- Created DHCP scopes
- Configured automatic IP assignment

### Skills Practiced

- DNS troubleshooting
- DHCP configuration
- Network connectivity testing
- Client/server communication

---

# File Server & Permissions

## Shared Resource Management

Built a file server environment with department-based access control.

### Tasks Completed

- Created shared folders
- Configured NTFS permissions
- Configured Share permissions
- Implemented department-based access restrictions
- Tested user access scenarios

### Skills Practiced

- File server administration
- Permission management
- Access control troubleshooting
- NTFS vs Share permissions

---

# PowerShell Automation

## Administrative Scripting

Used PowerShell to automate common administrative tasks.

### Tasks Completed

- Created users via PowerShell
- Automated bulk user creation
- Managed accounts through scripts
- Performed administrative automation tasks

### Example Commands

```powershell
New-ADUser
Add-ADGroupMember
Disable-ADAccount
```

### Skills Practiced

- PowerShell scripting
- Automation
- Bulk administration
- IT task automation

---

# Linux & SSH Home Lab

## Ubuntu Server Remote Administration

Built a Linux server environment and practiced remote administration using SSH.

### Tasks Completed

- Installed Ubuntu Server VM
- Installed and configured OpenSSH Server
- Verified SSH service status
- Connected remotely using SSH
- Managed Linux systems through CLI
- Installed NGINX web server

### Linux Commands Practiced

```bash
sudo apt update
sudo apt upgrade
sudo apt install openssh-server
sudo systemctl status ssh
ip a
ssh username@IP_ADDRESS
ls
cd
pwd
```

### Skills Practiced

- Linux administration
- SSH remote access
- Command-line navigation
- Package management
- Remote server management
- Networking troubleshooting

---

# Troubleshooting & Break/Fix Scenarios

## Simulated Real-World Issues

Created intentional failures to practice troubleshooting and problem resolution.

### Scenarios Included

- DNS misconfiguration
- GPO conflicts
- User permission issues
- Authentication failures
- Network connectivity problems
- Policy application failures

### Skills Practiced

- Root cause analysis
- Troubleshooting methodology
- DNS troubleshooting
- GPO debugging
- Permission troubleshooting

---

# Advanced Administration

## Enterprise-Level Concepts

Practiced advanced Active Directory administration concepts.

### Tasks Completed

- Configured secondary Domain Controller
- Tested AD replication
- Simulated backup & restore scenarios
- Delegated administrative permissions
- Configured audit policies and event logging

### Skills Practiced

- AD replication
- Backup & recovery
- Delegation
- Security auditing
- Enterprise administration

---

# Key Learning Outcomes

Through this home lab, I gained hands-on experience with:

- Active Directory administration
- Windows Server management
- Group Policy deployment and troubleshooting
- DNS & DHCP configuration
- File server management
- PowerShell automation
- Linux server administration
- SSH remote management
- IT troubleshooting methodologies
- Enterprise infrastructure management

---

# Future Improvements

Planned future additions to the lab include:

- Microsoft Azure integration
- SIEM monitoring
- VPN configuration
- Security hardening
- Docker & containerization
- Advanced PowerShell automation
- Backup monitoring solutions