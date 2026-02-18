# Active Directory Home Lab — Role Based Access Control

## Overview

In this project I built a small company network using Windows Server and a domain-joined workstation.
The goal was to simulate how businesses manage employee file access using Active Directory groups and NTFS permissions.

The environment enforces department-based access so users can only open folders that belong to their department.

---

## Environment

**Virtualization**

* Oracle VirtualBox

**Servers**

* Windows Server 2022 — Domain Controller (DC01)

**Client**

* Windows 10/11 Workstation (WS01)

**Domain**

* barnescorp.local

---

## Network Configuration

* Internal network: CorpNet
* Domain Controller IP: 192.168.10.10
* Workstation IP: 192.168.10.20
* DNS handled by Domain Controller

---

## Active Directory Structure

Organizational Units:

* IT
* HR
* Sales

Security Groups:

* IT_Staff
* HR_Staff
* Sales_Staff

Users were created and assigned to their department group.

---

## File Server Configuration

Shared folder:

```
\\DC01\CompanyData
```

Department folders:

* IT
* HR
* Sales

Permissions model:

Share Permissions:

* Everyone → Full Control (lab simplification)

NTFS Permissions:

* IT_Staff → Access to IT folder only
* HR_Staff → Access to HR folder only
* Sales_Staff → Access to Sales folder only
* Other departments → Access Denied

---

## Testing

A domain workstation was joined to the domain and users logged in to verify access control.

Example test:
User: msales

Results:

* Sales folder → Accessible
* IT folder → Access Denied
* HR folder → Access Denied

Screenshots included in repository.

---

## Skills Demonstrated

* Active Directory deployment
* Organizational Unit design
* Security group management
* Domain join configuration
* DNS troubleshooting
* NTFS permissions
* Share permissions
* Role Based Access Control (RBAC)
* Windows authentication testing
* Troubleshooting connectivity and login issues

---

## What I Learned

This lab helped me understand how authentication, DNS, and permissions interact in a real environment.
I also diagnosed issues related to domain discovery, group membership tokens, and network communication between client and server.

---

## Author

Katie Barnes
