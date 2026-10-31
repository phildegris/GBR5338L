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

CB-003 protects the **DC-COM-01 feeder**. The **10 A / 3 A / 3 A branch fuses**, allocated as FU-001–FU-003, protect their respective outgoing circuits. **The 10 A VHF branch fuse equals the upstream 10 A breaker nominal rating**; selectivity is not established without fuse/breaker characteristics. EQ-057's fourth position is not confirmed as occupied or spare.
