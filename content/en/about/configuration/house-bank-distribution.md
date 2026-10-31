---
title: "House-bank source and DC distribution"
description: "Five service feeds, one shared House/Autopilot switch and BMV-712 negative monitoring"
date: 2026-10-31
summary: "House bank as a single source, three always-on feeds, one remote switch supplying House and Autopilot, plus Victron BMV-712 shunt."
---

[← Electrical configuration](/about/configuration/) · [Equipment Register](/about/configuration/equipment-register/) · [Circuit Register](/about/configuration/circuit-register/)

> **Owner-confirmed functional architecture, not a verified as-built wiring diagram.** The house bank is represented **only as a single positive and negative electrical source interface**. The internal battery count, chemistry, capacity, interconnection, and proposed LiFePO4 replacement will be recorded **later**, as a separate bank/component audit. Historic proposal specifications are identified explicitly below.

## Supply and return topology

{{< house-distribution id="house_bank" >}}

The source is [EQ-059](/about/configuration/equipment/eq-059/), an **aggregated source port**, not an additional battery. The house-bank positive feeds a distribution bus [BB-003](/about/configuration/equipment/bb-003/) with **five functional service branches**, but **only one shared remote switch** [SW-002](/about/configuration/equipment/sw-002/) for House and Autopilot. The three other service feeds bypass SW-002:

| Output | Owner-confirmed switching | Circuit | Destination / outstanding detail |
| --- | --- | --- | --- |
| Watchkeeper | **Always supplied** (not disconnected by remote House/Autopilot switches) | [DC-WAT-01](/about/configuration/circuits/dc-wat-01/) | Watchkeeper services; individual devices and fuse unknown |
| Pump 1 | **Unswitched** by remote House/Autopilot isolation | [DC-BIL-01](/about/configuration/circuits/dc-bil-01/) | Pump 1; distinct local fuse/controls not traced |
| Pump 2 | **Unswitched** by remote House/Autopilot isolation | [DC-BIL-02](/about/configuration/circuits/dc-bil-02/) | Pump 2; distinct local fuse/controls not traced |
| House | **Switched together with Autopilot** through [SW-002](/about/configuration/equipment/sw-002/) | [DC-HOU-01](/about/configuration/circuits/dc-hou-01/) | Main DC panel [EQ-001](/about/configuration/equipment/eq-001/) and downstream house services |
| Autopilot | **Switched together with House** through the **same [SW-002](/about/configuration/equipment/sw-002/)** | [DC-PIL-01](/about/configuration/circuits/dc-pil-01/) | Separate autopilot distribution; individual branch fuse unknown |

**Unswitched does not mean unprotected.** Branch fuse sizes, positions, source fuse and wire gauges are **not yet established from as-fitted evidence**. Likewise the pump service numbers are not yet proven to correspond to the legacy tentative [EQ-030](/about/configuration/equipment/eq-030/) and [EQ-031](/about/configuration/equipment/eq-031/) entries.

## Victron BMV-712 negative return path

The owner confirms a fitted [Victron BMV-712](/about/configuration/equipment/eq-060/). Its **shunt is connected directly to the existing house-bank negative terminals through the bespoke tinned-copper interconnection [BB-004](/about/configuration/equipment/bb-004/)**.

- **Battery side of shunt:** only the house-bank negative terminals via the copper bar. No load or charging return should bypass the shunt.
- **System/load side of shunt:** returns for all house circuits **and** any battery charging equipment. The previous record [BB-001](/about/configuration/equipment/bb-001/) describes a main engine-bay negative busbar, but the actual shunt-to-busbar cable, connection order and any engine-ground relationships have **not** been traced.
- **BMV monitor supply/sensing:** the battery monitor should remain live when the one common remote service switch SW-002 is OFF. The historic design places its fused monitor feed on the **always-live Watchkeeper side**; the *actual fused sense connection* has not been surveyed.

The shunt is a **current measurement component**, not a negative-side circuit isolation switch. The bespoke copper bar's dimensions and current rating require physical verification; a previously discussed 25.4 × 3.2 mm link is a historical construction design, **not an as-fitted measurement**.

## Historical assembly photograph — 5 August 2025

The owner supplied an image of a **pre-existing modular positive distribution assembly**, shown in a photo-library entry dated **5 August 2025**. This is direct **photographic evidence of the assembly at that date**, **not yet confirmation of its current installed state aboard Ragtime**. The original image is available in the electrical audit conversation; the site currently records its observations rather than hosting a copy.

