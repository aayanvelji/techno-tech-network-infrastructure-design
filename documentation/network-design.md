# Network Design

## Enterprise layout

The proposed network contains four branch locations:

- Malaysia
- Singapore
- Australia
- Japan

The assignment treats Malaysia as the company's headquarters. Each branch has its own LAN design, floor plan, network diagram and IP-addressing documentation.

## LAN topology

The report describes an **extended star topology** for the branch LAN designs. End devices connect through access switches, with switching infrastructure connected toward a central network device. The report's stated design considerations include scalability, centralized management and easier fault isolation. It also recognises the dependency on central infrastructure and the additional cabling and equipment cost.

## WAN design

The assignment includes a WAN topology chapter and a section describing the connection of all branches in a mesh topology. The report documents IP addressing and routing configuration for the inter-branch links.

The final topology and exact routing behaviour should be verified against the original Packet Tracer file before adding detailed claims or diagrams here.

## Addressing

The report provides branch-specific IP addressing schemes and subnet tables. For example, it assigns the Malaysia branch address space from the 10.10.x.x range and the Singapore branch from the 10.20.x.x range.

Refer to the original assignment report for the full device-level addressing tables. A consolidated, checked addressing reference can be added after validating the simulation file.

## Network services

The assignment documents configuration areas for DNS, web, FTP, email, IoT, access points and end devices. Which services are centralised or branch-local is described in the report and will be cross-checked against the Packet Tracer implementation.