# FollowMe Printer Setup (PS-01)

This file covers creation of shared FollowMe printer queues on the print server.

These queues provide two logical print paths using a single physical printer:
- Colour printing queue
- Mono (black & white) printing queue

Both point to the same device: `192.168.1.128`

---

## 1. Create Colour Queue (FollowMe_Colour)

On PS-01:
- Press **Win+R**
- Enter:
  - `printmanagement.msc`
- Navigate to:
  - Print Servers\PS-01\Printers
- Add printer using TCP/IP:
  - IP:`192.168.1.128`
  - Port:`FollowMe-Colour`

After installation:

- Open `printmanagement.msc`
- Right-click printer\Manage Sharing...

Then configure:

- Enable:
  - Share this printer

Set share name:

- `FollowMe_Colour`

Then configure colour settings:

- Right-click printer name\Properties
- Go to **Advanced\Printing Defaults...**
- Color:
  - Color 

---

## 2. Create Mono Queue (FollowMe_Mono)

Repeat printer setup using same IP:

- IP:`192.168.1.128`
- Port:`FollowMe_Mono`

After installation:

- Open `printmanagement.msc`
- Right-click printer\Manage Sharing...

Then configure:

- Enable:
  - Share this printer

Set share name:

- `FollowMe_Mono`

Then configure mono settings:

- Right-click printer name\Properties
- Go to **Advanced\Printing Defaults...**
- Color:
  - Grayscale

---

## 3. Verify Print Server Configuration

On PS-01:

- Open `printmanagement.msc`
- Confirm both printers exist under:
  - Print Servers\PS-01\Printers

Check:
- Driver installed correctly
- Both queues are shared
- Colour and mono settings applied correctly

