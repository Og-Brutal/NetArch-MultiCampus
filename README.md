<div align="center">

# NetArch-MultiCampus

**Design and Implementation of a Multi-Campus University Network Infrastructure**

Cisco Packet Tracer | Computer Networks | BSSE-6th | Spring 2026

---

</div>

<div align="center">

### -- Network Demo --

<video src="demo/network-demo.mp4" width="100%" controls autoplay muted loop>
  Your browser does not support the video tag.
</video>

*Live demonstration of inter-campus communication across the network infrastructure*

</div>

---

## About The Project

A comprehensive network infrastructure project simulating the design and deployment of a scalable
university network spanning **six geographically distributed campuses** across the country. This project
demonstrates enterprise-grade network architecture principles including hierarchical design, VLSM-based
IP management, VLAN segmentation, dynamic inter-campus routing through a centralized hub topology,
and department-level traffic isolation using **Cisco Packet Tracer**.

Built as part of the **Computer Networks** course (BSSE-6th Semester, Spring 2026).

---

## Project Objective

Design and simulate the complete network infrastructure of a university with six campuses, implementing
IP addressing, subnetting, routing protocols, WAN connectivity, security layers, and redundancy mechanisms.

---

## Campus Architecture

| Campus     | Region   | Role                                    |
|------------|----------|-----------------------------------------|
| Campus A   | Central  | Head Office / Data Center / Central Hub |
| Campus B   | Northern | Regional Campus                         |
| Campus C   | Southern | Regional Campus                         |
| Campus D   | Eastern  | Regional Campus                         |
| Campus E   | Western  | Regional Campus                         |
| Campus F   | Central  | Regional Campus                         |

### Department Scale (Per Campus)

| Department  | PCs        | Servers                  | Network Devices          |
|-------------|------------|--------------------------|--------------------------|
| Admin       | 20 - 40    | DHCP, DNS, Web, Mail     | Managed Switches         |
| Faculty     | 50 - 100   | Dedicated Server         | Managed Switches         |
| Students    | 500 - 1000 | Dedicated Server         | Managed Switches         |
| Wi-Fi Zone  | 10 - 50 APs | --                     | Wireless LAN Controller  |

---

## Implementation Progress

### Phase 1 -- Network Topology Design

- Designed the complete physical and logical topology for all 6 campuses
- Established the hierarchical network model (Core, Distribution, Access layers)
- Configured Campus A as the central hub and primary data center
- Defined WAN link paths between all regional campuses and the central hub

### Phase 2 -- VLSM Subnetting

- Implemented Variable Length Subnet Masking (VLSM) across the entire network
- Allocated optimized subnet blocks for each department in every campus
- Ensured efficient IP address utilization with minimal waste
- Separate subnets assigned for Admin, Faculty, Students, and Server networks per campus
- Point-to-point WAN links assigned dedicated /30 subnets

### Phase 3 -- VLAN Configuration

- Configured separate VLANs for each department (Admin, Faculty, Students, Servers)
- Implemented VLAN trunking between switches using ISL / 802.1Q encapsulation
- Ensured Layer 2 isolation between department traffic within each campus
- Applied consistent VLAN numbering scheme across all 6 campuses

### Phase 4 -- Intra-Campus Communication

- Established inter-VLAN routing within each campus
- Connected all department networks to the campus core router (central hub per campus)
- Configured ISL trunking for seamless intra-campus data flow
- Verified end-to-end connectivity between all departments within a campus

### Phase 5 -- Inter-Campus Communication (In Progress)

- Successfully established routing between Campus B and Campus C through Campus A
- Successfully established routing between Campus B and Campus D through Campus A
- Campus A serves as the transit hub for all inter-campus traffic (hub-and-spoke model)
- WAN serial links configured and operational between Campus A <-> B, Campus A <-> C, and Campus A <-> D
- Routing tables updated to enable cross-campus packet forwarding
- Remaining campuses (E, F) to be connected in upcoming phases

---

## Network Topology Overview

```
                        +-------------+
                        |  Campus B   |
                        |  (Northern) |
                        +------+------+
                               |
                               | WAN Link
                               |
+-------------+         +------+------+         +-------------+
|  Campus E   +---------+  Campus A   +---------+  Campus D   |
|  (Western)  |   WAN   | (Central    |   WAN   |  (Eastern)  |
+-------------+         |    Hub)     |         +-------------+
                        +------+------+
                               |
                               | WAN Link
                               |
+-------------+         +------+------+
|  Campus F   +---------+  Campus C   |
|  (Central)  |   WAN   |  (Southern) |
+-------------+         +-------------+
```

---

## Technology Stack

| Component        | Technology                                |
|------------------|-------------------------------------------|
| Simulation Tool  | Cisco Packet Tracer                       |
| IP Addressing    | VLSM (Variable Length Subnet Masking)     |
| Layer 2          | VLANs, 802.1Q / ISL Trunking             |
| Layer 3          | Inter-VLAN Routing, Static/Dynamic Routing|
| WAN              | Serial Links (Point-to-Point)             |
| Services         | DHCP, DNS, Web Server, Mail Server        |

---

## Repository Structure

```
NetArch-MultiCampus/
|-- CN_Project_Topology.pkt              # Cisco Packet Tracer topology file
|-- Spring2026-CN_Semester_Project.pdf   # Project requirements document
|-- demo/
|   |-- network-demo.mp4                # Network demonstration recording
|-- README.md
```

---

## Getting Started

### Prerequisites

- Cisco Packet Tracer 8.0 or later

### Usage

1. Clone the repository
   ```
   git clone https://github.com/Og-Brutal/NetArch-MultiCampus.git
   ```
2. Open `CN_Project_Topology.pkt` in Cisco Packet Tracer
3. Explore the network topology and test connectivity between campuses

---

## Course Information

| Detail    | Info                    |
|-----------|-------------------------|
| Course    | Computer Networks       |
| Program   | BSSE-6th Semester       |
| Term      | Spring 2026             |
| Duration  | 4 Weeks                 |
| Team Size | 3 Students              |

---

## License

This project is developed for academic purposes as part of the Computer Networks course curriculum.

---

<div align="center">

**NetArch-MultiCampus** -- Building Networks That Connect Worlds

</div>
