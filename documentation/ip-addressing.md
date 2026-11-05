# IP Addressing Plan

This document consolidates the branch, device and WAN addressing information recorded in the submitted assignment. Values are reproduced as written; the Packet Tracer file has not been independently inspected to validate every entry.

## Branch address spaces

| Branch | Address space | Subnet mask used in the report |
|---|---|---|
| Malaysia | 10.10.x.x | 255.255.255.0 (/24) |
| Singapore | 10.20.x.x | 255.255.255.240 (/28) |
| Australia | 10.30.x.x | 255.255.255.240 (/28) |
| Japan | 10.40.x.x | 255.255.255.0 (/24) |

## Router gateway and server reference

| Branch | Department / purpose | Gateway or server address |
|---|---|---|
| Malaysia | Department LANs (device tables) | 10.10.1.1 |
| Malaysia | HQ / DNS server | 10.10.1.100 |
| Malaysia | Web server | 10.10.1.101 |
| Malaysia | Mail server | 10.10.1.102 |
| Singapore | Finance | 10.20.1.1 |
| Singapore | IT | 10.20.2.1 |
| Singapore | Administration | 10.20.3.1 |
| Singapore | Server room | 10.20.4.1 |
| Singapore | IoT / Web / DNS | 10.20.4.5 / 10.20.4.6 / 10.20.4.7 |
| Australia | Finance / IT / Administration / Server-IoT | 10.30.1.1 / 10.30.2.1 / 10.30.3.1 / 10.30.4.1 |
| Australia | Web-DNS / FTP / IoT gateway | 10.30.4.3 / 10.30.4.4 / 10.30.4.5 |
| Japan | Administration / HR / Finance / IT (branch interface table) | 10.40.1.1 / 10.40.2.1 / 10.40.3.1 / 10.40.4.1 |
| Japan | DNS / central email | 10.40.4.15 / 10.40.4.8 |

## Malaysia device addressing

All entries below use subnet mask 255.255.255.0 and default gateway 10.10.1.1, as shown in the report's device tables.

| Device | Interface | IP address |
|---|---|---|
| IT-PC1 | Fa0/2 | 10.10.1.160 |
| IT-PC2 | Fa0/3 | 10.10.1.161 |
| IT-Laptop1 | Wireless | 10.10.1.170 |
| IT-Laptop2 | Wireless | 10.10.1.171 |
| IT-SP1 | Wireless | 10.10.1.180 |
| IT-SP2 | Wireless | 10.10.1.181 |
| IT-Printer | Fa0/8 | 10.10.1.162 |
| FIN-PC1 | Fa0/2 | 10.10.1.110 |
| FIN-PC2 | Fa0/3 | 10.10.1.111 |
| FIN-Laptop1 | Wireless | 10.10.1.120 |
| FIN-Laptop2 | Wireless | 10.10.1.121 |
| FIN-SP1 | Wireless | 10.10.1.130 |
| FIN-SP2 | Wireless | 10.10.1.131 |
| FIN-Printer | Fa0/8 | 10.10.1.112 |
| ADM-PC1 | Fa0/2 | 10.10.1.60 |
| ADM-PC2 | Fa0/3 | 10.10.1.61 |
| ADM-Laptop1 | Wireless | 10.10.1.70 |
| ADM-Laptop2 | Wireless | 10.10.1.71 |
| ADM-SP1 | Wireless | 10.10.1.80 |
| ADM-SP2 | Wireless | 10.10.1.81 |
| ADM-Printer | Fa0/8 | 10.10.1.62 |
| HR-PC1 | Fa0/2 | 10.10.1.10 |
| HR-PC2 | Fa0/3 | 10.10.1.11 |
| HR-Laptop1 | Wireless | 10.10.1.23 |
| HR-Laptop2 | Wireless | 10.10.1.24 |
| HR-SP1 | Wireless | 10.10.1.30 |
| HR-SP2 | Wireless | 10.10.1.31 |
| HR-Printer | Fa0/8 | 10.10.1.12 |
| SRV-WEB | Fa0/2 | 10.10.1.101 |
| SRV-MAIL | Fa0/3 | 10.10.1.102 |
| SRV-HQ/DNS | Fa0/4 | 10.10.1.100 |

