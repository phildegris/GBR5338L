---
title: "Navigation and deck-light circuits"
description: "Owner-confirmed original Moody 336 NAV LTS breaker and lighting topology"
date: 2026-10-31
summary: "Four 10A breakers, NASA combined masthead tricolour/anchor LED, Osculati combined steaming/deck lamp, bow bicolour and stern LED."
---

[← Electrical configuration](/about/configuration/) · [Equipment Register](/about/configuration/equipment-register/) · [Circuit Register](/about/configuration/circuit-register/)

> **Evidence: four breaker functions and 10 A ratings owner-confirmed (31 October 2026), but electrical wiring and breaker body markings not independently inspected.** The photograph shows four labelled controls in the upper-left NAV LTS assembly of the original Moody 336 DC panel.

## Functional DC distribution

{{< nav-distribution id="nav_lights" >}}

The **NAV LTS panel** is [EQ-002](/about/configuration/equipment/eq-002/), part of main Moody DC panel [EQ-001](/about/configuration/equipment/eq-001/). The yacht-outline mimic and its indicator dots are present on the faceplate, but their actual status feedback/illumination circuit has not been verified.

## Confirmed equipment functions

- **Masthead:** [CB-001](/about/configuration/equipment/cb-001/), 10 A, feeds [SW-001](/about/configuration/equipment/sw-001/) DPDT On-Off-On polarity-reversing selector. It supplies one [NASA Marine Combi LED](/about/configuration/equipment/eq-021/) tricolour/anchor light at the masthead. Centre-off disables both; polarity reversal selects a mode; **the switch pinout and exact polarity mapping have not been independently tested**.
- **Steaming:** [CB-002](/about/configuration/equipment/cb-002/), 10 A, feeds the steaming (forward white) function of one [Osculati combined masthead/deck fixture](/about/configuration/equipment/eq-020/). Legacy notes name terminal **Y2** on the DIN block and a **yellow** conductor in the seven-core mast cable.
- **Deck:** [CB-004](/about/configuration/equipment/cb-004/), 10 A, separately feeds the deck floodlight function of **that same EQ-020 Osculati housing**, not a second fixture. The deck-feed DIN terminal and conductor colour are still unknown.
- **Bow and stern:** [CB-005](/about/configuration/equipment/cb-005/), 10 A, feeds [Osculati bow bicolour LED](/about/configuration/equipment/eq-018/) and [Osculati stern LED](/about/configuration/equipment/eq-019/) together. Their branch point, return path and DIN clamp assignments have not been traced.

The owner confirms all four branches run through the original **DIN-rail mounted colour-coded clamp connector blocks** described in the [legacy DC Logical Circuits](/about/configuration/logical-circuits/), without establishing the exact clamp positions for all four circuits.

## Legacy terminal notes, retained as references

| Historical reference | Reported function | Status |
| --- | --- | --- |
| Breaker 1,1 | Masthead to DPDT selector | Owner confirms function and 10 A breaker; physical terminal alias retained |
| Selector pins 1–6 | Polarity-reversing masthead supply | Legacy pin notes only; contact map not independently tested |
| B2, blue seven-core mast conductor | One side of NASA masthead lamp | Legacy notes; no continuity measurement |
| Y3, black seven-core mast conductor | Other side of NASA masthead lamp | Legacy notes; no continuity measurement |
| Breaker 1,2 → Y2, yellow mast conductor | Steaming function of Osculati fixture | Legacy field notes; no continuity measurement |
| CB-004 / CB-005 downstream DIN positions | Deck and bow/stern feeds | Not recorded, rather than guessed |

## Manufacturer references (models not independently matched)

- [NASA Marine Supernova Combi product](https://www.nasamarine.com/product/supernova-combi-tri-and-anchor-l-e-d-mastlight/) and [original fitting instructions (PDF)](https://www.nasamarine.com/wp-content/uploads/2015/12/Super-Nova.pdf) explain a **two-wire polarity-reversing tricolour/anchor arrangement**, consistent with Ragtime's NASA Combi. The installed suffix/revision is not independently confirmed.
- [Osculati product catalogue](https://www.osculati.com/en/page/catalogues) contains combined steaming/deck light variants. **Do not adopt a specific model's current, mounting dimensions or wiring-colour codes** until the fitted Osculati product code is identified.

**Important protection question:** NASA's published Supernova Combi instructions call for a **1 A fuse**. Ragtime's confirmed feeder is an older **10 A panel breaker**. We do not yet know whether a smaller local fuse is fitted, what cross-section is protected, or the exact installed NASA variant. This is a **survey/coordination item**, not a conclusion that the installation is unsafe or noncompliant.

## Outstanding onboard survey

Confirm the exact NASA and Osculati part numbers; photograph breaker side labels (10 A currently owner-reported); trace Y2/B2/Y3 and the other colour-coded DIN clamps; identify wire cross-sections and returns; check the SW-001 polarity truth table and if any local downstream fuse exists. Retain [EQ-022](/about/configuration/equipment/eq-022/) only as a legacy grouped heading until we know whether any additional deck light fixtures exist.
