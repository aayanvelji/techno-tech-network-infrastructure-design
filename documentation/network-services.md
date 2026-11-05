# Network Services

This document summarises services and device roles described in Chapter 3 of the Techno Tech assignment. Details are based on the report and are not a claim of independent service testing.

## DNS

| Branch | DNS address |
|---|---|
| Malaysia | 10.10.1.100 (HQ/DNS server) |
| Singapore | 10.20.4.7 |
| Australia | 10.30.4.3 (shared with the web server) |
| Japan | 10.40.4.15 |

The Australia example enables DNS and adds A records including www.technotech.au pointing to 10.30.4.3 and ftp.technotech.au pointing to 10.30.4.4.

## HTTP / Web

The Australia web server is listed at 10.30.4.3/28 with gateway 10.30.4.1. The documented procedure enables HTTP and edits the default page to show a Techno Tech Australia page. Malaysia's web server is listed at 10.10.1.101 and Singapore's at 10.20.4.6.

## FTP

The Australia FTP server is listed at 10.30.4.4/28 with gateway 10.30.4.1. The report's procedure enables FTP and adds a test file named technotech.txt. Credentials are not reproduced.

## Centralised email

The assignment places the central email server in Japan at 10.40.4.8, with DNS at 10.40.4.15 and the domain technotech.com. The procedure enables the email service, configures the domain, creates user accounts and describes sending and receiving a test message. Account passwords are excluded.

The task allocation identifies Aayan Velji as responsible for the Japan branch's local DNS, centralised email server for all branches, email-server configuration and account creation.

## IoT services and devices

### Singapore

The Singapore server room contains an IoT server listed at 10.20.4.5. The report describes cameras, air conditioners, RFID card readers and IoT doors. It documents a rule where a valid configured card-reader value unlocks the door and an invalid value leaves it locked, and describes checking device connectivity to the server.

### Australia

The Australia IoT gateway is listed at 10.30.4.5. The report identifies a temperature monitor, smoke detector, humidity sensor and CO2 monitor, as well as security cameras and building-control devices. The procedure describes registering devices with the gateway and checking their status in its dashboard.

## Wireless access points

The assignment describes separate wireless network names for departments, protected with WPA2-PSK. Australia uses departmental SSIDs for Finance, IT and Administration and an optional IoT SSID. Singapore, Japan and Malaysia also have separate department SSIDs. Wireless passphrases are deliberately excluded from this repository.

## End devices

The report describes configuring wired PCs with static IP details and connecting wireless laptops and mobile devices to the appropriate departmental SSID. Devices use the IP address, subnet mask, gateway and DNS settings specified for their branch.

## Source

Based on Chapter 3.1 and sections 3.4.1–3.4.6 of the submitted assignment. Passwords, account credentials and wireless keys have been omitted.
