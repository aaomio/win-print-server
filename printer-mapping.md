# Printer Mapping (CLIENT-01)

This file covers how domain users connect to shared printers hosted on PS-01.

Printers are accessed via SMB share:
- \\PS-01

---

## 1. Verify Network Access

From CLIENT-01:

- Press **Win+R**
- Enter:
  - \\PS-01

Confirm visibility of:
- FollowMe_Colour
- FollowMe_Mono

---

## 2. Manual Printer Mapping

### Method 1 (Run command)

- Press **Win+R**
- Enter:
  - \\PS-01

Then:
- Double-click:
  - FollowMe_Colour
  - FollowMe_Mono

---

### Method 2 (Control Panel)

- Press **Win+R**
- Enter:
  - control 
- Click: 
  - View devices and printers 

Then:

- Click **Add Printer**
- Select:
  - The printer that I want isn't listed
- Choose:
  - Select a shared printer by name

Enter:

- \\PS-01\FollowMe_Colour  
- \\PS-01\FollowMe_Mono  

---

## Result

Printers are mapped from PS-01 using SMB sharing, allowing domain users to install FollowMe queues directly without manual driver installation.