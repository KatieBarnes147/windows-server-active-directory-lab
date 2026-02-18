# Windows Server Active Directory Lab

## Overview

This project simulates a small business network built from scratch using Windows Server and a domain-joined workstation.
The goal was to understand how organizations manage users, authentication, and file access using Active Directory.

Domain: **barnescorp.local**

---

## Technologies Used

* Windows Server 2022
* Active Directory Domain Services (AD DS)
* DNS
* NTFS Permissions
* Windows Client Workstation
* Oracle VirtualBox Networking

---

## Network Design

Departments created:

* HR
* IT
* Sales

Each department should only access its own files.

---

## 1. Server Installation

Windows Server was installed in a virtual environment.

![Server Install](screenshots/1-installation/4.png)

---

## 2. Domain Controller Promotion

The server was promoted to a Domain Controller and the Active Directory domain was created.

![Domain Created](screenshots/2-domain-controller/10.png)

---

## 3. Active Directory Configuration

Organizational Units, users, and security groups were created.

![Active Directory](screenshots/3-active-directory/11.png)

---

## 4. Client Domain Join

A workstation was joined to the domain and authenticated with domain credentials.

![Client Join](screenshots/4-client-join/12.png)

---

## 5. Access Control Testing

Shared folders were configured and tested using a Sales user account.

Sales user:

* Access allowed: Sales folder
* Access denied: HR and IT folders

![Access Test 1](screenshots/5-permissions/IMAGE2.png)
![Access Test 2](screenshots/5-permissions/IMAGE3.png)
![Access Test 3](screenshots/5-permissions/IMAGE4.png)
![Access Test 4](screenshots/5-permissions/IMAGE5.png)

---

## Troubleshooting Performed

* DNS configuration preventing domain join
* User authentication failures
* Network adapter connectivity in virtual network
* NTFS permission inheritance conflicts

---

## What I Learned

This lab demonstrated how authentication relies on DNS and how group membership controls authorization in enterprise environments.
It also reinforced troubleshooting workflow for real domain environments.

---

## Author

Katie Barnes
