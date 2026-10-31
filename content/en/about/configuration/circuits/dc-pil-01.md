---
title: "DC-PIL-01 — Autopilot — remotely switched supply"
description: "Owner-confirmed Ragtime house-bank feeder circuit"
circuit_id: "DC-PIL-01"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [House-bank supply diagram](/about/configuration/house-bank-distribution/)

> **Owner-reported circuit purpose; electrical installation not independently surveyed.** Owner-confirmed separate **Autopilot supply circuit**, but controlled **together with House and Windlass** by the **one common remote switch SW-002**. Breaker/fuse rating and downstream wiring unverified.

| Field | Record |
| --- | --- |
| Circuit | `DC-PIL-01` |
| Source | [BB-003](/about/configuration/equipment/bb-003/) positive distribution |
| Function / destination | Autopilot distribution: NAC-3 and steering drive related equipment, protected subcircuits not yet allocated |
| Functional control | **[SW-002](/about/configuration/equipment/sw-002/) common remote switch**, simultaneously controlling Autopilot, House and Windlass; **NOT independent remote isolation** |
| Installed branch fuse / breaker | **Original ANL fusing installed per owner**, precise branch allocation and nominal value not independently verified |
| Source protection / isolation | **Unknown**; input connection to source and upstream protection not surveyed |
| Cable and return path | Conductor size, route, overcurrent coordination, negative return through the BMV-712 system-side shunt terminal **unverified** |

This circuit is a **functional link**, not evidence that a correctly rated protective device has been inspected. The service's switching state, its fusing and its protective role are independent properties. The unswitched circuits remain live while the common SW-002 House/Autopilot/Windlass switch is OFF; do not interpret unswitched as unprotected.

## Outstanding physical inspection

Identify the fitted circuit protective device and rating, branch/feeder conductor cross-section, its DC panel or load endpoint, correct negative return via the [BMV-712 shunt](/about/configuration/equipment/eq-060/), and the controlling hardware where relevant.
