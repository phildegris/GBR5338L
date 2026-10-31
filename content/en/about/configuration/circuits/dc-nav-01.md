---
title: "DC-NAV-01 — NASA Combi masthead tricolour/anchor LED"
description: "Owner-confirmed navigation and deck-light protected circuit"
circuit_id: "DC-NAV-01"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [Navigation-light topology](/about/configuration/navigation-lights/)

> **Owner-confirmed circuit function, not independently traced or measured.** Ragtime's original Moody NAV LTS breaker panel contains four 10 A breakers. This branch is physically position 1, labelled **MAST HEAD LIGHT** in the owner-supplied close-up. The 10 A rating comes from owner confirmation, not a visible breaker-body marking.

| Field | Record |
| --- | --- |
| Circuit ID | `DC-NAV-01` |
| Source | [EQ-002](/about/configuration/equipment/eq-002/) NAV LTS panel, upper-left of [EQ-001](/about/configuration/equipment/eq-001/) main DC panel |
| Primary circuit protection | [CB-001](/about/configuration/equipment/cb-001/) **10 A**, panel position 1 |
| Load | [EQ-021](/about/configuration/equipment/eq-021/) — NASA Combi masthead tricolour/anchor LED |
| Switching and wiring | Original switch [SW-001](/about/configuration/equipment/sw-001/); **B2 → blue** and **Y3 → black** cores in **Oceanflex seven-core trunk to forecabin locker**. Older DPDT notes call Y3 a NASA light wire while handwritten CB column says `NC`; neither statement establishes the exact switched return or onward mast leg. |
| Supply busbar, return path, cable size and length | Owner confirms upstream **Oceanflex 7 × 1.5 mm²** trunk to forecabin locker; onward mast cable/returns/total length not traced. [Schedule](/about/configuration/dc-terminal-schedule/) |
| Provenance | Owner confirmation, 31 October 2026; any terminal references from earlier [DC Logical Circuits](/about/configuration/logical-circuits/) notes |

**Masthead function:** SW-001 reverses polarity to select the tricolour or anchor mode of one combined NASA light. The old switch terminal numbers and lamp polarity direction remain untested.

## Remaining survey

Confirm breaker maker/DC voltage rating, terminal numbering through the DIN clamp blocks, conductor ampacity/size, return routing, voltage drop and physical device labels. Do not infer a cable size or protection suitability from the stated breaker rating.
