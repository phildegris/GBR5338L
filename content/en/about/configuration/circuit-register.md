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

## House-bank primary DC distribution

**Source:** The complete House bank remains one interface [EQ-059](/about/configuration/equipment/eq-059/). The owner confirms fitted **battery-post MRBF fuses** and **ANL distribution fuses**, with **one common SW-002** for House, Autopilot and Windlass; Watchkeeper and both pumps bypass it. Windlass also retains a **fitted 70 A breaker CB-006**. Current ANL fuse ratings, positions and six-service mapping remain unverified. [Distribution diagram](/about/configuration/house-bank-distribution/).

| Circuit | Installed protective evidence | Functional destination | Switching / outstanding detail |
| --- | --- | --- | --- |
| [DC-PWR-01](/about/configuration/circuits/dc-pwr-01/) | Battery-post fuses owner-confirmed installed; 2025 design specified 2 × 125 A MRBF | [EQ-059](/about/configuration/equipment/eq-059/) → [BB-003](/about/configuration/equipment/bb-003/) | Current count, rating and cabling not inspected |
| [DC-WAT-01](/about/configuration/circuits/dc-wat-01/) | ANL fuse installation confirmed as a group; particular fuse/rating not yet mapped | Watchkeeper | Unswitched by SW-002 |
| [DC-BIL-01](/about/configuration/circuits/dc-bil-01/) | Pump circuit protection untraced | Pump 1 | Unswitched by SW-002 |
| [DC-BIL-02](/about/configuration/circuits/dc-bil-02/) | Pump circuit protection untraced | Pump 2 | Unswitched by SW-002 |
| [DC-HOU-01](/about/configuration/circuits/dc-hou-01/) | Original ANL installation owner-confirmed; fuse allocation not yet traced | Main DC panel [EQ-001](/about/configuration/equipment/eq-001/) | Shares SW-002 with Pilot and Windlass |
| [DC-PIL-01](/about/configuration/circuits/dc-pil-01/) | Original ANL installation owner-confirmed; individual branch protection not yet mapped | Autopilot | Shares SW-002 with House and Windlass |
| [DC-WIN-01](/about/configuration/circuits/dc-win-01/) | **[CB-006](/about/configuration/equipment/cb-006/) fitted 70 A breaker** plus installed ANL scheme (2025 design called for 100 A ANL Windlass) | **[Lewmar HX1 800 W EQ-061](/about/configuration/equipment/eq-061/)** | Shares SW-002 with House and Pilot; via [contactor EQ-062](/about/configuration/equipment/eq-062/) controlled by two foredeck switches; physical ANL rating/order untraced |
| [DC-WIN-02](/about/configuration/circuits/dc-win-02/) | **Control fuse not verified**; Lewmar manufacturer standard includes 3 A control fuse | Two [foredeck switches SW-003](/about/configuration/equipment/sw-003/) and [SW-004](/about/configuration/equipment/sw-004/) actuating [contactor EQ-062](/about/configuration/equipment/eq-062/) → [HX1 EQ-061](/about/configuration/equipment/eq-061/) | Separate low-current control function; fitted coil wiring, direction mapping and fuse position untraced |

The 2025 Primary/Auxiliary/Watchkeeper/Winch ANL schedule must not be silently mapped to today's six service circuit names. **Unswitched does not mean unprotected.** Assign individual `FU-NNN` records when particular fitted fuses and ways have been positively identified.

## Navigation and deck lighting

| [DC-NAV-01](/about/configuration/circuits/dc-nav-01/) | [CB-001](/about/configuration/equipment/cb-001/) **10 A**, NAV LTS row 1 | EQ-021 — NASA Combi via SW-001 | Owner-confirmed 10 A and functional loads; DIN conductor paths not electrically traced |
| [DC-NAV-02](/about/configuration/circuits/dc-nav-02/) | [CB-002](/about/configuration/equipment/cb-002/) **10 A**, NAV LTS row 2 | EQ-020 — Osculati steaming function | Owner-confirmed 10 A and functional loads; DIN conductor paths not electrically traced |
| [DC-NAV-03](/about/configuration/circuits/dc-nav-03/) | [CB-004](/about/configuration/equipment/cb-004/) **10 A**, NAV LTS row 3 | EQ-020 — Osculati deck function, **same physical housing** | Owner-confirmed 10 A and functional loads; DIN conductor paths not electrically traced |
| [DC-NAV-04](/about/configuration/circuits/dc-nav-04/) | [CB-005](/about/configuration/equipment/cb-005/) **10 A**, NAV LTS row 4 | EQ-018 + EQ-019 — Osculati bow bicolour and stern LEDs | Owner-confirmed 10 A and functional loads; DIN conductor paths not electrically traced |

The NAV LTS panel contains four owner-confirmed **10 A** branch breakers. The separate steaming and deck circuits feed *different functions of the same Osculati fitting EQ-020*; the bow and stern each have a luminaire but **share CB-005**. The exact DIN terminal assignments beyond legacy notes, conductor sizes and return paths remain unverified.

## Communications power distribution

CB-003 protects the **DC-COM-01 feeder**. The **10 A / 3 A / 3 A branch fuses**, allocated as FU-001–FU-003, protect their respective outgoing circuits. **The 10 A VHF branch fuse equals the upstream 10 A breaker nominal rating**; selectivity is not established without fuse/breaker characteristics. EQ-057's fourth position is not confirmed as occupied or spare.

## NMEA 2000 power injection

| Circuit | Protection | Functional destination | Evidence / outstanding detail |
| --- | --- | --- | --- |
| [DC-N2K-01](/about/configuration/circuits/dc-n2k-01/) | [CB-007](/about/configuration/equipment/cb-007/) — one shared **10 A NAV INSTR breaker** | Common supply to A and B injection feeds | Owner-confirmed; split point and wiring untraced |
| [DC-N2K-02](/about/configuration/circuits/dc-n2k-02/) | Shared upstream CB-007; local fuse unknown | Segment A power injection behind DCP | Owner-confirmed functional feed; historical R1 alias untraced |
| [DC-N2K-03](/about/configuration/circuits/dc-n2k-03/) | Shared upstream CB-007; local fuse unknown | Segment B power injection behind DCP | Owner-confirmed functional feed; historical Y1 alias untraced |

The A/B power isolator separates positive supplies at the network interconnection; it does not give these two feeds independent upstream breaker protection. Local protective devices and conductor suitability have not been surveyed.
