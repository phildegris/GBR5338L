---
title: "COM frame — DC and RF functional connections"
description: "Owner-reported communications DC supply and shared antenna topology"
date: 2026-10-31
summary: "COM-frame four-way fused distribution and masthead shared VHF/AIS antenna."
---

> **Status: Owner-reported topology, not tested as-built wiring.** Equipment locations and functional supply/RF relationships were confirmed by Ragtime's owner on 31 October 2026. Cable routes, fuse positions/ratings, conductor sizes, RF connectors and upstream protective-device identities are **not yet surveyed**.

[← Electrical configuration](/about/configuration/) · [Equipment Register](/about/configuration/equipment-register/) · [Location reference system](/about/configuration/electrical-reference-system/)

## Physical locations

- **`SL-COM` — COM frame:** saloon, starboard-forward side, adjacent to the original main DC panel. Holds [EQ-003](/about/configuration/equipment/eq-003/) Icom M510, [EQ-004](/about/configuration/equipment/eq-004/) Ocean Signal ATB1, [EQ-005](/about/configuration/equipment/eq-005/) Digital Yacht SPL2000 and [EQ-057](/about/configuration/equipment/eq-057/) four-way FC fuse board.
- **`MS-T` — masthead:** [EQ-058](/about/configuration/equipment/eq-058/) shared VHF/AIS-band-compatible **Vesper Marine VA159** antenna (manufacturer and model owner-confirmed).

## DC distribution — owner-reported functional topology

```text
EQ-001  Original main DC panel
  |
  |  Feeder and upstream protection: NOT YET SURVEYED
  v
EQ-057  Four-way FC fuse board (SL-COM)
  |-- [way ? / fuse ?] --> EQ-003  Icom M510 VHF
  |-- [way ? / fuse ?] --> EQ-004  Ocean Signal ATB1 AIS
  |-- [way ? / fuse ?] --> EQ-005  Digital Yacht SPL2000 splitter
  '-- [way ?]          --> Unknown; spare status unconfirmed
```

- The **fuse board assembly** has equipment ID `EQ-057`. Four fuse positions are **not yet four individually allocated FU devices**: each actual installed fuse should receive its own `FU-xxx` equipment ID after a survey, with its physical way, type, rating and protected conductor/circuit recorded.
- The board is owner-reported as **supplied from the main panel**. The feeder cable, its source breaker/fuse, return arrangements and upstream protection remain unspecified.
- Do not assign circuit IDs or manufacturer-recommended fuse sizes as Ragtime's installed protective ratings without tracing and checking the conductors.

## RF signal paths — owner-confirmed functional topology

```text
EQ-058  Masthead shared VHF / AIS antenna (MS-T)
  |
  |  Mast coax details: NOT YET SURVEYED
  v
EQ-005  Digital Yacht SPL2000, ANTENNA input (SL-COM)
  |-- VHF output --> EQ-003  Icom M510 VHF
  '-- AIS output --> EQ-004  Ocean Signal ATB1
```

The owner confirms the VHF and AIS RF connections through the SPL2000 and the single masthead antenna. The SPL2000 manufacturer documents common-antenna operation, including a fail-safe VHF path in the event of lost splitter power. The optional AM/FM port is not documented as connected aboard Ragtime.

**Product reference:** [Digital Yacht SPL2000 installation and user manual (PDF)](https://support.digitalyacht.net/Manuals/SPL2000%20User%20Manual%20V1_00_Eng.pdf).

## Outstanding onboard survey

1. Identify the model/manufacturer of the **FC** four-way fuse board, its rated voltage/current and whether the fourth way is occupied or spare.
2. Record the main panel feeder source, upstream fuse/breaker, conductor cross-section and length, negative return, fuse-board way numbers and *actual fitted* fuse ratings.
3. Confirm the **Vesper Marine VA159** coax type, masthead mounting, connectors and measured VSWR where possible; the model is owner-confirmed but installation measurements remain outstanding.
4. Inspect coax cable type, masthead base and deck transitions, splitter RF connectors, and the optional AM/FM output; record checks of antenna match/VSWR at both voice VHF and AIS frequencies when practical.
5. Recheck these supply and protection relationships when the main DC panel is replaced in the planned winter refit.

