---
title: "DC-WIN-01 — Windlass — common remotely switched supply"
description: "Windlass feed through Ragtime's common remote switch with retained 70 A breaker"
circuit_id: "DC-WIN-01"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [House-bank diagram](/about/configuration/house-bank-distribution/)

> **Owner-confirmed circuit and protection facts:** Windlass is on the same common **[SW-002](/about/configuration/equipment/sw-002/)** remote switch as House and Autopilot. A dedicated **70 A breaker [CB-006](/about/configuration/equipment/cb-006/)** was retained in the windlass feed. The original ANL and battery-post fuses were also fitted, but the present physical fuse ratings and series connections have not been inspected.

| Property | Recorded value |
| --- | --- |
| Circuit ID | `DC-WIN-01` |
| Source | House-bank distribution [BB-003](/about/configuration/equipment/bb-003/), via common [SW-002](/about/configuration/equipment/sw-002/) |
| Destination | **[EQ-061](/about/configuration/equipment/eq-061/) Lewmar HX1 800 W**, owner-confirmed installed; motor terminals and mechanical details not yet electrically surveyed |
| Contactor and controls | Separate windlass **[EQ-062](/about/configuration/equipment/eq-062/) contactor** controlled by **two foredeck switches [SW-003](/about/configuration/equipment/sw-003/) and [SW-004](/about/configuration/equipment/sw-004/)**; control direction allocation, cable colours, supply and protective fuse untraced |
| Confirmed protective device | **[CB-006](/about/configuration/equipment/cb-006/) 70 A circuit breaker**, retained and fitted |
| Additional protection | ANL fuse installation owner-confirmed; the [5 August 2025 design](/articles/technical/dc-distribution-panel/) specifies **100 A ANL Windlass**, **not independently read from a fitted fuse** |
| Original proposed cable | 25 mm², 10 m nominal windlass run in 2025 plan; actual fitted size/length unverified |
| Negative return | Must use system side of [BMV-712 shunt](/about/configuration/equipment/eq-060/) if supplied by house bank; actual path untraced |

## Evidence and protection coordination

The owner has **now confirmed both** the historical ANL/battery-post fuse installation **and retention of the 70 A windlass breaker**. Earlier July 2025 discussions cited the 70 A breaker for local isolation. The August 2025 article proposed a 100 A ANL windlass feed. There is no basis to treat the two devices as mutually exclusive.

Until checked aboard, **do not claim** their precise series order, fuse class/rating, conductor protection adequacy or selective tripping. Keep windlass on the one common remote-switched side, not a dedicated second switch.

## Current owner-confirmed windlass configuration

**1 November 2026:** The installed windlass is specifically **Lewmar HX1 800 W**. The dedicated circuit breaker is **70 A**. A **separate contactor** switches the windlass motor and is operated by **two physical switches on the foredeck**. The two switches are documented as individually identified controls, but which is UP and DOWN and whether any other control stations exist remain unverified. The earlier **80 A breaker** reference was incorrect and is superseded by the owner's 70 A confirmation.

The Lewmar HX1 manufacturer's manual identifies a **70 A supplied breaker (68000240)**, **contactor 68000939** and a **3 A control circuit fuse** in its standard wiring scheme. These part numbers and control fuse are *manufacturer references*, **not proof those exact accessory parts or fuse ratings are fitted** aboard Ragtime. [Windlass equipment](/about/configuration/equipment/eq-061/) · [Contactor](/about/configuration/equipment/eq-062/) · [Controls](/about/configuration/equipment/sw-003/), [SW-004](/about/configuration/equipment/sw-004/).

## Next inspection

Confirm windlass motor/controller, 70 A breaker location and part markings, relevant ANL fuse holder and markings, cable sizes, negative return and the switched-output branch point.
