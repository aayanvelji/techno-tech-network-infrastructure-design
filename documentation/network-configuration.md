# Network Configuration

This document summarises the configuration approach and representative command patterns in the assignment. Passwords and other secrets from the source report are intentionally omitted.

## Router configuration

The routers provide the default gateways for the department LANs and connect the branches over the WAN. The Australia router example is identified as TT-AU-R1. Its LAN interfaces are assigned:

| Interface in assignment | Purpose | Address / mask |
|---|---|---|
| GigabitEthernet 5/0 | Finance | 10.30.1.1 255.255.255.240 |
| GigabitEthernet 6/0 | IT | 10.30.2.1 255.255.255.240 |
| GigabitEthernet 7/0 | Administration | 10.30.3.1 255.255.255.240 |
| GigabitEthernet 8/0 | Server / IoT | 10.30.4.1 255.255.255.240 |

The report's example uses hostname configuration, disabling DNS lookup, password-encryption settings, a login banner, console and VTY line settings, interface descriptions, addressing and enabling interfaces. Secrets are omitted from this example.

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

These interface identifiers reproduce the Australia router example in the report. Confirm the actual device interface names before reusing commands.

## Switch configuration

The Australia switch example is SW-AU-IT. The report assigns VLAN 1 management address 10.30.2.2/28 and default gateway 10.30.2.1.

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

The report says the other switches follow the same general method with branch- and department-specific addressing.

## WAN interfaces and routing

- Six serial point-to-point links connect the four branch routers.
- WAN links use /30 subnets from 10.255.0.0/30 through 10.255.0.20/30.
- The WAN table identifies serial interfaces and a DCE clock rate of 128000.
- Chapter 3.5.2 specifies RIP on all routers; the Australia conclusion refers to RIP v2.

The report does not provide a complete consolidated router configuration for every branch in the command examples, so full configurations are not invented here.

## End-device addressing

The assignment states that DHCP is not used for the documented branch endpoint address plans. PCs, laptops, servers and access-point management interfaces use static addresses from their branch subnets. See [IP Addressing](ip-addressing.md).

## Verification commands

The report lists these commands for checking router and switch settings:

```text
show ip interface brief
show running-config
show interface status
```

These are the commands specified in the report; this document does not claim that fresh output has been collected.

## Configuration security

The source report contains router/switch passwords, FTP and IoT credentials, email passwords and wireless passphrases. They are deliberately excluded. Do not publish credentials in project documentation.

## Source

Based on Chapter 3.1–3.6 and the Australia router/switch configuration examples in the assignment.