## Singapore device addressing

All entries use subnet mask 255.255.255.240. The default gateway is the first usable address of the department subnet as listed in the report.

| Device | Interface | IP address | Default gateway |
|---|---|---|---|
| IT PC1 | Fa0/3 | 10.20.2.3 | 10.20.2.1 |
| IT Laptop1 | Wireless | 10.20.2.4 | 10.20.2.1 |
| IT SP1 | Wireless | 10.20.2.5 | 10.20.2.1 |
| IT SP2 | Wireless | 10.20.2.6 | 10.20.2.1 |
| IT Printer1 | Fa0/4 | 10.20.2.7 | 10.20.2.1 |
| IT CAMERA | Wireless | 10.20.2.8 | 10.20.2.1 |
| IT RFID | Fa0/5 | 10.20.2.9 | 10.20.2.1 |
| IT Door | Fa0/6 | 10.20.2.11 | 10.20.2.1 |
| IT AC | Fa0/7 | 10.20.2.12 | 10.20.2.1 |
| Finance PC1 | Fa0/3 | 10.20.1.3 | 10.20.1.1 |
| Finance Laptop1 | Wireless | 10.20.1.4 | 10.20.1.1 |
| Finance Laptop2 | Wireless | 10.20.1.5 | 10.20.1.1 |
| Finance Laptop3 | Wireless | 10.20.1.6 | 10.20.1.1 |
| Finance AC | Fa0/7 | 10.20.1.7 | 10.20.1.1 |
| Finance SP1 | Wireless | 10.20.1.8 | 10.20.1.1 |
| Finance SP2 | Wireless | 10.20.1.9 | 10.20.1.1 |
| Finance SP3 | Wireless | 10.20.1.10 | 10.20.1.1 |
| Finance RFID | Fa0/5 | 10.20.1.11 | 10.20.1.1 |
| Finance CAMERA | Wireless | 10.20.1.12 | 10.20.1.1 |
| Finance Printer1 | Fa0/4 | 10.20.1.13 | 10.20.1.1 |
| Finance Door | Fa0/6 | 10.20.1.14 | 10.20.1.1 |
| ADNIN AC | Fa0/10 | 10.20.3.2 | 10.20.3.1 |
| ADMIN PC1 | Fa0/3 | 10.20.3.3 | 10.20.3.1 |
| ADMIN PC2 | Fa0/4 | 10.20.3.4 | 10.20.3.1 |
| ADMIN PC3 | Fa0/5 | 10.20.3.5 | 10.20.3.1 |
| ADMIN CAMERA | Wireless | 10.20.3.6 | 10.20.3.1 |
| ADMIN RFID | Fa0/6 | 10.20.3.7 | 10.20.3.1 |
| ADMIN SP1 | Wireless | 10.20.3.8 | 10.20.3.1 |
| ADMIN SP2 | Wireless | 10.20.3.9 | 10.20.3.1 |
| ADMIN SP3 | Wireless | 10.20.3.10 | 10.20.3.1 |
| ADMIN Printer1 | Fa0/8 | 10.20.3.11 | 10.20.3.1 |
| ADMIN Printer2 | Fa0/7 | 10.20.3.12 | 10.20.3.1 |
| ADMIN Tablet1 | Wireless | 10.20.3.13 | 10.20.3.1 |
| ADMIN Door | Fa0/9 | 10.20.3.14 | 10.20.3.1 |
| Server Door | Fa0/9 | 10.20.4.2 | 10.20.4.1 |
| Server AC | Fa0/2 | 10.20.4.3 | 10.20.4.1 |
| IoT Server | Fa0/5 | 10.20.4.5 | 10.20.4.1 |
| Web Server | Fa0/6 | 10.20.4.6 | 10.20.4.1 |
| DNS server | Fa0/7 | 10.20.4.7 | 10.20.4.1 |
| Server RFID | Fa0/8 | 10.20.4.8 | 10.20.4.1 |
| Server CAMERA | Fa0/10 | 10.20.4.9 | 10.20.4.1 |

