---
title: "DC-WIN-02 — Windlass foredeck control circuit"
description: "Two foredeck windlass switches actuating a separate contactor"
circuit_id: "DC-WIN-02"
date: 2026-11-01
---

[← Circuit Register](/about/configuration/circuit-register/) · [Windlass power circuit](/about/configuration/circuits/dc-win-01/) · [Windlass EQ-061](/about/configuration/equipment/eq-061/)

> **Owner-confirmed function, control supply untraced:** Two separate switches mounted on the foredeck, [SW-003](/about/configuration/equipment/sw-003/) and [SW-004](/about/configuration/equipment/sw-004/), command [contactor EQ-062](/about/configuration/equipment/eq-062/), which operates the [Lewmar HX1 800 W motor EQ-061](/about/configuration/equipment/eq-061/). This is a **low-current functional control relationship**, separate from high-current motor supply [DC-WIN-01](/about/configuration/circuits/dc-win-01/).

| Attribute | Current documentation |
| --- | --- |
| Logical control circuit | `DC-WIN-02` |
| Operator inputs | Two separate foredeck switches **SW-003** and **SW-004**, exact UP/DOWN mapping not yet established |
| Controlled device | **EQ-062** windlass contactor |
| Controlled load | **EQ-061** Lewmar HX1 800 W |
| Control source and return | **Unknown**; no traced fuse position, earth return, terminal number or wire colour |
| Installed control fuse | **Unknown**; manufacturer standard circuit shows **3 A fuse**, not established fitted |
| Installed control cable | **Unknown**; Lewmar standard suggests 1.5 mm² switch wiring, not an as-fitted observation |
| Other control stations | Not established by owner evidence; do not assume absent |

The shared [SW-002](/about/configuration/equipment/sw-002/) is the **upstream high-current common battery-switching function**, not one of the two foredeck contactor switches. The [70 A CB-006](/about/configuration/equipment/cb-006/) protects the windlass motor supply, **not a confirmed 70 A control circuit**.

Reference: [Lewmar HX1 installation and wiring manual, Issue 2](https://www.lewmar.com/mst_attachment/attachment/click/attachment_id/56/), section 4.

## Next inspection

Identify both foredeck positions, UP/DOWN operation, contactor coil/command terminal locations, control supply source and protective device, and any cabling to additional controls.
