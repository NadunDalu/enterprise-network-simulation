# Multi-Site Enterprise Network Design using Cisco Packet Tracer

## Project Overview

This project demonstrates the design and implementation of a secure multi-site enterprise network using Cisco Packet Tracer. The network consists of a Headquarters (HQ) and a Branch Office connected through a WAN link. The primary objective of the project is to simulate a real-world enterprise environment that supports departmental segmentation, dynamic routing, automated IP addressing, and network security.

The project was developed to strengthen practical networking skills and apply CCNA-level concepts in a realistic enterprise network scenario.

---

## Network Topology

The network consists of:

### Headquarters (HQ)

* Layer 3 Core Switch (Cisco 3650)
* Access Switch (Cisco 2960)
* HQ Router (Cisco ISR 4321)
* DHCP/DNS Server
* IT Department PCs
* HR Department PCs
* Finance Department PCs

### Branch Office

* Branch Router (Cisco ISR 4321)
* Branch Switch (Cisco 2960)
* Branch User PCs

### WAN Connection

* Point-to-Point Serial Link between HQ Router and Branch Router

---

## IP Addressing Scheme

| Network Segment           | Subnet          | Gateway      |
| ------------------------- | --------------- | ------------ |
| VLAN 10 (IT)              | 192.168.10.0/24 | 192.168.10.1 |
| VLAN 20 (HR)              | 192.168.20.0/24 | 192.168.20.1 |
| VLAN 30 (Finance)         | 192.168.30.0/24 | 192.168.30.1 |
| Branch LAN                | 192.168.40.0/24 | 192.168.40.1 |
| HQ-Core ↔ HQ-Router       | 10.0.0.4/30     | -            |
| HQ-Router ↔ Branch-Router | 10.0.0.0/30     | -            |

---

## Technologies and Features Implemented

### VLAN Segmentation

Three VLANs were created to separate departments within the headquarters network:

* VLAN 10 – IT Department
* VLAN 20 – Human Resources (HR)
* VLAN 30 – Finance Department

This improves security, reduces broadcast traffic, and enhances network management.

### Trunking

802.1Q trunking was configured between the core and access switches to allow multiple VLANs to traverse a single physical connection.

### Inter-VLAN Routing

A Layer 3 switch was configured with Switch Virtual Interfaces (SVIs) to enable communication between VLANs while maintaining logical separation.

### DHCP Configuration

DHCP pools were configured to automatically assign IP addresses, subnet masks, and default gateways to client devices.

### OSPF Dynamic Routing

OSPF Area 0 was implemented between the HQ Core Switch, HQ Router, and Branch Router to dynamically exchange routing information and maintain connectivity between sites.

### WAN Connectivity

A serial point-to-point WAN link was configured between the HQ and Branch routers to simulate communication between geographically separated offices.

### NAT/PAT

Port Address Translation (PAT) was configured on the HQ Router, allowing internal devices to share a single external IP address.

### Access Control Lists (ACLs)

Security policies were implemented using ACLs to restrict communication between specific departments.

Example:

* HR users are prevented from accessing Finance resources.
* Other authorized communications remain permitted.

### Port Security

Port security was enabled on access switch ports to limit the number of devices that can connect and prevent unauthorized access.

### SSH Remote Management

Secure Shell (SSH) was configured to allow encrypted remote administration of network devices while disabling insecure management methods.

---

## Verification and Testing

The network was tested using multiple verification methods:

### Connectivity Testing

* Inter-VLAN communication verified using ICMP ping.
* HQ to Branch communication verified successfully.
* End-to-end network connectivity confirmed.

### DHCP Verification

* All client devices successfully obtained IP addresses automatically.
* DHCP bindings verified using Cisco IOS commands.

### OSPF Verification

* OSPF neighbor relationships established successfully.
* Dynamic routes learned and populated in routing tables.

### ACL Verification

* HR department traffic to Finance network successfully blocked.
* Authorized traffic remained functional.

### SSH Verification

* Successful remote login to network devices through SSH.

### Simulation Mode Testing

Packet Tracer Simulation Mode was used to visualize packet flow across the enterprise network and verify routing decisions.

---

## Skills Demonstrated

* Enterprise Network Design
* Cisco Routing and Switching
* VLAN Configuration
* Inter-VLAN Routing
* OSPF Dynamic Routing
* DHCP Configuration
* NAT/PAT Implementation
* Access Control Lists (ACLs)
* Network Security
* SSH Administration
* Troubleshooting and Verification
* Cisco Packet Tracer

---

## Learning Outcomes

Through this project, I gained practical experience in designing, configuring, securing, and troubleshooting enterprise networks. The implementation strengthened my understanding of CCNA networking concepts and provided hands-on exposure to technologies commonly used in modern organizational infrastructures.

---

## Author

**Nadun Daluwatta**

Bachelor of Information and Communication Technology (BICT)

University of Sri Jayewardenepura

Aspiring Network Engineer | CCNA Learner | IT Infrastructure Enthusiast
