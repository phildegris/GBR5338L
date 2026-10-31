---
title: "DC-NAV-04 — Osculati bow bicolour LED and stern LED"
description: "Owner-confirmed navigation and deck-light protected circuit"
circuit_id: "DC-NAV-04"
date: 2026-10-31
---

[← Circuit Register](/about/configuration/circuit-register/) · [Navigation-light topology](/about/configuration/navigation-lights/)

> **Owner-confirmed circuit function, not independently traced or measured.** Ragtime's original Moody NAV LTS breaker panel contains four 10 A breakers. This branch is physically position 4, labelled **NAVIGATION LIGHTS** in the owner-supplied close-up. The 10 A rating comes from owner confirmation, not a visible breaker-body marking.

| Field | Record |
| --- | --- |
| Circuit ID | `DC-NAV-04` |
| Source | [EQ-002](/about/configuration/equipment/eq-002/) NAV LTS panel, upper-left of [EQ-001](/about/configuration/equipment/eq-001/) main DC panel |
| Primary circuit protection | [CB-005](/about/configuration/equipment/cb-005/) **10 A**, panel position 4 |
| Load | [EQ-018](/about/configuration/equipment/eq-018/) and [EQ-019](/about/configuration/equipment/eq-019/) — Osculati bow bicolour LED and stern LED |
| Switching and wiring | Handwritten **B3 → green** Oceanflex 7 × 1.5 mm² trunk core for bow; **B1** also stern-light-labelled (first abbreviation unclear). CB-005 protects both luminaires per owner, but full wiring routes, branch point and returns untraced. |
| Supply busbar, return path, cable size and length | Bow panel-to-forecabin branch uses **Oceanflex 7 × 1.5 mm²** owner-confirmed trunk; stern route may be separate and is unknown. [Schedule](/about/configuration/dc-terminal-schedule/) |
| Provenance | Owner confirmation, 31 October 2026; any terminal references from earlier [DC Logical Circuits](/about/configuration/logical-circuits/) notes |

**Shared breaker:** One 10 A breaker feeds *both* bow and stern luminaires. The branch point and individual return arrangement are unknown.

## Remaining survey

Confirm breaker maker/DC voltage rating, terminal numbering through the DIN clamp blocks, conductor ampacity/size, return routing, voltage drop and physical device labels. Do not infer a cable size or protection suitability from the stated breaker rating.
