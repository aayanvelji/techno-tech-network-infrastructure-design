# Branch Network Designs

This document summarises the four branch LAN designs described in the Techno Tech university assignment. Each branch uses an extended-star LAN topology. Department names, device roles and address plans below follow the report.

## Malaysia — Headquarters

Malaysia is identified as the company headquarters and the main point of contact for customers in Malaysia.

### Departments and devices

The report identifies five areas:
- **Finance:** handles expenses and revenue and maintains compliance with Malaysian regulations.
- **IT:** provides technical support and maintains the branch's network infrastructure, services and devices.
- **Administration:** coordinates daily administrative work, documentation and external communication.
- **Human Resources:** supports employee-related activities.
- **Server department:** provides the branch's server facilities.

The design uses standard computing devices such as PCs, laptops, smartphones and printers. The Malaysia assumptions state that the branch does not use specialised IoT infrastructure.

### LAN and addressing

The report specifies an extended-star LAN and the 10.10.x.x address range. Its device tables use the 10.10.1.x network with a 255.255.255.0 mask and gateway 10.10.1.1. The listed server addresses are:
- HQ/DNS: 10.10.1.100
- Web: 10.10.1.101
- Mail: 10.10.1.102

The report's addressing summary gives department gateway values within the shared 10.10.1.x range. Refer to the source assignment for the individual endpoint table.

## Singapore — Business centre

Singapore is described as the company's business centre and local point of contact for potential customers.

### Departments and devices

The four areas are Finance, IT, Administration and Server Room. The report describes security and IoT equipment including air conditioners, cameras, RFID card readers and security doors. Finance includes desktops, wireless laptops, printers and smartphones. IT is described as a smaller team with desktop, laptop, smartphone and printer equipment. Administration includes manager facilities and employee devices.

The server room hosts the branch IoT server and the company's web and DNS servers, as described in the assignment.

### LAN and addressing

Singapore uses 10.20.x.x addressing, with /28 subnets (255.255.255.240) for the four department/server networks:

| Area | Network | Gateway |
|---|---|---|
| Finance | 10.20.1.0/28 | 10.20.1.1 |
| IT | 10.20.2.0/28 | 10.20.2.1 |
| Administration | 10.20.3.0/28 | 10.20.3.1 |
| Server Room | 10.20.4.0/28 | 10.20.4.1 |

The assignment lists the local service addresses as IoT 10.20.4.5, web 10.20.4.6 and DNS 10.20.4.7.

## Australia — Branch office

Australia is described as a full branch office supporting local staff and providing local web/FTP and IoT monitoring services.

### Functional areas and devices

- **Finance:** PCs, laptops, mobile devices and security equipment.
- **IT:** PCs, laptops, mobile devices and security equipment.
- **Administration:** staff devices and security equipment.
- **Server Room:** web and FTP servers, IoT monitoring and security devices.

The assumptions describe one security camera in each area and four environmental sensors in the server room: temperature, smoke, humidity and CO2. The design uses one router with separate physical interfaces for the four functional areas, avoiding VLAN/trunk complexity.

### LAN and addressing

Australia uses 10.30.x.x. Each functional area is assigned a /28 network (255.255.255.240), providing 14 usable host addresses according to the assignment.

| Area | Network | Gateway |
|---|---|---|
| Finance | 10.30.1.0/28 | 10.30.1.1 |
| IT | 10.30.2.0/28 | 10.30.2.1 |
| Administration | 10.30.3.0/28 | 10.30.3.1 |
| Server Room / IoT | 10.30.4.0/28 | 10.30.4.1 |

The listed servers are AU-WEB-SRV at 10.30.4.3 (HTTP and DNS) and AU-FTP-SRV at 10.30.4.4 (FTP). The IoT gateway is listed at 10.30.4.5.

## Japan — Branch office

Japan is described as the business hub for Techno Tech in Japan and the local point of contact for customers.

### Departments and devices

Japan has four departments:
- **Finance:** local expenses and revenue.
- **IT:** technical assistance and maintenance of systems, networks and devices.
- **Administration:** daily operations, documentation, contracts and client coordination.
- **Human Resources:** recruitment, training, performance management and workplace policies.

The report describes cameras in each department. Finance and HR use wired and wireless computers/laptops; IT also includes tablets, printers and servers; Administration includes manager facilities, a dedicated printer and wireless laptop.

### LAN and addressing

Japan uses the 10.40.x.x range and /24 subnet masks (255.255.255.0), as stated in the branch design. The department gateway table lists:
- Administration: 10.40.1.1
- HR: 10.40.2.1 in the branch interface table
- Finance: 10.40.3.1
- IT: 10.40.4.1

The Chapter 3 addressing summary separately lists HR as 10.40.3.1, which conflicts with the branch interface table. This document preserves the branch table's department mapping and records the discrepancy rather than choosing an unverified correction. The Japan DNS server is listed as 10.40.4.15 and the email server as 10.40.4.8.

## LAN topology common to the branches

The assignment describes an **extended-star topology**: end devices connect to switches, and switching infrastructure connects toward a router. The report identifies scalability, improved performance, fault isolation and centralised management as benefits, while noting equipment, cabling, space, power and management costs.

## Source

Based on Chapters 1.1–1.4 and Chapter 3 of the submitted *Networking Assignment* report. Addressing discrepancies are explicitly noted where the report's own sections differ.
