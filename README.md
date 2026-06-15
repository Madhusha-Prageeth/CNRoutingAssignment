# Computer Networks Assignment - Router Configuration and Routing Protocols

This repository contains the Cisco Packet Tracer networks, configuration scripts, and documentation for the Computer Networks assignment. The project demonstrates the implementation of both **Static Routing** and **Dynamic Routing (RIPv2 & EIGRP)** protocols across multi-router topologies.

## 👤 Student Information
* **Name:** E.M.M.P.S.Ekanayaka
* **Student ID:** 39318[cite: 2]
* **University:** NSBM Green University[cite: 2]
* **Module:** Computer Networks[cite: 2]
* **Lecturer:** Mr. Krishantha Ranaweera[cite: 2]
* **Submission Date:** 14 June 2026[cite: 2]

---

## 🛠️ Technologies & Tools Used
* **Cisco Packet Tracer** (Network Simulation & Configuration)[cite: 2]
* **Cisco IOS CLI** (Router & Switch Configurations)[cite: 2]
* **Routing Protocols:** Static Routing, RIPv2, EIGRP[cite: 2]

---

## 📋 Project Structure & Tasks

### 🔹 Task 1: Basic Router Configuration
Initial configuration for Cisco 2911 routers to establish secure console access and unique device identity[cite: 2].
* Hostname assignment (`kandyNSBM_39318`)[cite: 2].
* Securing the console line with password mechanisms[cite: 2].
* Configuration saving using the privileged EXEC mode (`write memory`)[cite: 2].

### 🔹 Task 2: Static Routing Implementation
A 3-router fully mesh/redundant network architecture mapping dedicated departmental or regional subnets[cite: 2].

| Router Name | Connected LAN Subnet | WAN Interfaces | Next-Hop Targets |
| :--- | :--- | :--- | :--- |
| **ComputingRouter** (Router 0) | `192.168.1.0/24` | `11.0.0.0/30`, `12.0.0.0/30` | `12.0.0.2`, `11.0.0.2` |
| **Router 1** | `192.168.2.0/24` | `12.0.0.0/30`, `14.0.0.0/30` | `12.0.0.1`, `14.0.0.2` |
| **ScienceRouter** (Router 2) | `192.168.3.0/24` | `11.0.0.0/30`, `14.0.0.0/30` | `11.0.0.1`, `14.0.0.1` |

### 🔹 Task 3: Dynamic Routing (RIPv2 & EIGRP)
Transitioning from static layouts to adaptive, dynamic network infrastructures using a linear 3-node topology (`KandyNSBM` ↔ `ColomboNSBM` ↔ `GalleNSBM`)[cite: 2].

* **Part A - RIPv2:** Classless dynamic routing configuration enabling automatic network discovery via RIP Version 2[cite: 2].
* **Part B - EIGRP:** Advanced distance-vector deployment utilizing Autonomous System (AS 10) for optimized routing convergence and metric calculation[cite: 2].

---

## 💻 Key Configuration Snippets

### Static Routing Example (Router 1)
```text
Router> enable
Router# configure terminal
Router(config)# ip route 192.168.1.0 255.255.255.0 12.0.0.1
Router(config)# ip route 192.168.3.0 255.255.255.0 14.0.0.2