| Visible feature | Observation and evidence limit |
| --- | --- |
| Remote switching unit | One **WhisperPower-branded DC Modular Remote Battery Switch** is visible, with local OPEN/CLOSE buttons, status LEDs and a five-wire-style control cable. The **actual fitted model number, voltage variant and live control wiring are not legible** |
| Manufacturer comparison | [WhisperPower Remote Battery Switch 12 V / 500 A (article 50214733)](https://www.whisperpower.com/remote-battery-switch-12-v-500-a) is a strong product-family match. Its published **500 A continuous** rating, latching operation, manual controls and status feedback are **manufacturer specifications**, not measurements or a confirmed model label on this photographed device |
| High-current fuse positions | **Four individual transparent-covered fuseholders are clearly visible across the lower row**. Their fuse values, exact series, connected loads and load-side cable terminations **cannot be read or assigned** from this image |
| Upper protected hardware | Additional covered stud/terminal positions and interconnecting metal links are visible beside the switching unit. **A fifth branch fuse or source termination cannot safely be identified from this view** |
| Cable terminations | The photographed face does not establish the outgoing high-current leads, individual fuse values, battery-side main protection or negative return wiring |
| House / Autopilot switching | **One switching unit** is visible in the August 2025 photo. **Owner has now confirmed one common remote switch supplying House and Autopilot**, while Watchkeeper and both pumps bypass it. The photograph alone does not establish which terminals, protective devices or cables provide these connections |

The modular fuseholder/busbar construction is consistent with the [TBS Electronics DC Modular family](https://tbs-electronics.com/product-category/dc-modular-fuseholders-busbars/), used in WhisperPower distribution products. Do not infer a particular fuse type or holder rating until its part markings are inspected.

**Chronology matters:** This **August 2025 pictured WhisperPower assembly** predates the **September 2026 preference for BEP 701-MD** in our design discussions. The owner's October 2026 clarification confirms one common switching function; it does **not** verify the brand/model of the currently fitted hardware. The later BEP choice was **a proposed alternative**, not evidence of a replacement or the currently fitted model. The photograph does not justify upgrading any of the five circuit protection entries to a specific fuse rating.

## Remote switching — earlier design recovered

The original 2025 [DC panel upgrade article](/articles/technical/dc-distribution-panel/) proposed separately fused Watchkeeper, Primary, Auxiliary and Windlass branches, with different currents and switching arrangements. That is **design history**, not evidence the older grouping remains fitted; it does not override the **one common remote switch** and five functional services now confirmed by the owner.

The August 2025 photograph above provides a **specific historical WhisperPower assembly**, distinct from the later design preferences. In the September 2026 design discussion the preferred **remote-switch architecture** was a mechanically/manual-operable motorised switch with **remote ON/OFF, local ON/OFF operating the same power contacts and state reporting the actual position**. **BEP 701-MD** was the leading **candidate** for that architecture (rated 275 A in product references), preferred to an earlier Durakool DSC08 bistable-relay plus bypass approach and the larger Blue Sea 7700 ML-RBS. **The owner has confirmed there is only ONE remote switch for both House and Autopilot** ([SW-002](/about/configuration/equipment/sw-002/)); its exact product model and remote-control wiring remain unverified. Neither BEP 701-MD nor the older alternatives are recorded as installed.

**The Watchkeeper and both pump branches bypass the single SW-002 contact** and remain supplied when SW-002 is OPEN. House and Autopilot share its switched state, but their separate downstream protective devices and cable routes remain to be identified.

## Items needed for as-fitted completion

1. Identify the **main bank positive terminal protection**, master/manual isolation and any fuses serving each of five outputs, including ratings and wire cross-sections.
2. Owner has confirmed **one common switch** [SW-002](/about/configuration/equipment/sw-002/) serving both House and Autopilot (not separate independent controls). Confirm whether the **5 August 2025 WhisperPower device** is still the fitted hardware, its model/ratings, actual incoming and outgoing connections and remote control location.
3. Photograph/identify the **positive busbar construction**, shunt marking and the custom negative copper link, verifying the shunt's battery-side/system-side orientation and connection to existing [BB-001](/about/configuration/equipment/bb-001/).
4. Confirm the Watchkeeper loads, the identity of Pump 1 and Pump 2, and the actual house-feed cable destination on the DC panel.

**Safety and provenance:** This is an inventory/documentation exercise, not an instruction to disconnect or work on live battery cables. Maintain isolation and manufacturer-approved service practice when surveying a high-current house-bank installation.
