# Techno Tech – Enterprise Network Infrastructure Design

A university group project designing a multi-branch enterprise network for Techno Tech using Cisco Packet Tracer.

## Project overview

The proposed network connects four branch offices:
- **Malaysia** — headquarters
- **Singapore** — business centre
- **Australia** — branch office with local web, FTP and IoT services
- **Japan** — branch office with DNS and the centralised company email service

The assignment covers branch LAN design, IP addressing, a full-mesh WAN, router and switch configuration, wireless access, end devices and network services.

## Network architecture

- **LAN:** Extended-star topology at each branch.
- **WAN:** Full-mesh topology connecting all four branches through six point-to-point serial links.
- **Routing:** RIP is identified as the routing protocol in Chapter 3 of the assignment.
- **Addressing:** Branch-specific private address ranges are used: Malaysia 10.10.x.x, Singapore 10.20.x.x, Australia 10.30.x.x and Japan 10.40.x.x. WAN links use 10.255.0.x.
- **Services:** DNS, HTTP, FTP, centralised email, IoT monitoring and wireless access.

See the [branch designs](documentation/branch-designs.md), [WAN architecture](documentation/wan-architecture.md), [IP addressing](documentation/ip-addressing.md), [network configuration](documentation/network-configuration.md) and [network services](documentation/network-services.md).

## Team project and responsibilities

This is a collaborative university assignment completed by:
- Aayan Velji — Japan branch; local DNS and centralised email server for all branches; email-server configuration and account creation.
- Mohammed Mujtaba Ahmed — Singapore branch; local DNS, web and IoT; WAN and configuration documentation.
- Mohammed Bilal Namoji — Malaysia branch; local DNS and web; configuration documentation.
- Keyaan Minhas — Australia branch; local DNS, FTP, web and IoT; WAN connection in Packet Tracer; configuration documentation.

The [individual contribution record](documentation/my-contribution.md) distinguishes Aayan's assigned work from the overall group project.

## Repository structure

| Path | Contents |
|---|---|
| `documentation/` | Project overview, branch designs, WAN, addressing, configurations, services and contribution |
| `packet-tracer/FINAL_PRESENTATION.pkt` | Original Cisco Packet Tracer project file |
| `reports/` | Information about the source university report |
| `presentation/` | Information about presentation material |

The repository is intentionally **image-free**. No screenshots or exported diagrams are included.

## Opening the simulation

Open `packet-tracer/FINAL_PRESENTATION.pkt` with Cisco Packet Tracer. The written documentation in this repository is based on the submitted assignment report. The Packet Tracer file is included as the simulation artefact; the text documentation should not be interpreted as a fresh independent test of every device or service.

## Source and security notes

- The university assignment report is the source for the design descriptions, address tables, device roles and recorded task allocation.
- Passwords, account credentials, wireless keys and student identification numbers are deliberately excluded from this repository.
- Addressing values are reproduced from the report. Where the source contains a value that appears inconsistent within its own tables, it is identified as recorded rather than silently corrected.
- Obtain any required group permission and follow university rules before making the repository public.
