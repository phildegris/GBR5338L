---
title: "DC-COM-02 — Icom M510 VHF power"
description: "COM-frame protected branch from fuse way 1 to Icom M510 VHF"
circuit_id: "DC-COM-02"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [COM-frame diagram](/about/configuration/com-frame/) · [Fuse equipment](/about/configuration/equipment/fu-001/)

> **Owner-confirmed branch assignment and fuse rating.** The physical conductor, terminations and return path have not been independently surveyed.

| Field | Value |
| --- | --- |
| Circuit identifier | **`DC-COM-02`** |
| Source | [EQ-057](/about/configuration/equipment/eq-057/) four-way fuse board on the COM frame |
| Primary branch protection | **[FU-001](/about/configuration/equipment/fu-001/)**, **10 A**, **fuse position 1** |
| Load | **[EQ-003](/about/configuration/equipment/eq-003/)** — Icom M510 VHF |
| Upstream feeder | [DC-COM-01](/about/configuration/circuits/dc-com-01/), protected by [CB-003](/about/configuration/equipment/cb-003/) **10 A** |
| Branch conductor/return | Type, cross-section, length, termination and routing not yet confirmed |
| Evidence status | Owner-confirmed load, fuse way and ampere rating; wiring not independently traced |

**Protected circuit:** This fuse protects the conductor from position 1 of EQ-057 to Icom M510 VHF. The upstream 10 A CB-003 feeder protection is separate.

**Coordination note:** The 10 A VHF branch fuse and upstream 10 A feeder breaker share a nominal current rating. This does not prove selectivity; confirm breaker and fuse time-current characteristics and the relevant cable sizes at refit.

## Remaining survey

Identify the fuse format and its actual characteristics; inspect conductor gauge, polarity, route, termination and return path before declaring the installation independently verified.
