---
title: "Electrical Reference System"
description: "Proposed conventions for identifying electrical circuits, devices and locations aboard Ragtime"
date: 2026-10-31
summary: "Location codes, equipment references, circuit identifiers and protection relationships."
---

> **Status: Proposed convention — not an as-built wiring record.** Numerical identifiers and electrical relationships on this page are illustrative until confirmed by a survey aboard Ragtime. Do not use example connections or protective-device ratings as installation instructions.

The objective is to identify a circuit, find the breaker or fuse protecting it, and locate any switch, terminal or piece of equipment aboard Ragtime. The convention takes inspiration from Royal Navy location and equipment referencing, without introducing warship-scale complexity.

## Four separate concepts

| Concept | Example | Meaning |
| --- | --- | --- |
| **Location** | `CT-P` | The physical location of an item |
| **Equipment** | `CB-014` | A particular circuit breaker |
| **Circuit** | `DC-PIL-01` | A specific electrical circuit |
| **Relationship** | `CB-014` protects `DC-PIL-01` | How a device participates in a circuit |

An equipment ID does **not** encode location, and a circuit ID does **not** encode its protective device. Consequently, equipment can move and protection can be replaced without renumbering the circuit.

## Location codes

Start with recognisable compartments or functional areas, adding a sublocation only when precision matters.

| Code | Proposed location |
| --- | --- |
| `FP` | Forepeak / anchor locker |
| `FC` | Forward cabin |
| `SL` | Saloon |
| `CT` | Chart table / navigation station |
| `GL` | Galley |
| `HD` | Heads |
| `AC` | Aft cabin |
| `ER` | Engine compartment |
| `AL` | Aft locker / steering compartment |
| `CP` | Cockpit |
| `HM` | Helm / pedestal |
| `MS` | Mast |
| `BL` | Bilge |

Examples: `CT-P` = chart table panel face; `CT-R` = rear of chart table panel; `AL-S` = starboard side of aft locker; `MS-T` = masthead. The generic examples remain **proposed** until surveyed.

### Owner-designated sublocations

| Code | Name | Physical description | Evidence and scope |
| --- | --- | --- | --- |
| `SL-COM` | **COM frame** | Saloon, starboard-forward side, adjacent to the chart-table DC panel | Owner-designated location (31 October 2026). Includes Icom M510 (`EQ-003`), Ocean Signal ATB1 (`EQ-004`), Digital Yacht SPL2000 (`EQ-005`), and four-way FC fuse board (`EQ-057`). [Supply and RF paths](/about/configuration/com-frame/) owner-reported; conductor and fuse ratings not surveyed. |
| `MS-T` | **Masthead** | Masthead antenna/light mounting area | Owner confirms the **Vesper Marine VA159** VHF/AIS-band antenna (`EQ-058`) connected to the SPL2000 on the COM frame; coax details and measured VSWR pending. |

The COM frame is a **location**, not an equipment item or circuit. Its location code is deliberately independent of the equipment IDs, so devices can be replaced or relocated without renumbering them.

## Equipment record and index status

Equipment documentation progress and electrical verification are **distinct**. Each equipment page owns its `survey_state` (for example `U`, `T` or `G`) and optional `documentation_stage`. The Equipment Register and Catalogue use a Hugo `equipment-status` shortcode to **render these values automatically**; do not separately maintain status in their tables.

- `documentation_stage: mapped` — equipment identity, location and relevant functional connections have been documented from owner information. **This is not independently verified as-built electrical work.**
- `survey_state: U` — installation not independently electrically surveyed, even if the owner has confirmed details; `T` = tentative, `G` = grouped.
- A completed physical inspection or electrical test should be recorded with its evidence and only then change the applicable survey state.

## Equipment references

Assign permanent identifiers to significant components, unique **within the equipment type**.

| Prefix | Type |
| --- | --- |
| `SW` | Switch or control |
| `CB` | Circuit breaker |
| `FU` | Fuse |
| `TB` | Terminal block |
| `BB` | Busbar |
| `RL` | Relay or contactor |
| `BAT` | Battery |
| `EQ` | Other electrical equipment |

