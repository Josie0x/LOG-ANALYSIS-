# 🛡️ Firewall Log Analysis: Port Scan Incident Report

## Incident Summary

A **port scan** targeting an internal resource was detected and successfully mitigated by the firewall. The attack originated from a single source IP probing **12 different ports** to discover open services.

---
 <img width="1143" height="639" alt="Screenshot 2025-11-13 at 4 27 54 PM" src="https://github.com/user-attachments/assets/ccf2ba22-21e6-4cc8-a87d-f2a63faf19b6" />
---

## 🔎 Attacker and Target Information

| Category | Detail |
| :--- | :--- |
| **Attacker Source IP** | `156.33.252.38` |
| **Target Host IP** | `10.34.1.197` |
| **Activity Type** | **Port Scanning** (Reconnaissance) |

---

## ⚔️ Defense and Findings

The firewall performed as expected, demonstrating effective rule-based policy enforcement.

| Port Status | Ports Identified | Notes |
| :--- | :--- | :--- |
| **Confirmed Open** | **443** (HTTPS), **53**, **1521** | These ports successfully responded to the attacker's probes. |
| **Blocked/Filtered** | 9 Other Ports | The firewall **silently blocked** these requests, sending no response back to the attacker. |

The firewall successfully mitigated the reconnaissance attempt, limiting the attacker's knowledge to three confirmed open ports. Immediate action is required to verify the security and necessity of the services running on ports 443, 53, and 1521.

