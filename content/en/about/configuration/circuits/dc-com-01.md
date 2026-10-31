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
| Protected branches | [DC-COM-02](/about/configuration/circuits/dc-com-02/) via [FU-001](/about/configuration/equipment/fu-001/) (**10 A VHF**); [DC-COM-03](/about/configuration/circuits/dc-com-03/) via [FU-002](/about/configuration/equipment/fu-002/) (**3 A SPL2000**); [DC-COM-04](/about/configuration/circuits/dc-com-04/) via [FU-003](/about/configuration/equipment/fu-003/) (**3 A ATB1**) |
| Feeder cable and return | Gauge, length, terminations and upstream source unverified |

This circuit's CB-003 protection covers the **feeder** to EQ-057. The individual downstream branch fuses are now identified as FU-001–FU-003 (ways 1–3), with ratings 10 A / 3 A / 3 A; their conductors and characteristics still require survey. Confirm feeder conductor sizing, actual breaker specification and protection coordination during the winter 2026–27 panel refit.
