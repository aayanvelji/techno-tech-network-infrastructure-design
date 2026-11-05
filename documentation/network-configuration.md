# Network Configuration

This document summarises configuration examples and the routing information stated in the assignment. Passwords and other secrets from the source report are intentionally omitted.

## Router configuration example — Australia

The report identifies the Australia router as TT-AU-R1 and lists these LAN interfaces:

| Interface in assignment | Purpose | Address / mask |
|---|---|---|
| GigabitEthernet 5/0 | Finance | 10.30.1.1 255.255.255.240 |
| GigabitEthernet 6/0 | IT | 10.30.2.1 255.255.255.240 |
| GigabitEthernet 7/0 | Administration | 10.30.3.1 255.255.255.240 |
| GigabitEthernet 8/0 | Server / IoT | 10.30.4.1 255.255.255.240 |

The report's example uses hostname configuration, disabling DNS lookup, password-encryption settings, a login banner, console and VTY line settings, interface descriptions, addressing and enabling interfaces. Credentials are omitted.

```text
enable
configure terminal
hostname TT-AU-R1
no ip domain-lookup
service password-encryption
!
interface gigabitEthernet5/0
 description To SW-AU-FIN (Finance LAN)
 ip address 10.30.1.1 255.255.255.240
 no shutdown
exit
interface gigabitEthernet6/0
 description To SW-AU-IT (IT LAN)
 ip address 10.30.2.1 255.255.255.240
 no shutdown
exit
interface gigabitEthernet7/0
 description To SW-AU-ADMIN (Admin LAN)
 ip address 10.30.3.1 255.255.255.240
 no shutdown
exit
interface gigabitEthernet8/0
 description To SW-AU-SRV (Servers/IoT LAN)
 ip address 10.30.4.1 255.255.255.240
 no shutdown
exit
end
copy running-config startup-config
```

These interface identifiers reproduce the Australia router example in the report. Confirm actual device interface names before reusing commands.

## Switch configuration example — Australia IT

The report's SW-AU-IT example assigns VLAN 1 management address 10.30.2.2/28 and default gateway 10.30.2.1.

```text
enable
configure terminal
hostname SW-AU-IT
service password-encryption
interface vlan 1
 ip address 10.30.2.2 255.255.255.240
 no shutdown
exit
ip default-gateway 10.30.2.1
end
copy running-config startup-config
```

The report says other switches follow the same general method with branch- and department-specific addressing.

## WAN interface configuration reference

The assignment documents six serial point-to-point links:

| Branch connection | Local interface / IP | Peer interface / IP | Subnet |
|---|---|---|---|
| Australia–Malaysia | Australia Serial2/0 — 10.255.0.1 | Malaysia Serial6/0 — 10.255.0.2 | 10.255.0.0/30 |
| Singapore–Japan | Singapore Serial6/0 — 10.255.0.5 | Japan Serial6/0 — 10.255.0.6 | 10.255.0.4/30 |
| Malaysia–Singapore | Malaysia Serial7/0 — 10.255.0.9 | Singapore Serial7/0 — 10.255.0.10 | 10.255.0.8/30 |
| Japan–Australia | Japan Serial7/0 — 10.255.0.13 | Australia Serial3/0 — 10.255.0.14 | 10.255.0.12/30 |
| Australia–Singapore | Australia Serial4/0 — 10.255.0.17 | Singapore Serial8/0 — 10.255.0.18 | 10.255.0.16/30 |
| Malaysia–Japan | Malaysia Serial8/0 — 10.255.0.21 | Japan Serial8/0 — 10.255.0.22 | 10.255.0.20/30 |

The report specifies subnet mask 255.255.255.252 (/30) and DCE clock rate 128000 for each serial link. The exact interface commands for every router are not provided in one complete, consistent configuration in the report, so full router configurations are not invented here.

## Routing protocol — unresolved in the source

The source report is inconsistent:

- Chapter 3.5.2 identifies RIP on all routers.
- The Australia branch conclusion refers to RIP version 2.
- Another branch conclusion mentions static routing.

The source does not provide a complete set of routing commands for all four routers. Therefore this repository does not present a guessed RIP/RIPv2/static configuration as verified. Confirm the running configuration in Packet Tracer before adding final routing commands.

## End-device addressing

The report states that DHCP is not used for the documented branch endpoint address plans. PCs, laptops, servers and access-point management interfaces use static addresses from their branch subnets. See [IP Addressing](ip-addressing.md) for device-level values.

## Verification commands

The report lists these commands for checking router and switch settings:

```text
show ip interface brief
show running-config
show interface status
```

These are suggested verification commands from the assignment; this document does not claim fresh output has been collected.

## Security

The source report contains router/switch passwords, FTP and IoT credentials, email passwords and wireless passphrases. They are deliberately excluded. Do not publish credentials in project documentation.

## Source

Based on the submitted assignment's Chapter 3.1–3.6 and Australia router/switch configuration examples.
