---
title: "Circuit Register"
date: 2026-10-31
---

**Status: owner-confirmed, not independently tested.** Circuit identities are distinct from equipment and physical locations.

| Circuit | Primary protection | Destination | Survey status |
| --- | --- | --- | --- |
| [DC-COM-01](/about/configuration/circuits/dc-com-01/) | [CB-003](/about/configuration/equipment/cb-003/) 10 A, panel `3,4` (VHF AIS) | [EQ-057](/about/configuration/equipment/eq-057/) four-way COM-frame fuse board | Owner-confirmed; feeder cable untested |
| [DC-COM-02](/about/configuration/circuits/dc-com-02/) | [FU-001](/about/configuration/equipment/fu-001/) **10 A**, EQ-057 way **1** | [EQ-003](/about/configuration/equipment/eq-003/) Icom M510 VHF | Owner-confirmed branch protection; conductor not surveyed |
| [DC-COM-03](/about/configuration/circuits/dc-com-03/) | [FU-002](/about/configuration/equipment/fu-002/) **3 A**, EQ-057 way **2** | [EQ-005](/about/configuration/equipment/eq-005/) Digital Yacht SPL2000 | Owner-confirmed branch protection; conductor not surveyed |
| [DC-COM-04](/about/configuration/circuits/dc-com-04/) | [FU-003](/about/configuration/equipment/fu-003/) **3 A**, EQ-057 way **3** | [EQ-004](/about/configuration/equipment/eq-004/) Ocean Signal ATB1 | Owner-confirmed branch protection; conductor not surveyed |

## Navigation and deck lighting

| [DC-NAV-01](/about/configuration/circuits/dc-nav-01/) | [CB-001](/about/configuration/equipment/cb-001/) **10 A**, NAV LTS row 1 | EQ-021 — NASA Combi via SW-001 | Owner-confirmed 10 A and functional loads; DIN conductor paths not electrically traced |
| [DC-NAV-02](/about/configuration/circuits/dc-nav-02/) | [CB-002](/about/configuration/equipment/cb-002/) **10 A**, NAV LTS row 2 | EQ-020 — Osculati steaming function | Owner-confirmed 10 A and functional loads; DIN conductor paths not electrically traced |
| [DC-NAV-03](/about/configuration/circuits/dc-nav-03/) | [CB-004](/about/configuration/equipment/cb-004/) **10 A**, NAV LTS row 3 | EQ-020 — Osculati deck function, **same physical housing** | Owner-confirmed 10 A and functional loads; DIN conductor paths not electrically traced |
| [DC-NAV-04](/about/configuration/circuits/dc-nav-04/) | [CB-005](/about/configuration/equipment/cb-005/) **10 A**, NAV LTS row 4 | EQ-018 + EQ-019 — Osculati bow bicolour and stern LEDs | Owner-confirmed 10 A and functional loads; DIN conductor paths not electrically traced |

The NAV LTS panel contains four owner-confirmed **10 A** branch breakers. The separate steaming and deck circuits feed *different functions of the same Osculati fitting EQ-020*; the bow and stern each have a luminaire but **share CB-005**. The exact DIN terminal assignments beyond legacy notes, conductor sizes and return paths remain unverified.

## Communications power distribution

CB-003 protects the **DC-COM-01 feeder**. The **10 A / 3 A / 3 A branch fuses**, allocated as FU-001–FU-003, protect their respective outgoing circuits. **The 10 A VHF branch fuse equals the upstream 10 A breaker nominal rating**; selectivity is not established without fuse/breaker characteristics. EQ-057's fourth position is not confirmed as occupied or spare.
