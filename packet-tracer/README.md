# Cisco Packet Tracer Project

## Project file

- `FINAL_PRESENTATION.pkt` — the group's original Cisco Packet Tracer project file. Keep this native file unchanged.

Open the file with Cisco Packet Tracer to inspect the topology and device configurations.

## Intended network represented

The assignment describes a four-branch enterprise network:

- **Malaysia (headquarters)**
- **Singapore**
- **Australia**
- **Japan**

The written design describes an extended-star LAN topology at each branch and a full-mesh WAN between the four branch routers. The full mesh is documented as six serial point-to-point links using /30 subnets from 10.255.0.0/30 to 10.255.0.20/30.

The assignment describes department LANs, wired and wireless end devices, access points, switches, routers, servers and IoT endpoints. Services documented include DNS, HTTP/web, FTP, centralised email and IoT monitoring. The branch-specific address plans are recorded in [IP Addressing](../documentation/ip-addressing.md), and the intended service roles are in [Network Services](../documentation/network-services.md).

## How to open

1. Install or open Cisco Packet Tracer.
2. Open `FINAL_PRESENTATION.pkt`.
3. Inspect the branch topology and router-to-router serial links.
4. Select individual routers, switches, servers and endpoints to review their configurations.
5. Use the verification checklist in [Testing and Verification](../documentation/testing-and-verification.md) to record tests you personally perform.

## Verification status

The file is preserved as supplied by the group. Its presence in GitHub is not evidence that every interface, routing protocol, service or end-to-end path has been tested. No successful ping, DNS, HTTP, FTP, email or IoT result is claimed by this repository unless a result is recorded in the testing document after an actual test.

## Important source discrepancies

The written assignment has conflicting values for some gateways and routing protocol descriptions. These are listed in the IP addressing and network configuration documents. Check the Packet Tracer configuration before treating a disputed value as final.

## Repository policy

This repository is intentionally image-free. No screenshots or exported images are included. The native Packet Tracer project is retained as the project artifact.