Thus `CB-014` denotes a breaker regardless of its panel position. Its equipment record should contain its physical location, make, model, rating and a photograph. Keep installation and change history separate from the identifier.

## Circuit references

Use `<SUPPLY>-<SYSTEM>-<NUMBER>`, with examples such as `DC-PWR-01` for DC power distribution, `DC-PIL-01` for autopilot power and `AC-PWR-01` for an AC distribution circuit. The system abbreviation describes the function; the number does not correspond to a breaker or switch number.

Examples here remain illustrative; the first real circuit is [DC-COM-01](/about/configuration/circuits/dc-com-01/), protected by CB-003 and supplying EQ-057.

## Relationship between a breaker and a circuit

Model protection as an explicit **circuit-to-device relationship**. The circuit record should identify its source, primary branch protection, upstream protection and loads. Crucially, a breaker or fuse protects a **defined downstream conductor or wiring section**, not necessarily a complete functional subsystem.

| Relationship | Illustrative example |
| --- | --- |
| Supply | `DC-PIL-01` supplied from `BB-001` |
| Primary branch protection | `CB-014` protects `DC-PIL-01` |
| Upstream protection | `FU-001` upstream of `CB-014` |
| Load | `DC-PIL-01` feeds `EQ-019` |
| Location | `CB-014` located at `CT-P` |

The **[Circuit Register](/about/configuration/circuit-register/)** is authoritative for the protective relationship. A breaker's equipment page can display the reverse relationship — *circuits protected by this device* — rather than keeping a second copy that might become inconsistent.

A proposed future structured circuit record:

```yaml
id: DC-PIL-01
name: Autopilot power
status: proposed
source: BB-001
protection:
  primary: CB-014
  upstream:
    - FU-001
loads:
  - EQ-019
```

This YAML is only an example, **not an as-installed circuit**. Each protective device's position in the actual wiring, size, rating and conductor cross-section must be verified.

## Preserve existing physical markings

The current [DC Logical Circuits](/about/configuration/logical-circuits/) page describes breaker positions by column and row (such as `1,1`), **individual cage-clamp connector positions** (such as `B2` and `Y3`), and existing busbar names (`DC-BB-M` and `DC-BB-A`).

### Confirmed DIN connector reference convention

Behind the main DC panel are **separate generic cage-clamp connectors**, arranged by the owner into repeating groups of **Yellow → Red → Blue** lever colours. Groups are numbered from the **top down** following the legacy notes. The code combines **connector lever colour + group number**, not cable insulation colour or an equipment ID.

| Physical alias | Exact meaning |
| --- | --- |
| `Y1` | Yellow lever connector, group 1 |
| `R1` | Red lever connector, group 1 |
| `B1` | Blue lever connector, group 1 |
| `Y2` | Yellow lever connector, group 2 — legacy steaming-light connection |
| `B2` | Blue lever connector, group 2 — legacy masthead connection |
| `Y3` | Yellow lever connector, group 3 — legacy masthead connection, **black-insulated conductor** |
| `R4` | Red lever connector, group 4 (naming example; connected circuit not established) |

A group is a **physical ordering convention**, not one electrically common three-terminal block. `TB-001` and `TB-002` currently document the **second and third groups**, respectively, without inventing equipment IDs for every clamp or claiming cross-connections. The **photo supplied is incomplete**; total group count, populated terminals, jumpers, actual wiring and equipment manufacturer's identity remain to be surveyed.

Do not conflate (1) lever colour, (2) mast-cable insulation colour or (3) product pigtail lead colour. They can differ. In particular, a `Y3` yellow-lever cage clamp is reported connected to the **black** mast conductor.

Keep these as **physical position references and legacy aliases** while migrating to the new conventions. Do not silently replace verified onboard markings with newly invented numbers.

## Verified versus proposed

Every future register entry should distinguish **Installed / Verified**, **Installed / Unverified**, **Planned** and **Retired**. Record the last physical verification date, location, connection and terminal references, protective-device ratings, cable details and photographs where practicable.

The sensible first survey is the chart-table DC panel. From that we can progressively build the Location Register, Equipment Register and Circuit Register without inventing wiring that has not yet been traced.
