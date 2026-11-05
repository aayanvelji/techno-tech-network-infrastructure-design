# Testing and Verification

## Purpose

This document provides a repeatable checklist for verifying the Techno Tech Packet Tracer network. It separates tests to perform from results actually observed.

**Current status:** No fresh independent Packet Tracer test results have been recorded in this repository. All test rows begin as **Not tested**. Update a row only after running the test in the supplied `.pkt` file.

## Test record

| Done? | Test area | What to verify | Suggested method / command | Result |
|---|---|---|---|---|
| ☐ | File opens | The original `FINAL_PRESENTATION.pkt` opens in Packet Tracer without an error. | Open the file in Packet Tracer. | Not tested |
| ☐ | Router interfaces | Required LAN and serial interfaces are present and operational. | On each router: `show ip interface brief`. | Not tested |
| ☐ | Switch interfaces | Expected switch ports and VLAN interfaces are operational. | On switches: `show interface status` and `show ip interface brief`. | Not tested |
| ☐ | Local LAN connectivity | Devices in the same branch/subnet can reach their default gateway. | From a representative endpoint, ping its configured gateway. | Not tested |
| ☐ | Inter-department routing | Devices in different department subnets at the same branch can communicate where permitted. | Ping between representative endpoints in different department subnets. | Not tested |
| ☐ | WAN links | Each of the six serial links can reach its directly connected peer address. | From each router, ping the peer serial IP. | Not tested |
| ☐ | Inter-branch routing | A representative endpoint in each branch can reach endpoints in other branches. | Run cross-branch pings in both directions. | Not tested |
| ☐ | Routing table | The configured routing protocol has installed the expected remote routes. | On each router: `show ip route`. | Not tested |
| ☐ | DNS | Clients can resolve the DNS records configured for the project. | Use the endpoint's DNS lookup tool or `nslookup` if available in the simulated host. | Not tested |
| ☐ | HTTP | The intended web server page can be opened from clients in the relevant branches. | Open the configured web server address/name in the simulated browser. | Not tested |
| ☐ | FTP | An authorised test client can connect to the FTP service and access permitted files. | Use the Packet Tracer FTP client with a test account; do not document passwords. | Not tested |
| ☐ | Email | Test accounts can send and receive a message through the configured mail service. | Send a test email between two project accounts. | Not tested |
| ☐ | IoT | IoT devices register/connect to the intended gateway or IoT service and report status. | Inspect IoT device and server/gateway status in Packet Tracer. | Not tested |
| ☐ | Wireless | Wireless clients can associate with the intended access point and reach their gateway. | Connect a test wireless endpoint and ping its gateway. | Not tested |

## How to record a result

For each test you perform:

1. Mark the checkbox only after completing the test.
2. Record the source and destination device names or addresses.
3. Record the actual result (for example, replies received, request timed out, DNS name resolved, or service unavailable).
4. If a test fails, record the error and the follow-up action. Do not mark it as passed until it succeeds.
5. Do not include passwords, wireless passphrases, student IDs or other secrets.

Example record format:

| Date | Test | Source → destination | Observed result | Status |
|---|---|---|---|---|
| YYYY-MM-DD | Example ping | Device A → gateway IP | Enter the actual output here | Pass / Fail |

## Items to resolve before final verification

The assignment contains inconsistent information that may affect the tests:

- RIP vs RIP v2 vs static routing descriptions.
- Malaysia department gateway values in Chapter 3.1 versus its device tables.
- Japan HR gateway value in Chapter 3.1 versus the branch interface table.
- Japan Administration switch gateway and one HR endpoint IP differ from the surrounding addressing plan.

Confirm these values against the actual Packet Tracer configuration before recording the corresponding test as passed.

## Verification commands referenced by the assignment

```text
show ip interface brief
show running-config
show interface status
show ip route
```

The commands above are useful checks; no command output or successful result is claimed here.
