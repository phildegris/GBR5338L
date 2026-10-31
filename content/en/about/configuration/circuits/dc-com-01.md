---
title: "DC-COM-01 — COM-frame feeder"
circuit_id: "DC-COM-01"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [COM frame](/about/configuration/com-frame/)

**Owner-confirmed feeder, not independently traced.**

| Property | Value |
| --- | --- |
| Supply | [EQ-001](/about/configuration/equipment/eq-001/) main Moody DC panel |
| Protection | [CB-003](/about/configuration/equipment/cb-003/), **10 A**, physical `3,4`, label VHF AIS |
| Destination | [EQ-057](/about/configuration/equipment/eq-057/) four-way fuse board, `SL-COM` |
| Individual loads | VHF EQ-003, AIS EQ-004, SPL2000 EQ-005, each via its own as-yet-unknown fuse |
| Feeder cable and return | Gauge, length, terminations and upstream source unverified |

This circuit's CB-003 protection covers the **feeder** to EQ-057. The individual downstream branch fuses must be identified separately. Confirm feeder conductor sizing, actual breaker specification and protection coordination during the winter 2026–27 panel refit.
