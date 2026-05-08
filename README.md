<div align="center">

# NetArch-MultiCampus

**Design and Implementation of a Multi-Campus University Network Infrastructure**

Cisco Packet Tracer | Computer Networks | BSSE-6th | Spring 2026

---

</div>

## About The Project

A comprehensive network infrastructure project simulating the design and deployment of a scalable
university network spanning **six geographically distributed campuses** across the country. This project
demonstrates enterprise-grade network architecture principles including hierarchical design, VLSM-based
IP management, and department-level network segmentation using **Cisco Packet Tracer**.

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

| Department  | PCs       | Servers                  | Network Devices          |
|-------------|-----------|--------------------------|--------------------------|
| Admin       | 20 - 40   | DHCP, DNS, Web, Mail     | Managed Switches         |
| Faculty     | 50 - 100  | Dedicated Server         | Managed Switches         |
| Students    | 500 - 1000| Dedicated Server         | Managed Switches         |
| Wi-Fi Zone  | 10 - 50 APs | --                    | Wireless LAN Controller  |

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

---

## Technology Stack

| Component        | Technology                                |
|------------------|-------------------------------------------|
| Simulation Tool  | Cisco Packet Tracer                       |
| IP Addressing    | VLSM (Variable Length Subnet Masking)     |
| Services         | DHCP, DNS, Web Server, Mail Server        |

---

## Repository Structure

```
NetArch-MultiCampus/
|-- CN_Project_Topology.pkt              # Cisco Packet Tracer topology file
|-- Spring2026-CN_Semester_Project.pdf   # Project requirements document
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
3. Explore the network topology and test connectivity

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
