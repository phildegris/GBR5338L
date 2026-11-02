---
title: "House-bank source and DC distribution"
description: "Six circuits; single remote switch; fitted ANL and battery-post fuses; retained 70 A windlass breaker"
date: 2026-10-31
summary: "Single house-bank source, three unswitched and three commonly switched services, installed protection, Victron BMV-712 shunt."
---

[← Electrical configuration](/about/configuration/) · [Equipment Register](/about/configuration/equipment-register/) · [Circuit Register](/about/configuration/circuit-register/)

> **Owner-confirmed installation facts, not an independently electrically tested as-built schematic.** The complete house bank is deliberately represented by one aggregate two-terminal source [EQ-059](/about/configuration/equipment/eq-059/). Its internal batteries, chemistry, capacity and forthcoming LiFePO4 upgrade belong in a separate audit.

## Positive supply and common negative return

{{< house-distribution id="house_bank" >}}

The house-bank positive source supplies [BB-003](/about/configuration/equipment/bb-003/). **One physical remote battery switch [SW-002](/about/configuration/equipment/sw-002/) controls House, Autopilot and Windlass together**; Watchkeeper, Pump 1 and Pump 2 bypass it.

| Supply | Remote-switch state | Circuit | As-fitted protective evidence |
| --- | --- | --- | --- |
| Watchkeeper | Unswitched | [DC-WAT-01](/about/configuration/circuits/dc-wat-01/) | ANL fuse installation confirmed as a group; actual current way/rating untraced |
| Pump 1 | Unswitched | [DC-BIL-01](/about/configuration/circuits/dc-bil-01/) | Protection device/branch position not yet reconciled |
| Pump 2 | Unswitched | [DC-BIL-02](/about/configuration/circuits/dc-bil-02/) | Protection device/branch position not yet reconciled |
| House | Switched through **SW-002** | [DC-HOU-01](/about/configuration/circuits/dc-hou-01/) | Owner confirms original ANL fuse installation; current assignment untraced |
| Autopilot | Switched through **same SW-002** | [DC-PIL-01](/about/configuration/circuits/dc-pil-01/) | Individual downstream fuse allocation untraced |
| Windlass | Switched through **same SW-002** | [DC-WIN-01](/about/configuration/circuits/dc-win-01/) → [Lewmar HX1 EQ-061](/about/configuration/equipment/eq-061/) | **Fitted 70 A breaker [CB-006](/about/configuration/equipment/cb-006/)**, with fitted ANL fusing also confirmed; circuit order/rating of ANL not traced |

There are **six distinct functional circuits**, **three unswitched** and **three controlled by one common remote switch**. The six circuits are not assumed to correspond to six individual terminals or fuseholders on the source busbar.

## Owner-confirmed fitted protection — ANL, battery posts and windlass breaker

The owner has now explicitly confirmed that **all of the ANL fuses and battery-post fuses associated with the earlier DC-distribution build were fitted**, and **the windlass's existing 70 A circuit breaker was retained in its supply**. Therefore **installed ANL/MRBF fusing is a fact**, not merely a project proposal. Exact fitted ratings, fuse counts, cable sizes, and today's connection to each service circuit still need inspection.

The older sources record the following **historical nominal design ratings**, which must not be mistaken for a current fuse-body reading:

| Design record | Nominal ratings and allocations documented then | Status |
| --- | --- | --- |
| July 2025 house-bank discussion | Two **125 A MRBF battery-post** fuses with equal **25 mm²** feed cables; an intermediate design also considered **80 A MIDI/MEGA panel**, **40 A MIDI/MEGA pump** and individual **20 A pump fuses** | Battery-post fuses **confirmed installed**; old exact ratings, count and MIDI/MEGA alternatives not independently checked |
| [5 August 2025 DC Distribution Panel Upgrade](/articles/technical/dc-distribution-panel/) | **80 A ANL Primary**, **80 A ANL Auxiliary**, **100 A ANL Windlass**, **40 A ANL Watchkeeper**; proposed Windlass **25 mm²**, **10 m**, **Lewmar HX1** | Original ANL fuses **confirmed installed**; the 2025 functional group names and per-fuse ratings must **not automatically be mapped** to today's six service circuits |
| Current owner confirmation | **70 A windlass breaker retained in the windlass supply** | **Confirmed fitted protective device [CB-006](/about/configuration/equipment/cb-006/)**, in addition to the installed ANL fuse arrangement |

A **100 A ANL fuse and 70 A breaker can both exist in the same windlass supply**. They may perform different upstream-cable protection and local isolation functions. Their actual ordering and protection selectivity remain unverified. We are **not** choosing one in place of the other.

**Current windlass identity:** Owner confirms fitted **[Lewmar HX1 800 W, EQ-061](/about/configuration/equipment/eq-061/)**, **70 A [CB-006](/about/configuration/equipment/cb-006/) breaker**, and a **separate [contactor EQ-062](/about/configuration/equipment/eq-062/)** controlled by **two foredeck switches [SW-003](/about/configuration/equipment/sw-003/) and [SW-004](/about/configuration/equipment/sw-004/)**. The earlier 80 A breaker reference was an audit error, superseded 1 November 2026. The historic **100 A ANL** remains a design rating pending inspection of the actual fuse. Contactor maker/part, UP/DOWN mapping and any control fuse are unverified.

**Evidence provenance:** Owner's direct installation confirmations in the October 2026 electrical audit, plus 2025 dated planning records. The physical 5 August 2025 photograph shows **one WhisperPower-branded remote battery switch** and **four lower covered fuseholders**; the labels and output cables cannot be read. It supports the hardware-family history, not individual fuse allocations. A later **BEP 701-MD** preference was a *replacement proposal*, not confirmed installed.

Individual `FU-NNN` IDs for the source ANL/MRBF fuses will be allocated when we can distinguish the particular fitted devices and identify their physical way/relationship without guessing. This does **not** defer recording that their installation was owner-confirmed.

## Victron BMV-712 negative measurement path

The owner confirms the **house-bank negative terminals directly connect through bespoke DIY tinned-copper link [BB-004](/about/configuration/equipment/bb-004/) to the battery-facing terminal of the fitted [BMV-712 shunt, EQ-060](/about/configuration/equipment/eq-060/)**.

All outgoing house services, windlass return (where connected to this bank), and charging returns must use the **system/load side of the shunt** to ensure net-bank current measurement. The physical path between this system-side terminal and the existing [main negative bus BB-001](/about/configuration/equipment/bb-001/) remains untraced.

The earlier copper-link design included approximately **25.4 × 3.2 mm tinned copper**, but the **installed bar's dimensions and ampacity have not been measured**. The BMV fused positive-sense feed and its physical location likewise remain to be inspected.

## Remaining as-fitted audit

Trace the battery-post fuse quantity and markings without expanding the aggregate house-bank model; read ANL fuse ratings and identify the photographed fuseholder ways; confirm SW-002's actual model and common switched output; trace the electrical placement of **CB-006** (mounted aft in the engine drive compartment, beneath the aft cabin bunk) relative to the Windlass ANL fuse and its motor controller; then map individual House, Autopilot, Watchkeeper and pump protections and all negative returns.

**Safety:** This documentation is not an instruction to disconnect live battery cables. Isolate and follow safe manufacturer-approved work methods when conducting the high-current physical survey.
