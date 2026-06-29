# Queue & Spooler Management (PS-01)

This file covers how to manage print queues and troubleshoot print issues on a Windows Print Server.

---

## 1. View Print Queue

On PS-01:

- Press **Win+R**
- Enter:
  - `printmanagement.msc`

Then:

- Navigate to:
  - Print Servers\PS-01\Printers
- Select printer:
  - FollowMe_Colour or FollowMe_Mono

Then:

- Open **See what's printing**

This displays:
- Active jobs
- Paused jobs
- Failed jobs

---

## 2. Cancel Stuck Print Jobs

If a job is stuck:

- Right-click job
- Select:
  - Cancel

If it does not clear:

- Restart Print Spooler (see below)

---

## 3. Restart Print Spooler Service

On PS-01:

- Press **Win+R**
- Enter:
  - `services.msc`

Locate:

- Print Spooler

Then:

- Right-click \ Restart

---

## 4. Manual Spooler Reset (if required)

If spooler is still stuck:

- Stop Print Spooler
- Clear queue manually if needed
- Start Print Spooler again

---

## 5. Verify After Reset

- Re-open `printmanagement.msc` (Win+R)
- Confirm queues are empty or jobs are processing normally
- Test print from CLIENT-01 if required

---

## Result

Print queue issues are managed through Print Management or Print Spooler service control, ensuring stable operation of FollowMe_Colour and FollowMe_Mono queues.