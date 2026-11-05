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

## Routing information requiring verification

The assignment does not consistently identify one final routing method. Chapter 3.5.2 identifies RIP, the Australia branch conclusion refers to RIP version 2, and another branch conclusion mentions static routing. The report does not provide a complete, consistent set of routing commands for all four routers. Therefore, this overview does not claim that a particular routing protocol was selected or independently verified. See [Network Configuration](network-configuration.md) and [Testing and Verification](testing-and-verification.md).

## Team responsibilities

- Mohammed Bilal Namoji: Malaysia branch, local DNS and web, configuration documentation.
- Mohammed Mujtaba Ahmed: Singapore branch, local DNS, web and IoT, WAN and configuration documentation.
- Keyaan Minhas: Australia branch, local DNS, FTP, web and IoT, WAN connection in Packet Tracer, configuration documentation.
- Aayan Velji: Japan branch, local DNS, centralised email server for all branches, email configuration and account creation, configuration documentation and individual conclusion.

The original Cisco Packet Tracer file is stored at `packet-tracer/FINAL_PRESENTATION.pkt`. This documentation is based on the assignment report, not an independent verification of every simulation setting or test result.

## Source

Submitted Networking Assignment, branch design chapters, WAN chapter, configuration chapter and task allocation table.
