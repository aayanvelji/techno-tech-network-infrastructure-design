# WAN Architecture

The assignment specifies a full-mesh WAN connecting Malaysia, Singapore, Australia and Japan. Four routers are joined by six serial point-to-point links. WAN addressing uses 10.255.0.x with /30 masks (255.255.255.252).

| Link | End A | End B | Subnet |
|---|---|---|---|
| 1 | Australia R-AU Serial2/0 — 10.255.0.1 | Malaysia Router0 Serial6/0 — 10.255.0.2 | 10.255.0.0/30 |
| 2 | Singapore MainrouterSingapore Serial6/0 — 10.255.0.5 | Japan Router Serial6/0 — 10.255.0.6 | 10.255.0.4/30 |
| 3 | Malaysia Router0 Serial7/0 — 10.255.0.9 | Singapore MainrouterSingapore Serial7/0 — 10.255.0.10 | 10.255.0.8/30 |
| 4 | Japan Router Serial7/0 — 10.255.0.13 | Australia R-AU Serial3/0 — 10.255.0.14 | 10.255.0.12/30 |
| 5 | Australia R-AU Serial4/0 — 10.255.0.17 | Singapore MainrouterSingapore Serial8/0 — 10.255.0.18 | 10.255.0.16/30 |
| 6 | Malaysia Router0 Serial8/0 — 10.255.0.21 | Japan Router Serial8/0 — 10.255.0.22 | 10.255.0.20/30 |

All links use 255.255.255.252. Their broadcast addresses, in link order, are 10.255.0.3, 10.255.0.7, 10.255.0.11, 10.255.0.15, 10.255.0.19 and 10.255.0.23. The DCE clock-rate table specifies 128000 for each serial connection; identify the DCE end before setting it.

## Routing

Chapter 3.5.2 states that RIP was selected and configured on all routers. The Australia conclusion specifically refers to RIP v2. A separate conclusion mentions static routing, so the report contains differing references; the explicit WAN configuration section identifies RIP.

## Source

Based on Chapter 2, WAN addressing tables and Chapter 3.5 of the assignment. These values are reproduced from the report, not from a fresh connectivity test.
