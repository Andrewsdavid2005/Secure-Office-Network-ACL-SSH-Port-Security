# 🔐 Secure Office Network — ACL + SSH + Port Security

A hands-on **Cisco Packet Tracer** project that simulates a secure office network using VLAN segmentation, inter-VLAN routing, DHCP, Access Control Lists (ACLs), SSH secure management, and switch port security.

The project also includes **intentional fault injection and troubleshooting** to simulate real-world network engineering tasks.

---

## 📌 Project Overview

This project demonstrates how a small enterprise office network can be designed, configured, secured, monitored, and troubleshot using Cisco IOS.

The network is divided into separate departments using VLANs:

- **VLAN 10 — HR**
- **VLAN 20 — IT**
- **VLAN 30 — SERVER**

A Cisco router provides inter-VLAN routing using **Router-on-a-Stick**.

Security policies are implemented using:

- Extended ACLs
- SSH
- Port Security
- VLAN segmentation

The project also includes controlled network failures such as:

- Incorrect VLAN assignment
- Trunk failure
- ACL misconfiguration
- DHCP failure
- SSH configuration failure

These faults are diagnosed and resolved using Cisco IOS verification commands.

---

# 🎯 Project Objectives

- Design a segmented office network
- Configure VLANs
- Configure access and trunk ports
- Configure Router-on-a-Stick
- Implement inter-VLAN routing
- Configure DHCP
- Implement traffic filtering using ACLs
- Configure secure SSH management
- Configure switch port security
- Perform network troubleshooting
- Verify network connectivity and security policies

---

# 🏗️ Network Topology

```text
                         ┌──────────────┐
                         │     R1       │
                         │ Cisco 2911   │
                         └──────┬───────┘
                                │
                              TRUNK
                                │
                         ┌──────┴───────┐
                         │     SW1      │
                         │ Cisco 2960   │
                         └──┬──┬──┬──┬──┘
                            │  │  │  │
                    ┌───────┘  │  │  └────────┐
                    │          │  │           │
                  PC1         PC2 PC3        PC4
                   HR          HR  IT          IT
                 VLAN 10    VLAN 10 VLAN 20  VLAN 20
                                     
                                │
                             SERVER1
                            VLAN 30
