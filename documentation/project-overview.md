# Project Overview

Techno Tech is a proposed multinational organisation with branches in Malaysia (headquarters), Singapore, Australia and Japan. The assignment covers four extended-star branch LANs, a full-mesh WAN with six serial /30 point-to-point links, branch IP addressing, routers, switches, end devices, wireless access and network services.

## Branch address spaces

| Branch | Address space |
|---|---|
| Malaysia | 10.10.x.x |
| Singapore | 10.20.x.x |
| Australia | 10.30.x.x |
| Japan | 10.40.x.x |

The WAN uses 10.255.0.x.

## Routing

The group confirmed that the Packet Tracer network uses **RIP Version 2 (RIPv2)** across the four-branch network. This clarifies the inconsistent routing references in different sections of the assignment report. See [Network Configuration](network-configuration.md).

## Team responsibilities

- Mohammed Bilal Namoji: Malaysia branch, local DNS and web, configuration documentation.
- Mohammed Mujtaba Ahmed: Singapore branch, local DNS, web and IoT, WAN and configuration documentation.
- Keyaan Minhas: Australia branch, local DNS, FTP, web and IoT, WAN connection in Packet Tracer, configuration documentation.
- Aayan Velji: Japan branch, local DNS, centralised email server for all branches, email configuration and account creation, configuration documentation and individual conclusion.

## Group testing

The group reports that network connectivity and the configured services were tested collectively in Packet Tracer and worked successfully. The testing document records this as a group-reported outcome; detailed command output or individual test logs were not added to the repository.

The original Cisco Packet Tracer file is stored at `packet-tracer/FINAL_PRESENTATION.pkt`.

## Source

Submitted Networking Assignment, branch design chapters, WAN chapter, configuration chapter and task allocation table; group confirmations during documentation review.
