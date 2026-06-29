# Windows Print Server and Print Services

Building on https://github.com/aaomio/win-server-AD

This lab extends a Windows Server Active Directory environment by adding a print server and shared network printing using VMware Workstation.

Focus is on setting up a print server, creating shared printers, and managing print queues within a domain.

---

## Printer Setup

Before configuring the print server, connect the physical printer to the network.

* Connect an Ethernet cable from the printer to a switch access port configured for printer devices.
* Ensure the switch port is active and connected to the correct VLAN.
* Verify the printer is configured to obtain an IP address automatically (DHCP).
* Print the printer's network configuration page to confirm:

  * IP address
  * Subnet mask
  * Default gateway
  * MAC address
* From PS-01, verify connectivity by running:

---

## Lab Workflow

Follow steps in order.

---

## Base Active Directory Setup

Follow the base lab here:
- [win-server-AD](https://github.com/aaomio/win-server-AD)

Includes:
- Domain Controller (DC-01)
- DNS configuration
- Domain creation (`matrix.local`)
- Domain join for CLIENT-01

---


## Print Server Setup

- [print-server-setup](./print-server-setup.md)

Includes:
- Install Print and Document Services on PS-01
- Add network printer via TCP/IP (192.168.1.128)
- Install Epson XP-3200 driver
- Configure shared printer on domain network

---

## FollowMe Printers

- [followme](./followme.md)

Includes:
- Create `FollowMe_Colour`
- Create `FollowMe_Mono`
- Configure colour and grayscale policies on same physical printer

---

## Printer Mapping

- [printer-mapping](./printer-mapping.md)

Includes:
- Connect CLIENT-01 to `\\PS-01`
- Map shared printers via SMB
- Auto-install drivers via print server
- Validate domain authentication access

---

## Queue & Spooler Management

- [queue-spooler](./queue-spooler.md)

Includes:
- Clear stuck print jobs
- Restart Print Spooler service
- Resolve queue issues

---

## Summary

This lab demonstrates:
- Centralised print server management
- Colour vs mono queue separation
- Domain-based printer deployment