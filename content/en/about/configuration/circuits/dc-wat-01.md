---
title: "DC-WAT-01 — Watchkeeper — always-on"
description: "Owner-confirmed Ragtime house-bank feeder circuit"
circuit_id: "DC-WAT-01"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [House-bank supply diagram](/about/configuration/house-bank-distribution/)

> **Owner-reported circuit purpose; electrical installation not independently surveyed.** Owner-confirmed always-on feed; individual branch protection, exact loads and conductor size unverified.

| Field | Record |
| --- | --- |
| Circuit | `DC-WAT-01` |
| Source | [BB-003](/about/configuration/equipment/bb-003/) positive distribution |
| Function / destination | Watchkeeper essential low-power and monitoring systems (individual loads yet to be recorded) |
| Functional control | Unswitched by House/Autopilot remote controls |
| Installed branch fuse / breaker | **Unknown**; not inferred from historical engineering proposals |
| Source protection / isolation | **Unknown**; input connection to source and upstream protection not surveyed |
| Cable and return path | Conductor size, route, overcurrent coordination, negative return through the BMV-712 system-side shunt terminal **unverified** |

This circuit is a **functional link**, not evidence that a correctly rated protective device has been inspected. The service's switching state, its fusing and its protective role are independent properties. The unswitched circuits remain live while the House or Autopilot remotely switched feeds are OFF; do not interpret unswitched as unprotected.

## Outstanding physical inspection

Identify the fitted circuit protective device and rating, branch/feeder conductor cross-section, its DC panel or load endpoint, correct negative return via the [BMV-712 shunt](/about/configuration/equipment/eq-060/), and the controlling hardware where relevant.
