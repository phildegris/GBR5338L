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
- **Steaming:** [CB-002](/about/configuration/equipment/cb-002/), 10 A, feeds the forward-white section of the **owner-confirmed Osculati 13.243.88** [EQ-020](/about/configuration/equipment/eq-020/). Legacy terminal **Y2** and **yellow seven-core mast conductor** have not been physically matched to the product's pigtail.
- **Deck:** [CB-004](/about/configuration/equipment/cb-004/), 10 A, separately feeds **four downward-facing LEDs** on the **same EQ-020 Osculati housing**, not a second fixture. Its DIN feed and mast cable colour are still unknown.
- **Bow and stern:** [CB-005](/about/configuration/equipment/cb-005/), 10 A, feeds [Osculati bow bicolour LED](/about/configuration/equipment/eq-018/) and [Osculati stern LED](/about/configuration/equipment/eq-019/) together. Their branch point, return path and DIN clamp assignments have not been traced.

The owner confirms that the branches use the original **DIN-rail mounted generic cage-clamp connectors**, arranged into repeated **Yellow → Red → Blue** groups. A code like **`B2`** names the **blue-lever connector in group 2**, not a blue wire or the second terminal on a common connector assembly. [Naming convention](/about/configuration/electrical-reference-system/#confirmed-din-connector-reference-convention). The supplied connector photograph is **partial**; actual branch assignments beyond the legacy entries below remain untraced.

## Legacy terminal notes, retained as references

| Historical reference | Reported function | Status |
| --- | --- | --- |
| Breaker 1,1 | Masthead to DPDT selector | Owner confirms function and 10 A breaker; physical terminal alias retained |
| Selector pins 1–6 | Polarity-reversing masthead supply | Legacy pin notes only; contact map not independently tested |
| `B2` — **blue-lever clamp, group 2** | Blue-insulated seven-core mast conductor → NASA Combi [EQ-021](/about/configuration/equipment/eq-021/) | Legacy notes; no continuity measurement |
| `Y3` — **yellow-lever clamp, group 3** | **Black-insulated** seven-core mast conductor → NASA Combi [EQ-021](/about/configuration/equipment/eq-021/) | Legacy notes; lever colour ≠ wire colour; no continuity measurement |
| Breaker 1,2 → `Y2` — **yellow-lever clamp, group 2** | Yellow-insulated seven-core mast conductor → Osculati steaming light [EQ-020](/about/configuration/equipment/eq-020/) | Legacy notes; manufacturer pigtail junction untraced |
| CB-004 / CB-005 downstream DIN positions | Deck and bow/stern feeds | Not recorded, rather than guessed |

## Manufacturer references (separate model identity from electrical verification)

- [NASA Marine Supernova Combi product](https://www.nasamarine.com/product/supernova-combi-tri-and-anchor-l-e-d-mastlight/) and [original fitting instructions (PDF)](https://www.nasamarine.com/wp-content/uploads/2015/12/Super-Nova.pdf) explain a **two-wire polarity-reversing tricolour/anchor arrangement**, consistent with Ragtime's NASA Combi. The installed suffix/revision is not independently confirmed.
- **[Osculati 13.243.88 black combined LED light](https://www.osculati.com/en/11401-13.243.88/navigation-and-deck-led-light-1224-v) — owner-confirmed installed model.** Manufacturer specifications include 9–33 V supply, 225° / 3 NM white steaming LED, four 1 W deck LEDs and published current of 0.37 A at 12 V. These are **not measured Ragtime values**. [Technical PDF](https://www.osculati.com/document-handler.ashx?contentrefno=FILE&docpath=DAMST%2F13.243.88.pdf&itemno=M-027838).
- [13.243.88 product pigtail wiring reference](https://www.aquafax.co.uk/products/combined-masthead-white-navigation-light-deck-light-led-12v-24v-731730): yellow + steaming, brown + deck, white common − at the **manufacturer pigtail**. The existing mast cable's historical yellow conductor / Y2 connection is a separate, untraced part of the installation; do not assume the leads connect colour-for-colour.

**Important protection question:** NASA's published Supernova Combi instructions call for a **1 A fuse**. Ragtime's confirmed feeder is an older **10 A panel breaker**. We do not yet know whether a smaller local fuse is fitted, what cross-section is protected, or the exact installed NASA variant. This is a **survey/coordination item**, not a conclusion that the installation is unsafe or noncompliant.

## Outstanding onboard survey

The **Osculati 13.243.88 model is now owner-confirmed**. Confirm the NASA variant, photograph breaker body labels (10 A reported by owner), trace the manufacturer's pigtail leads separately from the legacy **Y2/B2/Y3** mast cable and DIN blocks, and record conductor sizes, negative returns, SW-001 polarity operation and local protection.
