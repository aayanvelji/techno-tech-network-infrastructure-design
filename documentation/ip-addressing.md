# IP Addressing Plan

This document consolidates the branch and WAN addressing information in the assignment. Values are reproduced from its tables and Chapter 3 summary; they have not been independently corrected against the Packet Tracer simulation.

## Branch address spaces

| Branch | Address space | Subnet approach |
|---|---|---|
| Malaysia | 10.10.x.x | 10.10.1.x with 255.255.255.0 (/24) in device tables |
| Singapore | 10.20.x.x | Four /28 subnets |
| Australia | 10.30.x.x | Four /28 subnets |
| Japan | 10.40.x.x | Four /24 subnets |

## Malaysia

The device tables use 10.10.1.x, mask 255.255.255.0 and gateway 10.10.1.1. Listed servers: HQ/DNS 10.10.1.100, web 10.10.1.101 and mail 10.10.1.102. Chapter 3.1 lists department gateway values Finance 10.10.1.110, IT 10.10.1.160, Administration 10.10.1.60 and HR 10.10.1.10; detailed device tables instead use 10.10.1.1 as gateway. Both source references are retained here.

## Singapore — mask 255.255.255.240 (/28)

| Area | Network | Gateway | Broadcast |
|---|---|---|---|
| Finance | 10.20.1.0/28 | 10.20.1.1 | 10.20.1.15 |
| IT | 10.20.2.0/28 | 10.20.2.1 | 10.20.2.15 |
| Administration | 10.20.3.0/28 | 10.20.3.1 | 10.20.3.15 |
| Server Room | 10.20.4.0/28 | 10.20.4.1 | 10.20.4.15 |

Listed services: IoT 10.20.4.5, web 10.20.4.6 and DNS 10.20.4.7.

## Australia — mask 255.255.255.240 (/28)

| Area | Network | Gateway | Broadcast |
|---|---|---|---|
| Finance | 10.30.1.0/28 | 10.30.1.1 | 10.30.1.15 |
| IT | 10.30.2.0/28 | 10.30.2.1 | 10.30.2.15 |
| Administration | 10.30.3.0/28 | 10.30.3.1 | 10.30.3.15 |
| Server Room / IoT | 10.30.4.0/28 | 10.30.4.1 | 10.30.4.15 |

Listed infrastructure: switch management addresses 10.30.1.2, 10.30.2.2 and 10.30.4.2; web/DNS 10.30.4.3; FTP 10.30.4.4; IoT gateway 10.30.4.5.

## Japan — mask 255.255.255.0 (/24)

| Department | Network | Gateway in branch interface table |
|---|---|---|
| Administration | 10.40.1.0/24 | 10.40.1.1 |
| HR | 10.40.2.0/24 | 10.40.2.1 |
| Finance | 10.40.3.0/24 | 10.40.3.1 |
| IT | 10.40.4.0/24 | 10.40.4.1 |

Listed servers: DNS 10.40.4.15 and central email 10.40.4.8. Chapter 3.1 instead lists the HR gateway as 10.40.3.1, which conflicts with the Japan branch interface table. The table mapping is shown above and the difference is not silently corrected.

## WAN point-to-point addressing

All links use 255.255.255.252 (/30).

| Link | Subnet | Usable endpoints | Broadcast |
|---|---|---|---|
| Australia–Malaysia | 10.255.0.0/30 | 10.255.0.1–10.255.0.2 | 10.255.0.3 |
| Singapore–Japan | 10.255.0.4/30 | 10.255.0.5–10.255.0.6 | 10.255.0.7 |
| Malaysia–Singapore | 10.255.0.8/30 | 10.255.0.9–10.255.0.10 | 10.255.0.11 |
| Japan–Australia | 10.255.0.12/30 | 10.255.0.13–10.255.0.14 | 10.255.0.15 |
| Australia–Singapore | 10.255.0.16/30 | 10.255.0.17–10.255.0.18 | 10.255.0.19 |
| Malaysia–Japan | 10.255.0.20/30 | 10.255.0.21–10.255.0.22 | 10.255.0.23 |

The report specifies DCE clock rate 128000 for each WAN serial link. It states that DHCP is not used for the branch endpoint addressing; static addressing is used. Passwords, account credentials and wireless keys are not included.

## Source

Based on the branch IP tables and Chapter 3.1 of the submitted assignment report. Where the report gives conflicting values, the differences are explicitly identified.
