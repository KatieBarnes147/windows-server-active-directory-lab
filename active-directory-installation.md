# Active Directory Installation and Domain Setup

## Objective

Deploy a Windows Server Domain Controller to provide centralized authentication and management for a small business network.

---

## Server Preparation

Installed Windows Server and configured:

* Static IP address
* Computer name: DC01
* Verified network connectivity between server and workstation

Reason: Domain controllers must maintain consistent network identity to prevent authentication failures.

---

## Active Directory Domain Services Installation

Installed Active Directory Domain Services role using Server Manager.

After installation, promoted the server to a domain controller.

Domain created:
BarnesCorp.local

Reason: Internal domain namespace prevents external DNS conflicts and mirrors real enterprise environments.

---

## DNS Configuration

DNS role installed automatically during domain promotion.

Verified:

* Forward lookup zone created
* Server resolves domain clients
* Client can locate domain controller

Result: Workstation successfully discovered domain services.

---

## Validation

Tested by joining workstation WS01 to domain.

Successful domain login confirmed centralized authentication functioning.

---

## Outcome

A functional Active Directory environment capable of managing users, devices, and security policies was successfully deployed.
