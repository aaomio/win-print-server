# Print Management Setup (PS-01)

This file covers setup of the Windows Print Server role and Print Management console.

---

## 1. Configure Network Settings

Open Network Connections:

```text
Win + R
ncpa.cpl
```

Configure IPv4 settings:

```text
IP Address:      192.168.178.20
Subnet Mask:     255.255.255.0
Default Gateway: 192.168.178.2
DNS Server:      192.168.178.199
```

---

## 2. Configure Computer Name

Open System Properties:

```text
Win + R
sysdm.cpl
```

Rename the server:

```text
FS-01
```

Restart the system if prompted.

---

## 3. Join the Domain

Open System Properties:

```text
sysdm.cpl
```

Join the domain:

```text
matrix.local
```

Authenticate using:

```text
matrix\Administrator
```

Restart the server after the domain join completes.

---

## 4. Install Print Server Role

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

## 5. Open Print Management

Launch:

- `printmanagement.msc`

Verify:

- Print Server\PS-01 is visible

---

## 6. Verify Printer Network Configuration

Before adding printers:

### Print configuration page

Print a network/config page to confirm:

- IP address
- MAC address
- Network status

### Test connectivity

From PS-01:

- `ping X.X.X.X`

---

## 7. Install Printer Driver

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
