---
title: "DC-NAV-03 — Osculati combined fitting: deck function"
description: "Owner-confirmed navigation and deck-light protected circuit"
circuit_id: "DC-NAV-03"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [Navigation-light topology](/about/configuration/navigation-lights/)

> **Owner-confirmed circuit function, not independently traced or measured.** Ragtime's original Moody NAV LTS breaker panel contains four 10 A breakers. This branch is physically position 3, labelled **DECK LIGHTS** in the owner-supplied close-up. The 10 A rating comes from owner confirmation, not a visible breaker-body marking.

| Field | Record |
| --- | --- |
| Circuit ID | `DC-NAV-03` |
| Source | [EQ-002](/about/configuration/equipment/eq-002/) NAV LTS panel, upper-left of [EQ-001](/about/configuration/equipment/eq-001/) main DC panel |
| Primary circuit protection | [CB-004](/about/configuration/equipment/cb-004/) **10 A**, panel position 3 |
| Load | [EQ-020](/about/configuration/equipment/eq-020/) — Osculati combined fitting: deck function |
| Switching and wiring | Separate supply from steaming light; actual DIN terminals and wire colour unrecorded. |
| Supply busbar, return path, cable size and length | Not independently inspected |
| Provenance | Owner confirmation, 31 October 2026; any terminal references from earlier [DC Logical Circuits](/about/configuration/logical-circuits/) notes |

**Shared physical housing:** This and the other Osculati circuit independently supply two functions of the **same EQ-020 combined steaming/deck fitting**, not two independent luminaires.

## Remaining survey

Confirm breaker maker/DC voltage rating, terminal numbering through the DIN clamp blocks, conductor ampacity/size, return routing, voltage drop and physical device labels. Do not infer a cable size or protection suitability from the stated breaker rating.
