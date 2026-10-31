---
title: "DC-COM-03 — Digital Yacht SPL2000 power"
description: "COM-frame protected branch from fuse way 2 to Digital Yacht SPL2000"
circuit_id: "DC-COM-03"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [COM-frame diagram](/about/configuration/com-frame/) · [Fuse equipment](/about/configuration/equipment/fu-002/)

> **Owner-confirmed branch assignment and fuse rating.** The physical conductor, terminations and return path have not been independently surveyed.

| Field | Value |
| --- | --- |
| Circuit identifier | **`DC-COM-03`** |
| Source | [EQ-057](/about/configuration/equipment/eq-057/) four-way fuse board on the COM frame |
| Primary branch protection | **[FU-002](/about/configuration/equipment/fu-002/)**, **3 A**, **fuse position 2** |
| Load | **[EQ-005](/about/configuration/equipment/eq-005/)** — Digital Yacht SPL2000 |
| Upstream feeder | [DC-COM-01](/about/configuration/circuits/dc-com-01/), protected by [CB-003](/about/configuration/equipment/cb-003/) **10 A** |
| Branch conductor/return | Type, cross-section, length, termination and routing not yet confirmed |
| Evidence status | Owner-confirmed load, fuse way and ampere rating; wiring not independently traced |

**Protected circuit:** This fuse protects the conductor from position 2 of EQ-057 to Digital Yacht SPL2000. The upstream 10 A CB-003 feeder protection is separate.

## Remaining survey

Identify the fuse format and its actual characteristics; inspect conductor gauge, polarity, route, termination and return path before declaring the installation independently verified.
