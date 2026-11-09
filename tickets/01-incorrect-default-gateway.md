# Ticket 01: Incorrect Default Gateway

**Type:** Simulated support incident
**Affected device:** Admin-PC1
**Status:** Resolved

## Reported Problem
An Administration employee could reach another Administration
computer but could not reach a computer in Sales.

## Fault Introduced
Changed Admin-PC1 to static IPv4 configuration with:
- IP address: 192.168.10.21
- Subnet mask: 255.255.255.0
- Incorrect default gateway: 192.168.10.254

## Investigation
- Ping to Admin-PC2 (192.168.10.22) succeeded.
- Ping to Sales-PC1 (192.168.20.21) timed out on all four attempts.
- Compared the PC's gateway setting with the documented
  Administration router interface address, 192.168.10.1.

## Root Cause
Admin-PC1 had an incorrect default gateway. It could communicate
within its own subnet but could not forward traffic to Sales
through the router.

## Resolution
Changed the default gateway to 192.168.10.1.

## Verification
Repeated the ping to 192.168.20.21:
- Packets sent: 4
- Packets received: 4
- Packet loss: 0%

## Before the fix
<img width="298" height="260" alt="ticket-01-before-fix" src="https://github.com/user-attachments/assets/e2c9cbf5-034f-47de-b9f4-de57f8b3ed3c" />

## After the fix
<img width="319" height="154" alt="ticket-01-after-fix" src="https://github.com/user-attachments/assets/f8be77b1-051c-4b9a-b248-cc3fdb42e33d" />



