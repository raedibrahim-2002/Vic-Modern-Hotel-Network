# Vic Modern Hotel Network

End-of-year networking project designed and implemented in **Cisco Packet Tracer**.

## Topology
![Topology](Hotel_Screenshot.png)

## Overview
The hotel has three floors, each with its own router and switch:

| Floor | Departments |
|-------|-------------|
| 1st   | Reception, Store, Logistics |
| 2nd   | Finance, HR, Sales/Marketing |
| 3rd   | IT, Admin |

## VLANs & Networks

| Floor | Department | VLAN | Network |
|-------|-----------|------|---------|
| 1st | Reception | 80 | 192.168.8.0/24 |
| 1st | Store | 70 | 192.168.7.0/24 |
| 1st | Logistics | 60 | 192.168.6.0/24 |
| 2nd | Finance | 50 | 192.168.5.0/24 |
| 2nd | HR | 40 | 192.168.4.0/24 |
| 2nd | Sales | 30 | 192.168.3.0/24 |
| 3rd | Admin | 20 | 192.168.2.0/24 |
| 3rd | IT | 10 | 192.168.1.0/24 |

## Router Links (Serial DCE)
- F2 ↔ F3: `10.10.10.0/30`
- F3 ↔ F1: `10.10.10.4/30`
- F1 ↔ F2: `10.10.10.8/30`

## Features Implemented
- Inter-VLAN routing on each floor
- OSPF dynamic routing between the three routers
- DHCP server on each router
- Wi-Fi access point on each floor
- Printer in every department
- SSH remote login on all routers
- Port security on the IT switch (fa0/1, sticky MAC, violation mode: shutdown)

## How to Open
Open `Hotel_Management.pkt` using Cisco Packet Tracer.