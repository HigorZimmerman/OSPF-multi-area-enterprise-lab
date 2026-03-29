# OSPF Multi-Area Enterprise Lab — Cisco Packet Tracer

## 🎯 Objective

Design and implement a scalable multi-area OSPF topology simulating an enterprise network with hierarchical routing and segmented departments.

---

## 🧠 Architecture Overview

This lab implements a hierarchical OSPF design with a backbone and multiple non-backbone areas for departmental segmentation.

### OSPF Area Design

| Area   | Purpose                   |
| ------ | ------------------------- |
| Area 0 | Backbone core             |
| Area 1 | Branch network A          |
| Area 2 | Branch network B          |
| Area 4 | Technology department LAN |

---

## 🗺️ Logical Topology

![Topology](topology.png)

---

## 🌐 IP Addressing Plan

| Segment        | Network         |
| -------------- | --------------- |
| LAN Technology | 192.168.10.0/24 |
| LAN HR         | 192.168.20.0/24 |
| LAN Branch A   | 192.168.30.0/24 |
| LAN Branch B   | 192.168.40.0/24 |
| R1–R2          | 10.0.0.0/30     |
| R2–R3          | 10.0.0.4/30     |
| R1–R4          | 10.0.0.8/30     |

---

## ⚙️ Technical Decisions

### Hierarchical Routing

* Area 0 used as backbone for inter-area communication
* ABRs performing route summarization and LSA propagation

### Interface Strategy

* WAN links configured as **OSPF point-to-point**
* LAN interfaces configured as **passive** to avoid unnecessary adjacencies

### Routing Control

* Manual Router-ID assignment
* OSPF cost manipulation for path control
* Inter-area route propagation (O IA)

---

## 🔍 Validation

### OSPF Adjacency

All routers reached FULL state with neighbors.

### Routing Table

* Intra-area routes propagated correctly
* Inter-area routes learned via backbone
* O IA entries present on ABRs

### End-to-End Connectivity

Successful ICMP communication between all LAN segments.

---

## 📁 Configurations

Router configurations available in:
configs/

---

## 🧪 Simulation Environment

Developed using Cisco Packet Tracer

---

## 🏢 Real-World Use Cases

* Enterprise campus networks
* Corporate branch expansion
* Multi-site backbone design
* Departmental traffic segmentation

---

## 🚀 Key Technologies

* OSPFv2
* Multi-area design
* Area Border Router (ABR)
* Inter-area routing
* Cost-based path selection
* Passive interfaces