## Australia device addressing

All entries use subnet mask 255.255.255.240. Each department gateway is the corresponding router interface address.

| Device | Interface | IP address | Default gateway |
|---|---|---|---|
| SW-AU-FIN | VLAN1 | 10.30.1.2 | 10.30.1.1 |
| Finance PC 1 | Fa0/3 | 10.30.1.3 | 10.30.1.1 |
| Finance PC 2 | Fa0/4 | 10.30.1.4 | 10.30.1.1 |
| Finance PC 3 | Fa0/5 | 10.30.1.5 | 10.30.1.1 |
| AP-AU-FIN | Mgmt | 10.30.1.6 | 10.30.1.1 |
| Finance Laptop 1 | WLAN | 10.30.1.7 | 10.30.1.1 |
| Finance Laptop 2 | WLAN | 10.30.1.8 | 10.30.1.1 |
| Finance Mobile 1 | WLAN | 10.30.1.9 | 10.30.1.1 |
| Finance Mobile 2 | WLAN | 10.30.1.10 | 10.30.1.1 |
| Finance Door | Fa0/6 | 10.30.1.11 | 10.30.1.1 |
| Finance RFID | Fa0/7 | 10.30.1.12 | 10.30.1.1 |
| Finance AC | Fa0/8 | 10.30.1.13 | 10.30.1.1 |
| Security Camera Finance | WLAN | 10.30.1.14 | 10.30.1.1 |
| SW-AU-IT | VLAN1 | 10.30.2.2 | 10.30.2.1 |
| IT PC 1 | Fa0/3 | 10.30.2.3 | 10.30.2.1 |
| IT PC 2 | Fa0/4 | 10.30.2.4 | 10.30.2.1 |
| IT PC 3 | Fa0/5 | 10.30.2.5 | 10.30.2.1 |
| AP-AU-IT | Mgmt | 10.30.2.6 | 10.30.2.1 |
| IT Laptop 1 | WLAN | 10.30.2.7 | 10.30.2.1 |
| IT Laptop 2 | WLAN | 10.30.2.8 | 10.30.2.1 |
| IT Mobile 1 | WLAN | 10.30.2.9 | 10.30.2.1 |
| IT Mobile 2 | WLAN | 10.30.2.10 | 10.30.2.1 |
| IT Door | Fa0/6 | 10.30.2.11 | 10.30.2.1 |
| IT RFID | Fa0/7 | 10.30.2.12 | 10.30.2.1 |
| IT AC | Fa0/8 | 10.30.2.13 | 10.30.2.1 |
| Security Camera IT | WLAN | 10.30.2.14 | 10.30.2.1 |
| SW-AU-SRV | VLAN1 | 10.30.4.2 | 10.30.4.1 |
| AU-WEB-SRV | NIC | 10.30.4.3 | 10.30.4.1 |
| AU-FTP-SRV | NIC | 10.30.4.4 | 10.30.4.1 |
| Home Gateway | NIC | 10.30.4.5 | 10.30.4.1 |
| Security Camera SRV | WLAN | 10.30.4.6 | 10.30.4.1 |
| Temperature Monitor | IoT WLAN | 10.30.4.7 | 10.30.4.1 |
| Smoke Detector | IoT WLAN | 10.30.4.8 | 10.30.4.1 |
| Humidity Sensor | IoT WLAN | 10.30.4.9 | 10.30.4.1 |
| CO2 Monitor | IoT WLAN | 10.30.4.10 | 10.30.4.1 |
| Server Door | Fa0/3 | 10.30.4.11 | 10.30.4.1 |
| Server RFID | Fa0/4 | 10.30.4.12 | 10.30.4.1 |
| Server AC | Fa0/5 | 10.30.4.13 | 10.30.4.1 |
| IoT Monitor PC (Mgmt) | Fa0/6 | 10.30.4.14 | 10.30.4.1 |

