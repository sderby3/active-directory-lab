# Windows Server Active Directory Homelab

## Overview
This project documents the creation of a Windows Server 2022 Active Directory homelab environment built using VirtualBox.

The purpose of the lab was to develop hands-on infrastructure, networking and systems administration skills commonly used in enterprise IT environments.

---

## Technologies Used
- VirtualBox
- Windows Server 2022
- Windows 11 Pro
- Active Directory Domain Services
- DNS
- Group Policy
- Virtual Networking
- Jira

---

## Lab Configuration

### Domain Controller
- Hostname: DC01
- Domain: homelab.local
- Services:
  - Active Directory
  - DNS

### Client Machine
- Windows 11 Pro
- Joined to Active Directory domain

### Network Configuration
- Internal VirtualBox network
- Static IP addressing

<img src="Network settings.png" width="700">

### Server IP
192.168.100.1

<img src="Server_IPConfig.png" width="700">

### Client IP
192.168.100.10

<img src="Wind11Client_IPConfig.png" width="700">

### Connectivity Test

<img src="Ping_and_Replies.png" width="700">

---

## Features Implemented

### Active Directory Domain Setup

<img src="Deployment Config.png" width="700">

### Organisational Units (HR, IT, Sales)

<img src="Organisational_units.png" width="700">

### User Account Creation

<img src="Users_Grouped.png" width="700">

### Security Groups

<img src="IT_Users.png" width="700">

### Windows Client Domain Join

<img src="Welcome_to_domain.png" width="700">

<img src="Login_success.png" width="700">

---

## Group Policy Configuration

### Company Wallpaper Policy
Configured a Group Policy Object (GPO) to automatically deploy a desktop wallpaper to domain users.

<img src="Wallpaper_Policy.png" width="700">

<img src="Wallpaper_ineffect.png" width="700">

### Disable Control Panel Policy
Configured a Group Policy Object to restrict access to Control Panel and Windows Settings.

<img src="ProhibitControlPanelAccess.png" width="700">

<img src="ControlPanelLocked.png" width="700">

---

## Troubleshooting & Issues Encountered

### Domain Controller Promotion Failure

#### Issue
Prerequisite checks failed due to pending hostname change requiring reboot.

<img src="Prerequisites Failed.png" width="700">

#### Resolution
Restarted the server VM and reran the Domain Controller promotion process successfully.

<img src="Prerequisites passed.png" width="700">

---

### Windows 11 Home Limitation

#### Issue
Windows 11 Home edition could not join the Active Directory domain.

#### Resolution
Reinstalled client VM using Windows 11 Pro edition.

---

### VM Networking Issues

#### Issue
Client machine could not communicate with Domain Controller.

#### Resolution
Configured both VMs on the same Internal Network in VirtualBox and assigned static IP addresses.

---

### Windows 11 Microsoft Account Requirement

#### Issue
Windows 11 setup required internet and Microsoft account sign-in.

#### Resolution
Used OOBE bypass methods to complete offline local account setup.

<img src="Bypass_no_network_cmd.png" width="700">

---

## Jira IT Support Workflow Simulation

Used Jira Service Management to simulate IT support workflows and issue tracking for the Active Directory homelab environment.

Created and managed tickets related to:
- Active Directory deployment
- DNS troubleshooting
- Group Policy issues
- Domain join failures
- Virtual network connectivity

Practised ticket lifecycle management using:
- To Do
- In Progress
- Done

Included troubleshooting notes, priorities, and documented resolutions to simulate real-world IT support operations.

<img src="jira_board.png" width="700">
<img src="Ticket_Comments.png" width="700">

---

## Skills Developed
- Windows Server administration
- Active Directory management
- DNS configuration
- Virtualisation
- Networking fundamentals
- Group Policy administration
- Troubleshooting and problem solving
- Infrastructure documentation
