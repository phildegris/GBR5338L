---
title: "DC-NAV-02 — Osculati combined fitting: steaming function"
description: "Owner-confirmed navigation and deck-light protected circuit"
circuit_id: "DC-NAV-02"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [Navigation-light topology](/about/configuration/navigation-lights/)

> **Owner-confirmed circuit function, not independently traced or measured.** Ragtime's original Moody NAV LTS breaker panel contains four 10 A breakers. This branch is physically position 2, labelled **STEAMING LIGHT** in the owner-supplied close-up. The 10 A rating comes from owner confirmation, not a visible breaker-body marking.

| Field | Record |
| --- | --- |
| Circuit ID | `DC-NAV-02` |
| Source | [EQ-002](/about/configuration/equipment/eq-002/) NAV LTS panel, upper-left of [EQ-001](/about/configuration/equipment/eq-001/) main DC panel |
| Primary circuit protection | [CB-002](/about/configuration/equipment/cb-002/) **10 A**, panel position 2 |
| Load | [EQ-020](/about/configuration/equipment/eq-020/) — Osculati combined fitting: steaming function |
| Switching and wiring | Panel **Y2 → yellow** Oceanflex 7 × 1.5 mm² trunk core to forecabin starboard-locker connectors; separate onward mast cable to Osculati lamp not yet traced. |
| Supply busbar, return path, cable size and length | Panel-to-forecabin **Oceanflex 7 × 1.5 mm²** owner-confirmed; onward mast cable, joins, return, total length unverified. [Schedule](/about/configuration/dc-terminal-schedule/) |
| Provenance | Owner confirmation, 31 October 2026; any terminal references from earlier [DC Logical Circuits](/about/configuration/logical-circuits/) notes |

**Owner-confirmed model:** **Osculati 13.243.88**, combined LED steaming/deck light. The product's published **yellow steaming-positive** pigtail has **not** been continuity-matched through the separate mast-going cable and forecabin junction to the **Y2/yellow Oceanflex distribution-trunk core**; leave this actual connection unverified.

**Shared physical housing:** This and the other Osculati circuit independently supply two functions of the **same EQ-020 combined steaming/deck fitting**, not two independent luminaires.

## Remaining survey

Confirm breaker maker/DC voltage rating, terminal numbering through the DIN clamp blocks, conductor ampacity/size, return routing, voltage drop and physical device labels. Do not infer a cable size or protection suitability from the stated breaker rating.