The source report's Australia device list for the IT department is duplicated in two tables; the entries above are listed once. The report's Finance/IT/Administration/Server-IoT router interface table lists all four /28 networks.

## Japan device addressing

The source tables show the following endpoint addressing. Subnet mask is 255.255.255.0 for all entries. DNS is 10.40.4.15 where shown.

| Device / department | IP address | Default gateway | DNS |
|---|---|---|---|
| Wired PC 1 – Finance | 10.40.3.3 | 10.40.3.1 | 10.40.4.15 |
| Wired Laptop 1 – Finance | 10.40.3.4 | 10.40.3.1 | 10.40.4.15 |
| Wired Laptop 2 – Finance | 10.40.3.5 | 10.40.3.1 | 10.40.4.15 |
| Wired Laptop 3 – Finance | 10.40.3.6 | 10.40.3.1 | 10.40.4.15 |
| Wired Laptop 4 – Finance | 10.40.3.8 | 10.40.3.1 | 10.40.4.15 |
| Wired Laptop 5 – Finance | 10.40.3.7 | 10.40.3.1 | 10.40.4.15 |
| Wireless Laptop 1 – Finance | 10.40.3.10 | 10.40.3.1 | 10.40.4.15 |
| Wireless PC 1 – Finance | 10.40.3.11 | 10.40.3.1 | 10.40.4.15 |
| WebCam IoT – Finance | 10.40.3.9 | 10.40.3.1 | 10.40.4.15 |
| Switch – IT | 10.40.4.2 | 10.40.4.1 | — |
| Wired Laptop 1 – IT | 10.40.4.3 | 10.40.4.1 | 10.40.4.15 |
| Wired Laptop 2 – IT | 10.40.4.4 | 10.40.4.1 | 10.40.4.15 |
| Printer – IT | 10.40.4.5 | 10.40.4.1 | 10.40.4.15 |
| DNS Server | 10.40.4.15 | 10.40.4.1 | 10.40.4.15 |
| Email Server | 10.40.4.8 | 10.40.4.1 | 10.40.4.15 |
| Wireless Laptop 1 – IT | 10.40.4.11 | 10.40.4.1 | 10.40.4.15 |
| Wireless Laptop 2 – IT | 10.40.4.12 | 10.40.4.1 | 10.40.4.15 |
| Wireless Laptop 3 – IT | 10.40.4.6 | 10.40.4.1 | 10.40.4.15 |
| Wireless Laptop 4 – IT | 10.40.4.7 | 10.40.4.1 | 10.40.4.15 |
| Tablet – IT | 10.40.4.9 | 10.40.4.1 | 10.40.4.15 |
| WebCam IoT – IT | 10.40.4.10 | 10.40.4.1 | 10.40.4.15 |
| Switch – Administration | 10.40.1.2 | 10.20.1.1 (as printed) | — |
| Wired Laptop 1 – Administration | 10.40.1.3 | 10.40.1.1 | 10.40.4.15 |
| Wired PC 1 – Administration | 10.40.1.4 | 10.40.1.1 | 10.40.4.15 |
| Wired PC 2 – Administration | 10.40.1.6 | 10.40.1.1 | 10.40.4.15 |
| Wired PC 3 – Administration | 10.40.1.5 | 10.40.1.1 | 10.40.4.15 |
| Printer – Administration | 10.40.1.7 | 10.40.1.1 | 10.40.4.15 |
| Wireless Laptop 1 – Administration | 10.40.1.8 | 10.40.1.1 | 10.40.4.15 |
| Wireless PC 1 – Administration | 10.40.1.10 | 10.40.1.1 | 10.40.4.15 |
| Wireless PC 2 – Administration | 10.40.1.9 | 10.40.1.1 | 10.40.4.15 |
| WebCam IoT – Administration | 10.40.1.11 | 10.40.1.1 | 10.40.4.15 |
| Switch – HR | 10.40.2.2 | 10.40.2.1 | — |
| Wired Laptop 1 – HR | 10.40.2.5 | 10.40.2.1 | 10.40.4.15 |
| Wired Laptop 2 – HR | 10.40.2.6 | 10.40.2.1 | 10.40.4.15 |
| Wired PC 1 – HR | 10.40.2.3 | 10.40.2.1 | 10.40.4.15 |
| Wired PC 2 – HR | 10.40.3.4 (as printed) | 10.40.2.1 | 10.40.4.15 |
| Wireless Laptop 1 – HR | 10.40.2.9 | 10.40.2.1 | 10.40.4.15 |
| Wireless Laptop 2 – HR | 10.40.2.8 | 10.40.2.1 | 10.40.4.15 |
| Wireless PC 1 – HR | 10.40.2.10 | 10.40.2.1 | 10.40.4.15 |
| WebCam IoT – HR | 10.40.2.7 | 10.40.2.1 | 10.40.4.15 |

