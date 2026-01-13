# Inter-VLAN Routing Fundamentals - CCNA Lab

## 📌 Project Overview
This is a foundational networking laboratory designed to demonstrate the implementation of **VLANs** and **Inter-VLAN Routing**. The project simulates a common enterprise scenario where different departments (VLAN 10 and VLAN 20) need to remain logically isolated at Layer 2 but require routed communication at Layer 3 through a single physical interface.

## 🏗️ Topology & Infrastructure
The network consists of a streamlined "Router-on-a-Stick" architecture:
- **Core Router:** 1x Cisco 1941 Router.
- **Access Switch:** 1x Cisco 2960-24TT Switch.
- **End Devices:** 2x Generic PCs representing different network segments.

### Network Addressing Plan
| Device | VLAN | Subnet | IP Address | Gateway |
| :--- | :--- | :--- | :--- | :--- |
| **PC 1** | 10 (Internal) | 192.168.10.0/24 | 192.168.10.10 | 192.168.10.1 |
| **PC 2** | 20 (Internal) | 192.168.20.0/24 | 192.168.20.10 | 192.168.20.1 |

## 🛠️ Configuration Highlights

### 1. Layer 2 Segmentation (Switch)
- Created VLANs 10 and 20.
- Assigned access ports to respective VLANs.
- Configured a **802.1Q Trunk** link to the router.

### 2. Layer 3 Routing (Router Subinterfaces)
Implemented subinterfaces on the GigabitEthernet interface to act as default gateways:
- `interface gig0/0.10`: Encapsulation dot1Q 10 | IP: 192.168.10.1
- `interface gig0/0.20`: Encapsulation dot1Q 20 | IP: 192.168.20.1

## ✅ Validation & Testing
Connectivity was verified through systematic ICMP testing (Ping):
- **Local Gateway Test:** Success from both PCs to their respective subinterfaces.
- **Inter-VLAN Test:** Success communication between PC 1 (VLAN 10) and PC 2 (VLAN 20).
- **Interface Verification:** Confirmed `up/up` status for all virtual and physical ports.

## 📁 Repository Contents
- `Topologia.png`: Visual network diagram.
- `Configuração IP.png`: Static IP assignment evidence.
- `Teste de Pings.png`: Connectivity validation between segments.
- `Show_vlan_brief.png`: Logical switch configuration proof.

---
*Developed for educational purposes to master Cisco IOS fundamentals.*
