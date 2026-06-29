# Print Management Setup (PS-01)

This file covers setup of the Windows Print Server role and Print Management console.

---

## 1. Install Print Server Role

On PS-01:
- Press **Win+R**
- Enter:
  - `servermanager`
- Click **Add Roles and Features**
- Select:
  - Role-based installation
- Choose PS-01

Enable:
- Print Server role service

Complete installation and restart if required.

---

## 2. Open Print Management

Launch:

- `printmanagement.msc`

Verify:

- Print Server \\\PS-01 is visible

---

## 3. Verify Printer Network Configuration

Before adding printers:

### Print configuration page

Print a network/config page to confirm:

- IP address
- MAC address
- Network status

---

### Test connectivity

From PS-01:

- `ping X.X.X.X`

## 4. Install Printer Driver

- Download the official driver from the Epson support page for the printer model
- Run the downloaded `.exe` installer on PS-01
- Allow the installer to extract and register the driver

After installation:

- Open `printmanagement.msc`
- Check under:
  - Print Servers\PS-01\Drivers
  - Printers

If it does not appear:

- Press **Win+R**
- Enter:
  - `services.msc`
- Locate **Print Spooler**
- Restart the service

After restart:

- Re-open `printmanagement.msc`
- Recheck the driver list under:
  - Print Servers\PS-01\Drivers