The Japan source tables also include access points with an IP value shown as N/A. The Japan HR table prints one endpoint as 10.40.3.4, although the row is in the HR section; this is retained as printed pending verification. The Administration switch default gateway is printed as 10.20.1.1, which differs from the Japan router interface table.

## WAN point-to-point addressing

All six WAN links use subnet mask 255.255.255.252 (/30).

| Link | Router A interface / IP | Router B interface / IP | Subnet |
|---|---|---|---|
| Australia–Malaysia | Australia Serial2/0 — 10.255.0.1 | Malaysia Serial6/0 — 10.255.0.2 | 10.255.0.0/30 |
| Singapore–Japan | Singapore Serial6/0 — 10.255.0.5 | Japan Serial6/0 — 10.255.0.6 | 10.255.0.4/30 |
| Malaysia–Singapore | Malaysia Serial7/0 — 10.255.0.9 | Singapore Serial7/0 — 10.255.0.10 | 10.255.0.8/30 |
| Japan–Australia | Japan Serial7/0 — 10.255.0.13 | Australia Serial3/0 — 10.255.0.14 | 10.255.0.12/30 |
| Australia–Singapore | Australia Serial4/0 — 10.255.0.17 | Singapore Serial8/0 — 10.255.0.18 | 10.255.0.16/30 |
| Malaysia–Japan | Malaysia Serial8/0 — 10.255.0.21 | Japan Serial8/0 — 10.255.0.22 | 10.255.0.20/30 |

The report specifies DCE clock rate 128000 for each WAN serial link.

## Source inconsistencies requiring verification

Do not silently correct these values. Compare them with the Packet Tracer file before treating them as final:

- **Malaysia gateways:** Chapter 3.1 lists department gateway values such as 10.10.1.110, 10.10.1.160, 10.10.1.60 and 10.10.1.10, while the Malaysia device tables use 10.10.1.1 as the gateway.
- **Japan HR gateway:** the Japan router interface table gives 10.40.2.1, while Chapter 3.1 gives 10.40.3.1.
- **Japan Administration switch gateway:** the switch row in the endpoint table prints 10.20.1.1, while the Japan router interface table gives 10.40.1.1.
- **Japan HR endpoint:** one HR endpoint is printed as 10.40.3.4 in the HR device table.
- **Japan department subnet assignment:** the Japan router interface table maps Administration 10.40.1.0/24, HR 10.40.2.0/24, Finance 10.40.3.0/24 and IT 10.40.4.0/24.

## Routing note

The report's Chapter 3.5.2 names RIP, while the Australia conclusion specifies RIP v2 and another conclusion mentions static routing. No routing protocol is selected here as the verified final configuration. See [Network Configuration](network-configuration.md).

## Security note

The source report includes account names and passwords. Credentials, passwords, wireless keys and student IDs are deliberately excluded from this repository.

## Source

Based on the submitted assignment report's branch router/interface tables, endpoint IP tables, WAN addressing tables and Chapter 3 summaries.
