# SLIIT Y1S1 Data Communication Networks - Enterprise Network Design (Group 13)

[![SLIIT Faculty of Computing](https://img.shields.io/badge/SLIIT-Faculty%20of%20Computing-blue.svg)](https://www.sliit.lk/)
[![Module](https://img.shields.io/badge/Module-IE1030%20DCN-orange.svg)]()
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()

This repository contains the comprehensive enterprise network design proposal, Cisco Packet Tracer simulation files, device CLI configurations, cable/port calculations, and cost estimates for **Group 13** as part of the Year 1 Semester 1 Data Communication Networks (IE1030) module at the Sri Lanka Institute of Information Technology (SLIIT)[cite: 1].

---

## 👥 Group 13 Members & Contributions

| IT Number | Name | Role / Contribution |
| :--- | :--- | :--- |
| **IT26102361** | VINOJA H.W.O. | Team Leader (Overall Coordination & Documentation)[cite: 1, 37] |
| **IT26102355** | KULATHUNGA M.A.S.S. | Group Member (Logical Network Design & Calculations)[cite: 1, 37] |
| **IT26102368** | PERERA M.K.J.C. | Group Member (Physical Network Layout & Cabling)[cite: 1, 37] |
| **IT26102357** | SUBHASHANA T.O. | Group Member (Device Specifications & Equipment Racks)[cite: 1, 37] |
| **IT26102317** | SITHUMINI W.T.I. | Group Member (Wireless Network Design & AP Planning)[cite: 1, 37] |
| **IT26102348** | DAMAYANTHA H.A.E. | Group Member (Cost Estimation & Verification)[cite: 1, 37] |

---

## 🏗️ Executive Summary & Scope

The project involves designing a robust, scalable, and secure enterprise network infrastructure for a two-story office building measuring $18\text{ m} \times 10\text{ m}$ per floor[cite: 5]. The network accommodates high-density wired office drops alongside high-speed wireless connectivity for employees, management, and visitors[cite: 5].

* **Total Active Nodes:** 42 wired connections + 54 wireless clients = **96 active nodes**[cite: 11]
* **Wired Infrastructure:** 36 Desktop PCs and 6 IP phones distributed evenly across both floors (21 wired drops per floor)[cite: 9]
* **Wireless Infrastructure:** 4 $\times$ TP-Link EAP225 AC1350 Access Points (2 per floor) configured for optimal indoor coverage with an 8m planning radius[cite: 20, 23]
* **Internet Gateway:** SLT-Mobitel Fiber Unlimited Pro (500 Mbps download / 200 Mbps upload) terminating via an Optical Network Terminal (ONT) into a Cisco 2911 Integrated Services Router[cite: 10, 11]

---

## 🛠️ Hardware & Active Stack Specifications

| Layer / Category | Equipment Model | Quantity & Specifications |
| :--- | :--- | :--- |
| **Internet Gateway** | Cisco 2911 Integrated Services Router | 1 unit (2U rack-mount, 3 onboard Gigabit Ethernet ports) |
| **Core & Access Switches** | Cisco Catalyst 2960X-24PS-L | 3 units ($24 \times 10/100/1000\text{ Mbps}$ PoE+ ports, 370W power budget) |
| **Wireless Access Points** | TP-Link EAP225 AC1350 | 4 units (Dual-band 802.11ac Wave 2, ceiling-mounted, PoE powered) |
| **Inter-Floor Backbone** | OM3 Multimode Fiber Optic Cable | 30m length, 4-core OM3 trunk with LC connectors |
| **Power Protection** | APC Smart-UPS SMC1500I-2UC | 2 units (1500VA / 900W Line-Interactive UPS, 2U rack mount) |
| **Network Racks** | Linkbasic 12U Floor-Standing Racks | 2 units ($600 \times 600\text{ mm}$ with glass door, one per floor) |

---

## 📏 Cabling, Patching & Port Calculations

* **Horizontal Cabling:** Cat6 UTP cables run from floor racks via cable trays to RJ45 wall outlets. Total calculated length required is **794 meters** (including a 15% waste allowance; 3 boxes of 305m = 915m purchased).
* **Patch Panels:** Two 24-port Cat6 patch panels (1 per floor rack). Each floor utilizes 23 ports (21 wired drops + 2 AP ceiling drops), leaving 1 spare port per floor.
* **Patch Cords:** 100 factory-molded Cat6 patch cords (1m and 2m variants) and 4 LC-LC duplex multimode OM3 fiber patch cords.

---

## 💰 Financial & Cost Estimation

| Cost Category | Total Amount (LKR) |
| :--- | :--- |
| **Active Network Equipment** | LKR 857,473 |
| **Passive Equipment & Cabling** | LKR 532,500 |
| **Installation, Labor & Testing** | LKR 130,000 |
| **Initial Project Cost** | **LKR 1,519,973** |
| **Monthly Internet Service (SLT Fiber Pro)** | LKR 25,870 (incl. taxes) |

---

## 🚀 Network Implementation & Verification

The logical and physical network topologies were fully implemented and simulated in **Cisco Packet Tracer**. 
* **IP Addressing Scheme:** Static IPv4 assignment utilizing subnet `192.168.1.0/24`.
* **Connectivity Verification:** Comprehensive ICMP echo requests (`ping`) were executed across all gateway, switch, and router interfaces, achieving a **100% success rate** with zero packet loss and minimal round-trip latency ($0–3\text{ ms}$).
```eof

---

## 📂 Repository Structure

```text
📦 SLIIT-Y1S1-DCN-Enterprise-Network-Design
 ┣ 📂 docs/
 ┃  ┗ 📜 DCN-GRP-WD-13-Proposal.pdf      # Complete 37-page formal group proposal document
 ┣ 📂 packet-tracer/
 ┃  ┗ 📜 enterprise-network.pkt          # Cisco Packet Tracer simulation topology
 ┣ 📂 configs/
 ┃  ┣ 📜 router-config.txt               # Cisco 2911 router CLI configuration
 ┃  ┣ 📜 core-switch-config.txt          # Core switch & VLAN configurations
 ┃  ┗ 📜 floor-switches-config.txt       # Ground & First floor switch CLI configurations
 ┗ 📜 README.md                          # Project documentation


