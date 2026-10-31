---
title: "DC-PWR-01 — House-bank source to positive distribution"
description: "Owner-confirmed Ragtime house-bank feeder circuit"
circuit_id: "DC-PWR-01"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [House-bank supply diagram](/about/configuration/house-bank-distribution/)

> **Owner-reported circuit purpose; electrical installation not independently surveyed.** Owner-confirmed source-to-positive bus topology; battery-post fuses owner-confirmed fitted, but their exact ratings/positions, isolation, conductor sizes and rated ampacity unverified.

| Field | Record |
| --- | --- |
| Circuit | `DC-PWR-01` |
| Source | [EQ-059](/about/configuration/equipment/eq-059/) house-bank positive source |
| Function / destination | [BB-003](/about/configuration/equipment/bb-003/) positive distribution feeding six functional services |
| Functional control | unspecified upstream source isolation; never assume the five downstream circuits are individually fused simply because they have five destinations |
| Installed branch fuse / breaker | **Battery-post MRBF fusing owner-confirmed fitted**; July 2025 design stated 2 × 125 A, current device markings not inspected |
| Source protection / isolation | Battery-post protection exists per owner; main isolation and fuse positions/values not physically surveyed |
| Cable and return path | Conductor size, route, overcurrent coordination, negative return through the BMV-712 system-side shunt terminal **unverified** |

This circuit is a **functional link**, not evidence that a correctly rated protective device has been inspected. The service's switching state, its fusing and its protective role are independent properties. The unswitched circuits remain live while the House or Autopilot remotely switched feeds are OFF; do not interpret unswitched as unprotected.

## Outstanding physical inspection

Identify the fitted circuit protective device and rating, branch/feeder conductor cross-section, its DC panel or load endpoint, correct negative return via the [BMV-712 shunt](/about/configuration/equipment/eq-060/), and the controlling hardware where relevant.
