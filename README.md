# Local Area Network Foundation 🌐

## 📌 Overview
This is the starting point of my networking journey. This project demonstrates the most essential concept in infrastructure: **Local Connectivity**. It shows how two end-devices communicate within the same broadcast domain using a Switch as the central intermediary.

> **Status:** Fully Functional ✅

## 📐 Network Topology
The topology is simple yet effective for demonstrating Layer 2 principles:
- **Switch:** Acting as the central distribution point for local traffic.
- **End Devices:** 2 PCs connected via Ethernet cables, simulating a small office or home office (SOHO) environment.

![Network Topology](01_Network_topology.png)

## 🛠️ Technical Specifications
- **Hardware:** Cisco Catalyst Switch.
- **Addressing:** Static IPv4 (Class C).
- **Communication:** ICMP Protocol (Ping) for reachability testing.

## ⚙️ Configuration Workflow

### 1. Physical Layer
- Connections established using straight-through cables.
- Interface status verified (Green lights) ensuring physical link stability.

### 2. Logical Layer (IP Addressing)
Both hosts were configured within the same subnet (e.g., 192.168.1.0/24) to allow direct communication without the need for a router:
- **PC-0:** 192.168.1.1
- **PC-1:** 192.168.1.2

## 🧪 Connectivity Verification
The "Moment of Truth" was verified through the Command Prompt. The successful ping exchange confirms that the Switch is correctly learning MAC addresses and forwarding traffic.

| Source | Destination | Status |
| :--- | :--- | :--- |
| PC-0 | PC-1 | Success (0% Loss) |

![Ping Result](06_Pc1_connectivity_Test.png)

---
**Developed by:** Eduardo Almeida  
*Building networking expertise from the ground up.*
