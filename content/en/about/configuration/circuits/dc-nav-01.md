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
| Switching and wiring | [SW-001](/about/configuration/equipment/sw-001/) DPDT switches **R3/brown and B4/white** of the 7 × 1.5 mm² Oceanflex trunk; forecabin-starboard-locker junction leads to **separate Oceanflex 2 × 1.5 mm² NASA mast cable**. Both wires polarity-reversible; individual mast-core-to-trunk matching not yet recorded. |
| Supply busbar, return path, cable size and length | Owner confirms **Oceanflex 7 × 1.5 mm² forecabin trunk** and **2 × 1.5 mm² NASA mast cable**. **No permanently negative lamp conductor**; supply polarity reverses via SW-001. Junction pin mapping and cable lengths untested. [Schedule](/about/configuration/dc-terminal-schedule/) |
| Provenance | Owner confirmation, 31 October 2026; any terminal references from earlier [DC Logical Circuits](/about/configuration/logical-circuits/) notes |

**Masthead function:** SW-001 reverses polarity to select tricolour versus anchor mode on **R3/brown and B4/white**, connecting to the two-core mast cable. The old **B2/blue and Y3/black** switch references are superseded historical evidence, not the current mapped pair. The actual selector contact truth table and individual mast cable core assignment remain untested.

## Remaining survey

Confirm breaker maker/DC voltage rating, terminal numbering through the DIN clamp blocks, conductor ampacity/size, return routing, voltage drop and physical device labels. Do not infer a cable size or protection suitability from the stated breaker rating.
