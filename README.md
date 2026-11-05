# Techno Tech – Enterprise Network Infrastructure Design

A university group project designing a multi-branch enterprise network for Techno Tech using Cisco Packet Tracer.

## Project overview

The proposed network connects four branch offices: **Malaysia (headquarters), Singapore, Australia and Japan**. The assignment covers branch LAN design, IP addressing, a full-mesh WAN, router and switch configuration, wireless access, end devices and network services.

## Network architecture

- **LAN:** Extended-star topology at each branch.
- **WAN:** Full-mesh topology connecting all four branches through six point-to-point serial links.
- **Routing:** RIP is identified in Chapter 3 of the assignment.
- **Addressing:** Malaysia 10.10.x.x, Singapore 10.20.x.x, Australia 10.30.x.x, Japan 10.40.x.x; WAN links use 10.255.0.x.
- **Services:** DNS, HTTP, FTP, centralised email, IoT monitoring and wireless access.

See [branch designs](documentation/branch-designs.md), [WAN architecture](documentation/wan-architecture.md), [IP addressing](documentation/ip-addressing.md), [network configuration](documentation/network-configuration.md) and [network services](documentation/network-services.md).

## Team project and responsibilities

This is a collaborative university assignment:
- **Aayan Velji:** Japan branch; local DNS and centralised email server for all branches; email-server configuration and account creation.
- **Mohammed Mujtaba Ahmed:** Singapore branch; local DNS, web and IoT; WAN and configuration documentation.
- **Mohammed Bilal Namoji:** Malaysia branch; local DNS and web; configuration documentation.
- **Keyaan Minhas:** Australia branch; local DNS, FTP, web and IoT; WAN connection in Packet Tracer; configuration documentation.

See [Individual Contribution](documentation/my-contribution.md) for Aayan's assigned responsibilities. The work is presented as a group project, not as an individual build.

## Repository structure

| Path | Contents |
|---|---|
| `documentation/` | Project overview, branch designs, WAN, device-level addressing, configuration, services, testing checklist and contribution |
| `packet-tracer/FINAL_PRESENTATION.pkt` | Original Cisco Packet Tracer project file |

The repository is intentionally **image-free**. No screenshots or exported diagrams are included.

## Opening the simulation

Open `packet-tracer/FINAL_PRESENTATION.pkt` with Cisco Packet Tracer. The written documentation is based on the submitted assignment report; it is not a fresh independent test of every device, service or connectivity path.

## Source and security notes

- The university assignment report is the source for design descriptions, address tables, device roles and recorded task allocation.
- Passwords, account credentials, wireless keys and student identification numbers are deliberately excluded.
- Addressing values are reproduced from the report. Where its own sections differ, the discrepancy is identified rather than silently corrected.
- Obtain any required group permission and follow university rules before making the repository public.
