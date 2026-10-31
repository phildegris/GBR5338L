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
| Switching and wiring | Via SW-001 DPDT centre-off polarity selector; legacy B2 blue and Y3 black conductors. |
| Supply busbar, return path, cable size and length | Not independently inspected |
| Provenance | Owner confirmation, 31 October 2026; any terminal references from earlier [DC Logical Circuits](/about/configuration/logical-circuits/) notes |

**Masthead function:** SW-001 reverses polarity to select the tricolour or anchor mode of one combined NASA light. The old switch terminal numbers and lamp polarity direction remain untested.

## Remaining survey

Confirm breaker maker/DC voltage rating, terminal numbering through the DIN clamp blocks, conductor ampacity/size, return routing, voltage drop and physical device labels. Do not infer a cable size or protection suitability from the stated breaker rating.
