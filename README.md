# Secure Office Network — Cisco Packet Tracer

A hands-on **Cisco Packet Tracer** project that simulates a secure enterprise office network using **VLAN segmentation, Router-on-a-Stick, DHCP, Extended ACLs, SSH, Port Security, and network troubleshooting**.

The project also includes controlled fault injection to practice a real-world network engineer's workflow:

> **Detect → Analyze → Identify → Fix → Verify → Document**

---

## Project Overview

This project demonstrates the design, configuration, security, and troubleshooting of a small enterprise office network.

The network is divided into three logical departments:

- **VLAN 10 — HR**
- **VLAN 20 — IT**
- **VLAN 30 — SERVER**

A Cisco 2911 router provides inter-VLAN communication using **Router-on-a-Stick**.

Network security is implemented using:

- Extended ACL
- SSH secure management
- Switch Port Security
- VLAN segmentation

DHCP is used to automatically assign IP addresses to HR and IT clients.

The project also contains intentionally introduced network failures to develop practical troubleshooting skills.

---

# Objectives

The main objectives of this project are:

- Design a small enterprise office network
- Create VLAN-based network segmentation
- Configure access ports
- Configure trunking
- Configure 802.1Q
- Implement Router-on-a-Stick
- Configure inter-VLAN routing
- Configure DHCP
- Configure Extended ACLs
- Secure router management using SSH
- Configure switch Port Security
- Test network connectivity
- Introduce controlled network faults
- Troubleshoot network failures
- Verify and document the final configuration

---

# Network Topology

```text
                         ┌─────────────────┐
                         │       R1        │
                         │  Cisco 2911     │
                         │  Router         │
                         └────────┬────────┘
                                  │
                                TRUNK
                                  │
                         ┌────────┴────────┐
                         │      SW1        │
                         │  Cisco 2960     │
                         │     Switch      │
                         └─┬────┬────┬────┬┘
                           │    │    │    │
                         PC1   PC2  PC3  PC4
                          HR    HR   IT   IT
                         V10   V10  V20  V20
                                  │
                                  │
                              SERVER1
                              VLAN 30
