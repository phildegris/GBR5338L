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

- **Masthead:** [CB-001](/about/configuration/equipment/cb-001/), 10 A, supplies [SW-001](/about/configuration/equipment/sw-001/) DPDT On-Off-On polarity-reversing selector and the [NASA Marine Combi LED](/about/configuration/equipment/eq-021/). **Owner-confirmed switched pair: R3/brown and B4/white** in the 7 × 1.5 mm² trunk, continuing from the forecabin locker into a **separate 2 × 1.5 mm² Oceanflex mast cable**. Both are polarity-switched; neither conductor is a permanent negative return. Exact 2-core wire-to-trunk colour matching and switch pin truth table remain untraced.
- **Steaming:** [CB-002](/about/configuration/equipment/cb-002/), 10 A, supplies the forward-white function of [Osculati 13.243.88 EQ-020](/about/configuration/equipment/eq-020/). The handwritten schedule establishes **Y2 → yellow Oceanflex seven-core trunk conductor** to the forecabin locker; the *separate* mast-going cable and fitting pigtail junction remain untraced.
- **Deck:** [CB-004](/about/configuration/equipment/cb-004/), 10 A, independently feeds the four-LED deck function in the **same EQ-020 housing**. New handwritten source: **R2 → red Oceanflex trunk conductor**; onward forecabin junction and mast leg remain untraced.
- **Bow and stern:** [CB-005](/about/configuration/equipment/cb-005/), 10 A, supplies [EQ-018 bow bicolour](/about/configuration/equipment/eq-018/) and [EQ-019 stern light](/about/configuration/equipment/eq-019/). Handwritten references identify **B3 → green Oceanflex trunk core (bow)** and **B1 → stern-light-labelled connector**, but the stern prefix is not fully legible and the separate routes have not been continuity-traced.

The owner has supplied a [handwritten connector schedule](/about/configuration/dc-terminal-schedule/) identifying all **seven core colours in one Oceanflex 7 × 1.5 mm² trunk**, running from the DC-panel rail to the **forecabin starboard locker**. A second set of similar cage-clamp connectors distributes the cable into **separate runs** for bow/forecabin, returns toward the saloon and routes through the swan neck to mast lighting. **The seven-core trunk does not run directly to the mast.** The branches use original **DIN-rail mounted generic cage-clamp connectors**, arranged into repeated **Yellow → Red → Blue** groups. A code like **`B2`** names the **blue-lever connector in group 2**, not a blue wire or the second terminal on a common connector assembly. [Naming convention](/about/configuration/electrical-reference-system/#confirmed-din-connector-reference-convention). The supplied connector photograph is **partial**; actual branch assignments beyond the legacy entries below remain untraced.

## Legacy terminal notes, retained as references

| Historical reference | Reported function | Status |
| --- | --- | --- |
| Breaker 1,1 | Masthead to DPDT selector | Owner confirms function and 10 A breaker; physical terminal alias retained |
| Selector pins 1–6 | Polarity-reversing masthead supply | Legacy pin notes only; contact map not independently tested |
| `B2` blue lever | **7× blue** trunk core, original handwriting `MAST HD` | Original label retained; superseded as **NASA Combi switched pair** by owner-confirmed R3/B4 |
| `Y2` yellow lever | **7× yellow** core, handwritten `STEAM.` | Panel-end allocation; onward mast leg untraced |
| `R2` red lever | **7× red** core, handwritten `DECK` | New owner handwriting; onward mast leg untraced |
| `B3` blue lever | **7× green** core, handwritten `NAV LTS (Bow)` | Forecabin-bound trunk; actual bow wiring untraced |
| `Y3` yellow lever | **7× black** core, CB column `NC`; older DPDT notes mention NASA | Older NASA link superseded; separate hypothesis of common −12 V return **not verified** |
| `R3` red lever | **7× brown** core, CB column `NC` | **Owner-confirmed NASA Combi switched conductor**, via SW-001; original NC label retained |
| `B4` blue lever | **7× white** core, CB column `NC` | **Owner-confirmed NASA Combi switched conductor**, via SW-001; original NC label retained |
| `B1` blue lever | “RG STERN LT”, prefix unclear | Stern-light label in handwritten notes; cable route untraced |

## Manufacturer references (separate model identity from electrical verification)

- [NASA Marine Supernova Combi product](https://www.nasamarine.com/product/supernova-combi-tri-and-anchor-l-e-d-mastlight/) and [original fitting instructions (PDF)](https://www.nasamarine.com/wp-content/uploads/2015/12/Super-Nova.pdf) explain a **two-wire polarity-reversing tricolour/anchor arrangement**, consistent with Ragtime's NASA Combi. The installed suffix/revision is not independently confirmed.
- **[Osculati 13.243.88 black combined LED light](https://www.osculati.com/en/11401-13.243.88/navigation-and-deck-led-light-1224-v) — owner-confirmed installed model.** Manufacturer specifications include 9–33 V supply, 225° / 3 NM white steaming LED, four 1 W deck LEDs and published current of 0.37 A at 12 V. These are **not measured Ragtime values**. [Technical PDF](https://www.osculati.com/document-handler.ashx?contentrefno=FILE&docpath=DAMST%2F13.243.88.pdf&itemno=M-027838).
- [13.243.88 product pigtail wiring reference](https://www.aquafax.co.uk/products/combined-masthead-white-navigation-light-deck-light-led-12v-24v-731730): yellow + steaming, brown + deck, white common − at the **manufacturer pigtail**. The historic **Y2/yellow Oceanflex forecabin trunk conductor**, the secondary distribution and the **separate mast-going cable** are different, untraced parts of the installation; do not assume the leads connect colour-for-colour.

**Important protection question:** NASA's published Supernova Combi instructions call for a **1 A fuse**. Ragtime's confirmed feeder is an older **10 A panel breaker**. We do not yet know whether a smaller local fuse is fitted, what cross-section is protected, or the exact installed NASA variant. This is a **survey/coordination item**, not a conclusion that the installation is unsafe or noncompliant.

## Outstanding onboard survey

The **Osculati 13.243.88** model, **Oceanflex 7 × 1.5 mm²** panel-to-forecabin trunk, **NASA mast 2 × 1.5 mm² cable**, **Osculati mast 3 × 1.5 mm² cable** and the NASA **R3/brown + B4/white switched pair** are now owner-confirmed. The next survey is the **forecabin starboard-locker secondary connectors**: identify onward runs to bow, saloon and mast (via the swan neck), negatives, joints and any jumpers. NASA variant, exact correspondence between the 2-core mast wires and brown/white trunk cores, polarity-switch contacts, assumed negative busbar connections and local downstream protection remain open.
