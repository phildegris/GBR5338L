---
title: "DC-WIN-01 — Windlass — common remotely switched supply"
description: "Windlass feed through Ragtime's common remote switch with retained 80 A breaker"
circuit_id: "DC-WIN-01"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [House-bank diagram](/about/configuration/house-bank-distribution/)

> **Owner-confirmed circuit and protection facts:** Windlass is on the same common **[SW-002](/about/configuration/equipment/sw-002/)** remote switch as House and Autopilot. A dedicated **80 A breaker [CB-006](/about/configuration/equipment/cb-006/)** was retained in the windlass feed. The original ANL and battery-post fuses were also fitted, but the present physical fuse ratings and series connections have not been inspected.

| Property | Recorded value |
| --- | --- |
| Circuit ID | `DC-WIN-01` |
| Source | House-bank distribution [BB-003](/about/configuration/equipment/bb-003/), via common [SW-002](/about/configuration/equipment/sw-002/) |
| Destination | Windlass feed; exact motor/controller model and physical terminals not independently identified |
| Confirmed protective device | **[CB-006](/about/configuration/equipment/cb-006/) 80 A circuit breaker**, retained and fitted |
| Additional protection | ANL fuse installation owner-confirmed; the [5 August 2025 design](/articles/technical/dc-distribution-panel/) specifies **100 A ANL Windlass**, **not independently read from a fitted fuse** |
| Original proposed cable | 25 mm², 10 m nominal windlass run in 2025 plan; actual fitted size/length unverified |
| Negative return | Must use system side of [BMV-712 shunt](/about/configuration/equipment/eq-060/) if supplied by house bank; actual path untraced |

## Evidence and protection coordination

The owner has **now confirmed both** the historical ANL/battery-post fuse installation **and retention of the 80 A windlass breaker**. Earlier July 2025 discussions cited the 80 A breaker for local isolation. The August 2025 article proposed a 100 A ANL windlass feed. There is no basis to treat the two devices as mutually exclusive.

Until checked aboard, **do not claim** their precise series order, fuse class/rating, conductor protection adequacy or selective tripping. Keep windlass on the one common remote-switched side, not a dedicated second switch.

## Next inspection

Confirm windlass motor/controller, 80 A breaker location and part markings, relevant ANL fuse holder and markings, cable sizes, negative return and the switched-output branch point.
