# Windows Server Active Directory + Print Lab (VMware)

Building on https://github.com/aaomio/win-server-AD

This lab extends a Windows Server Active Directory environment by adding a print server and shared network printing using VMware Workstation.

Focus is on setting up a print server, creating shared printers, and managing print queues within a domain.

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
- Install Print and Document Services on PS-01
- Add network printer via TCP/IP (192.168.1.128)
- Install Epson XP-3200 driver
- Share printer over domain network

---

## FollowMe Printers

- [followme](./followme.md)
- Create `FollowMe_Colour`
- Create `FollowMe_Mono`
- Configure both queues on same physical printer

---

## Printer Mapping

- [mapping](./printer-mapping.md)
- Connect CLIENT-01 to `\\PS-01`
- Auto-install shared printers
- Validate domain authentication access

---

## Queue & Spooler Management

- [queue-spooler](./queue-spooler.md)
- Clear print queues
- Restart Print Spooler service
- Troubleshoot stuck jobs

---

## Summary

This lab demonstrates:
- Shared printer management
- Colour vs mono queue separation
- Client printer deployment via domain