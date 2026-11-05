# Techno Tech – Enterprise Network Infrastructure Design

A university group project designing a multi-branch enterprise network for Techno Tech using Cisco Packet Tracer.

## Project overview

The proposed network connects four branch offices: **Malaysia (headquarters), Singapore, Australia and Japan**. The assignment covers branch LAN design, IP addressing, a full-mesh WAN, router and switch configuration, wireless access, end devices and network services.

## Network architecture

- **LAN:** Extended-star topology at each branch.
- **WAN:** Full-mesh topology connecting all four branches through six point-to-point serial links.
- **Routing:** RIP Version 2 (RIPv2), confirmed by the group as the routing method used in the Packet Tracer project.
- **Addressing:** Malaysia 10.10.x.x, Singapore 10.20.x.x, Australia 10.30.x.x, Japan 10.40.x.x; WAN links use 10.255.0.x.
- **Services:** DNS, HTTP, FTP, centralised email, IoT monitoring and wireless access.

See [branch designs](documentation/branch-designs.md), [WAN architecture](documentation/wan-architecture.md), [IP addressing](documentation/ip-addressing.md), [network configuration](documentation/network-configuration.md), [network services](documentation/network-services.md) and [testing and verification](documentation/testing-and-verification.md).

## Team project and responsibilities

This is a collaborative university assignment:
- **Aayan Velji:** Japan branch; local DNS and centralised email server for all branches; email-server configuration and account creation.
- **Mohammed Mujtaba Ahmed:** Singapore branch; local DNS, web and IoT; WAN and configuration documentation.
- **Mohammed Bilal Namoji:** Malaysia branch; local DNS and web; configuration documentation.
- **Keyaan Minhas:** Australia branch; local DNS, FTP, web and IoT; WAN connection in Packet Tracer; configuration documentation.

See [Individual Contribution](documentation/my-contribution.md) for Aayan's assigned responsibilities. The work is presented as a group project, not as an individual build.

## Group testing

The group reports that connectivity and all configured services were tested collectively in Packet Tracer and worked successfully. See [Testing and Verification](documentation/testing-and-verification.md) for the reported test coverage and evidence limitations.

## Repository structure

| Path | Contents |
|---|---|
| `documentation/` | Project overview, branch designs, WAN, device-level addressing, configuration, services, testing and contribution |
| `packet-tracer/FINAL_PRESENTATION.pkt` | Original Cisco Packet Tracer project file |

The repository is intentionally **image-free**. No screenshots or exported diagrams are included.

## Opening the simulation

Open `packet-tracer/FINAL_PRESENTATION.pkt` with Cisco Packet Tracer.

## Source and security notes

- The university assignment report is the source for design descriptions, address tables, device roles and recorded task allocation.
- Malaysia and Japan gateway details were clarified against the group's Packet Tracer project during documentation review. Singapore and Australia gateway tables remain based on the assignment's addressing summary.
- Passwords, account credentials, wireless keys and student identification numbers are deliberately excluded.
- Obtain any required group permission and follow university rules before making the repository public.
