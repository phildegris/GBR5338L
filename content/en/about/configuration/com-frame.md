---
title: "COM frame — DC and RF functional connections"
description: "Owner-reported communications DC supply and shared antenna topology"
date: 2026-10-31
summary: "COM-frame four-way fused distribution and masthead shared VHF/AIS antenna."
---

> **Status: Owner-confirmed functional topology, not independently tested.** CB-003 directly feeds EQ-057. The Vesper VA159 is connected to SPL2000 by white Ancor RG213 coax routed inside the mast and through a swan-neck into the deckhead. DC feeder cable size, fuse-board branch ratings, RF cable length, connectors and measured VSWR remain unverified.

[← Electrical configuration](/about/configuration/) · [Equipment Register](/about/configuration/equipment-register/) · [Location reference system](/about/configuration/electrical-reference-system/)

## Physical locations

- **`SL-COM` — COM frame:** saloon, starboard-forward side, adjacent to the original main DC panel. Holds [EQ-003](/about/configuration/equipment/eq-003/) Icom M510, [EQ-004](/about/configuration/equipment/eq-004/) Ocean Signal ATB1, [EQ-005](/about/configuration/equipment/eq-005/) Digital Yacht SPL2000 and [EQ-057](/about/configuration/equipment/eq-057/) four-way FC fuse board.
- **`MS-T` — masthead:** [EQ-058](/about/configuration/equipment/eq-058/) shared VHF/AIS-band-compatible **Vesper Marine VA159** antenna (manufacturer and model owner-confirmed).

## DC distribution — owner-confirmed

```text
EQ-001 Moody DC panel
  | 10 A CB-003 at 3,4, VHF AIS
  | DC-COM-01 (owner-confirmed)
  v
EQ-057 four-way fuse board (SL-COM)
  |-- fuse ? --> EQ-003 VHF
  |-- fuse ? --> EQ-004 AIS
  |-- fuse ? --> EQ-005 SPL2000
  '-- fourth way unknown
```

[DC-COM-01](/about/configuration/circuits/dc-com-01/) is the **confirmed feeder**, protected by [CB-003](/about/configuration/equipment/cb-003/) and supplying [EQ-057](/about/configuration/equipment/eq-057/). See the [Circuit Register](/about/configuration/circuit-register/). The 10 A feeder protection is **separate** from the board's three individual branch fuses; feeder conductor size and return path are not yet recorded.

## RF signal paths — owner-confirmed functional topology

```text
EQ-058  Masthead shared VHF / AIS antenna (MS-T)
  |
  |  Ancor white RG213 coax, 50 ohms
  |  Inside mast -> swan-neck pipe -> deckhead -> SPL2000
  v
EQ-005  Digital Yacht SPL2000, ANTENNA input (SL-COM)
  |-- VHF output --> EQ-003  Icom M510 VHF
  '-- AIS output --> EQ-004  Ocean Signal ATB1
```

The owner confirms a **white Ancor Marine Grade RG213 coax cable** runs from the Vesper VA159 **internally down the mast**, passes through a **swan-neck pipe into the deckhead**, then continues to the SPL2000. Length, connectors/joints and water sealing remain unverified. The owner confirms the VHF and AIS RF connections through the SPL2000 and the single masthead antenna. The SPL2000 manufacturer documents common-antenna operation, including a fail-safe VHF path in the event of lost splitter power. The optional AM/FM port is not documented as connected aboard Ragtime.

### Manufacturer reference — Ancor white RG213

| Specification | Ancor catalogue value |
| --- | --- |
| Impedance | **50 Ω** |
| Nominal outside diameter | **10.3 mm** |
| Conductors / screening | Tinned copper centre and braid; **96% braid coverage** |
| Sheath | UV-inhibited white PVC |
| Capacitance | **30.8 pF/ft** |
| Propagation velocity | **66%** |
| Attenuation | **1.9 dB/100 ft at 100 MHz**, not a measured 162 MHz loss |

The cable is an RF transmission connection, **not a new powered equipment asset**. Run length, connector count, measured loss and VSWR are not yet established.

- [Ancor 2024 manufacturer catalogue (PDF, coax specifications on printed page 16)](https://disvent.com/pub/media/descargas/Cat%C3%A1logo%20Ancor.pdf)
- [Digital Yacht SPL2000 installation manual (PDF)](https://support.digitalyacht.net/Manuals/SPL2000%20User%20Manual%20V1_00_Eng.pdf)

## Outstanding onboard survey

1. CB-003 directly feeds EQ-057 per owner confirmation. Check feeder conductors, fuse-board model and fourth-way use during survey.
2. Record feeder/return conductor sizes and route, additional upstream protection and actual branch fuse values.
3. Ancor white RG213 and the inside-mast/swan-neck route are owner-confirmed; record total run length and connector/joint locations.
4. Inspect connector moisture protection and swan-neck chafe/strain relief; measure VHF and AIS-frequency VSWR where practical.
5. Recheck these supply and protection relationships when the main DC panel is replaced in the planned winter refit.

