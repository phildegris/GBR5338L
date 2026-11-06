---
title: "Equipment Register"
description: "Equipment and components identified from Ragtime’s DC Logical Circuits inventory"
date: 2026-10-31
summary: "Provisional equipment identifiers, locations and survey status for electrical and electronic equipment aboard Ragtime."
---

> **Inventory imported from the [DC Logical Circuits](/about/configuration/logical-circuits/) page; not an as-built survey.** The source lists equipment, possible devices and grouped loads. No make, model, wiring rating, physical presence or condition has been independently verified for this register.

This register uses the permanent equipment IDs in the [Electrical Reference System](/about/configuration/electrical-reference-system/). IDs identify *equipment*, not circuits or panel positions. Legacy physical designations remain as aliases. Circuit-to-protection relationships belong in the [Circuit Register](/about/configuration/circuit-register/), not in the equipment ID.

**Index status is generated from each equipment page's front matter, not maintained here.** `Mapped (U)` means the identity and functional connections have been documented from owner evidence, but the installation has **not been independently electrically surveyed**. `U` = identified or owner-confirmed but unverified as-built; `T` = tentative installation/proposal status; `G` = grouped equipment, individual count unconfirmed. Documentation progress and physical verification are separate dimensions.

[Browse the equipment catalogue](/about/configuration/equipment/) for one record per item, with manufacturer references and survey questions.

**Current inventory:** 82 register records (62 EQ, 4 BB, 6 CB, 3 FU, 4 SW, 3 TB). Four entries represent groups with unknown individual counts; all other records identify one candidate device or subassembly each. Two entries (`EQ-057` and `EQ-058`) were added from the owner's 31 October 2026 COM-frame clarification.

**Sources:** [DC Logical Circuits](/about/configuration/logical-circuits/) (original notes), plus owner-supplied updates on 31 October 2026. See the [COM-frame supply and RF overview](/about/configuration/com-frame/). Individual equipment IDs are independent of circuit and location IDs; unverified nameplates and electrical values remain open.

## DC distribution and controls

**House bank upstream source and returns:** [Source topology](/about/configuration/house-bank-distribution/) models the bank as one port, without implying the previous battery-design options are installed.

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-059`](/about/configuration/equipment/eq-059/) | [House-bank aggregated source interface](/about/configuration/equipment/eq-059/) | House-bank distribution; exact mounting unverified | {{< equipment-status id="EQ-059" >}} | Single logical two-terminal source boundary; internal batteries deferred. [Source diagram](/about/configuration/house-bank-distribution/). |
| [`BB-003`](/about/configuration/equipment/bb-003/) | [House-bank positive six-service distribution](/about/configuration/equipment/bb-003/) | House-bank distribution; exact mounting unverified | {{< equipment-status id="BB-003" >}} | Watchkeeper and pumps 1/2 bypass SW-002; House, Autopilot and Windlass switch together. ANL and battery-post fuses owner-confirmed fitted. [Source diagram](/about/configuration/house-bank-distribution/). |
| [`BB-004`](/about/configuration/equipment/bb-004/) | [DIY tinned-copper battery-negative link](/about/configuration/equipment/bb-004/) | House-bank distribution; exact mounting unverified | {{< equipment-status id="BB-004" >}} | Direct house battery negatives to the battery side of EQ-060 BMV shunt; dimensions not as-built measured. [Source diagram](/about/configuration/house-bank-distribution/). |
| [`EQ-061`](/about/configuration/equipment/eq-061/) | [Lewmar HX1 800 W windlass](/about/configuration/equipment/eq-061/) | Foredeck/anchor locker | {{< equipment-status id="EQ-061" >}} | Owner-confirmed fitted motor; [DC-WIN-01](/about/configuration/circuits/dc-win-01/), 70 A [CB-006](/about/configuration/equipment/cb-006/), separate [contactor EQ-062](/about/configuration/equipment/eq-062/) and two foredeck controls. |
| [`EQ-062`](/about/configuration/equipment/eq-062/) | [Windlass contactor](/about/configuration/equipment/eq-062/) | Windlass power/control installation; physical mounting unknown | {{< equipment-status id="EQ-062" >}} | Owner-confirmed separate contactor actuated by two foredeck controls; fitted part number unverified. |
| [`EQ-060`](/about/configuration/equipment/eq-060/) | [Victron BMV-712 battery monitor and shunt](/about/configuration/equipment/eq-060/) | House-bank distribution; exact mounting unverified | {{< equipment-status id="EQ-060" >}} | Owner-confirmed monitoring; only battery negatives on shunt battery side, system loads/charging returns on other. [Source diagram](/about/configuration/house-bank-distribution/). |
| [`EQ-001`](/about/configuration/equipment/eq-001/) | [Main DC panel (DCP)](/about/configuration/equipment/eq-001/) | Chart table | {{< equipment-status id="EQ-001" >}} | Parent panel assembly; individual breakers recorded separately. |
| [`EQ-002`](/about/configuration/equipment/eq-002/) | [NAV LTS four-breaker / yacht-outline panel](/about/configuration/equipment/eq-002/) | `CT-P`, upper-left Moody panel | {{< equipment-status id="EQ-002" >}} | Four **10 A** circuits identified; [NAV lighting diagram](/about/configuration/navigation-lights/). |
| [`BB-001`](/about/configuration/equipment/bb-001/) | [Main negative busbar](/about/configuration/equipment/bb-001/) | Aft engine-bay frame | {{< equipment-status id="BB-001" >}} | Legacy alias DC-BB-M; linked to engine block/battery negative according to source; capacity to check. |
| [`BB-002`](/about/configuration/equipment/bb-002/) | [DC panel negative busbar](/about/configuration/equipment/bb-002/) | DCP | {{< equipment-status id="BB-002" >}} | Legacy alias DC-BB-A; source records link to DC-BB-M; legacy cable condition/capacity to check. |
| [`CB-001`](/about/configuration/equipment/cb-001/) | [NAV masthead breaker, 10 A](/about/configuration/equipment/cb-001/) | NAV LTS row 1; alias 1,1 | {{< equipment-status id="CB-001" >}} | Owner confirms 10 A [DC-NAV-01](/about/configuration/circuits/dc-nav-01/) through SW-001 to NASA Combi. |
| [`CB-002`](/about/configuration/equipment/cb-002/) | [NAV steaming breaker, 10 A](/about/configuration/equipment/cb-002/) | NAV LTS row 2; alias 1,2 | {{< equipment-status id="CB-002" >}} | Owner confirms 10 A [DC-NAV-02](/about/configuration/circuits/dc-nav-02/) to Osculati combined fixture. |
| [`CB-004`](/about/configuration/equipment/cb-004/) | [10 A deck-light breaker](/about/configuration/equipment/cb-004/) | NAV LTS row 3 | {{< equipment-status id="CB-004" >}} | Owner confirms Osculati combined fitting's deck function, distinct 10 A breaker. [DC-NAV-03](/about/configuration/circuits/dc-nav-03/). |
| [`CB-006`](/about/configuration/equipment/cb-006/) | [Windlass fitted 70 A circuit breaker](/about/configuration/equipment/cb-006/) | Aft end of engine drive compartment, beneath aft cabin bunk (owner-confirmed) | {{< equipment-status id="CB-006" >}} | Fitted, owner-confirmed **70 A** circuit breaker on [DC-WIN-01](/about/configuration/circuits/dc-win-01/); distinct from fitted ANL fusing. |
| [`CB-005`](/about/configuration/equipment/cb-005/) | [10 A bow/stern navigation breaker](/about/configuration/equipment/cb-005/) | NAV LTS row 4 | {{< equipment-status id="CB-005" >}} | Owner confirms bow bicolour and stern LED both on this 10 A breaker. [DC-NAV-04](/about/configuration/circuits/dc-nav-04/). |
| [`CB-003`](/about/configuration/equipment/cb-003/) | [VHF AIS panel circuit breaker — 10 A](/about/configuration/equipment/cb-003/) | `CT-P`, position `3,4` | {{< equipment-status id="CB-003" >}} | Panel feeder breaker to COM frame; see [DC-COM-01](/about/configuration/circuits/dc-com-01/) for protection and outstanding checks. |
| [`SW-003`](/about/configuration/equipment/sw-003/) | [Foredeck windlass control switch A](/about/configuration/equipment/sw-003/) | Foredeck; exact position to survey | {{< equipment-status id="SW-003" >}} | One of two owner-confirmed foredeck windlass switches commanding EQ-062; direction unassigned. |
| [`SW-004`](/about/configuration/equipment/sw-004/) | [Foredeck windlass control switch B](/about/configuration/equipment/sw-004/) | Foredeck; exact position to survey | {{< equipment-status id="SW-004" >}} | Second owner-confirmed foredeck windlass switch commanding EQ-062; direction unassigned. |
| [`SW-002`](/about/configuration/equipment/sw-002/) | [House/Autopilot/Windlass shared remote battery switch](/about/configuration/equipment/sw-002/) | House-bank positive distribution; physical device location unverified | {{< equipment-status id="SW-002" >}} | **One common switching device** for House, Autopilot and Windlass; Watchkeeper and both pumps bypass. WhisperPower family visible in Aug 2025 image, exact installed model unknown. |
| [`SW-001`](/about/configuration/equipment/sw-001/) | [Masthead DPDT polarity-reversing selector](/about/configuration/equipment/sw-001/) | Exact mounting unconfirmed | {{< equipment-status id="SW-001" >}} | Owner confirms NASA Combi tricolour/anchor mode selection, SW-001 in DC-NAV-01; pinout untested. |
| [`TB-001`](/about/configuration/equipment/tb-001/) | [DIN Y/R/B cage-clamp group 2](/about/configuration/equipment/tb-001/) | Behind DCP | {{< equipment-status id="TB-001" >}} | Owner-confirmed positional convention: Y2/R2/B2 are three individual clamps; Y2 steaming, B2 NASA masthead from legacy notes; wiring not traced. |
| [`TB-002`](/about/configuration/equipment/tb-002/) | [DIN Y/R/B cage-clamp group 3](/about/configuration/equipment/tb-002/) | Behind DCP | {{< equipment-status id="TB-002" >}} | Owner-confirmed positional convention: Y3/R3/B3 are three individual clamps; Y3 routes black mast conductor per legacy notes; wiring not traced. |
| [`TB-003`](/about/configuration/equipment/tb-003/) | [Four-way connector block](/about/configuration/equipment/tb-003/) | Unsurveyed | {{< equipment-status id="TB-003" >}} | Source notes a 4-way connector on the DPDT 2 to DC-BB-A path; verify identity/location. |

## Communications

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-003`](/about/configuration/equipment/eq-003/) | [Icom IC-M510 VHF transceiver](/about/configuration/equipment/eq-003/) | `SL-COM` — COM frame (saloon, starboard-forward) | {{< equipment-status id="EQ-003" >}} | COM-frame VHF; see [DC and RF connections](/about/configuration/com-frame/) and the equipment record for open survey items. |
| [`EQ-004`](/about/configuration/equipment/eq-004/) | [Ocean Signal ATB1 AIS transponder](/about/configuration/equipment/eq-004/) | `SL-COM` — COM frame (saloon, starboard-forward) | {{< equipment-status id="EQ-004" >}} | COM-frame AIS; see [DC and RF connections](/about/configuration/com-frame/) and the equipment record for open survey items. |
| [`EQ-005`](/about/configuration/equipment/eq-005/) | [Digital Yacht SPL2000 AIS/VHF splitter (owner-confirmed)](/about/configuration/equipment/eq-005/) | `SL-COM` — COM frame (saloon, starboard-forward) | {{< equipment-status id="EQ-005" >}} | COM-frame antenna splitter; see [DC and RF connections](/about/configuration/com-frame/) and the equipment record for open survey items. |
| [`EQ-057`](/about/configuration/equipment/eq-057/) | [COM-frame four-way FC fuse board](/about/configuration/equipment/eq-057/) | `SL-COM` — COM frame (saloon, starboard-forward) | {{< equipment-status id="EQ-057" >}} | COM-frame fused distribution; see [DC diagram](/about/configuration/com-frame/) and the equipment record for fuse-board survey items. |
| [`FU-001`](/about/configuration/equipment/fu-001/) | [COM-frame fuse way 1, 10 A, Icom M510 VHF](/about/configuration/equipment/fu-001/) | `SL-COM`, EQ-057 way 1 | {{< equipment-status id="FU-001" >}} | COM-frame VHF branch; see [DC-COM-02](/about/configuration/circuits/dc-com-02/) and the equipment record for fuse type and wiring. |
| [`FU-002`](/about/configuration/equipment/fu-002/) | [COM-frame fuse way 2, 3 A, Digital Yacht SPL2000](/about/configuration/equipment/fu-002/) | `SL-COM`, EQ-057 way 2 | {{< equipment-status id="FU-002" >}} | COM-frame SPL2000 branch; see [DC-COM-03](/about/configuration/circuits/dc-com-03/) and the equipment record for fuse type and wiring. |
| [`FU-003`](/about/configuration/equipment/fu-003/) | [COM-frame fuse way 3, 3 A, Ocean Signal ATB1](/about/configuration/equipment/fu-003/) | `SL-COM`, EQ-057 way 3 | {{< equipment-status id="FU-003" >}} | COM-frame ATB1 branch; see [DC-COM-04](/about/configuration/circuits/dc-com-04/) and the equipment record for fuse type and wiring. |
| [`EQ-058`](/about/configuration/equipment/eq-058/) | [Vesper Marine VA159 masthead VHF/AIS antenna](/about/configuration/equipment/eq-058/) | `MS-T` — masthead | {{< equipment-status id="EQ-058" >}} | Masthead VHF/AIS antenna; see [RF diagram](/about/configuration/com-frame/) and the equipment record for measurement backlog. |

## Charging outlets / devices

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-006`](/about/configuration/equipment/eq-006/) | [Handheld VHF charging point](/about/configuration/equipment/eq-006/) | Unsurveyed | {{< equipment-status id="EQ-006" >}} | Source: Handheld VHF under Charging; determine charger versus socket. |
| [`EQ-007`](/about/configuration/equipment/eq-007/) | [Instrument-panel charging point](/about/configuration/equipment/eq-007/) | Instrument panel | {{< equipment-status id="EQ-007" >}} | Source: Instrument Panel under Charging. |
| [`EQ-008`](/about/configuration/equipment/eq-008/) | [Companionway charging point](/about/configuration/equipment/eq-008/) | Companionway | {{< equipment-status id="EQ-008" >}} | Source: Companionway under Charging. |
| [`EQ-009`](/about/configuration/equipment/eq-009/) | [Pedestal magnetic-mount charging point](/about/configuration/equipment/eq-009/) | Pedestal | {{< equipment-status id="EQ-009" >}} | Source: Pedestal Mag Mount under Charging. |
| [`EQ-010`](/about/configuration/equipment/eq-010/) | [Navigation-station cave charging point 1](/about/configuration/equipment/eq-010/) | Nav station cave | {{< equipment-status id="EQ-010" >}} | Source explicitly states x4; provisional item 1 of 4. |
| [`EQ-011`](/about/configuration/equipment/eq-011/) | [Navigation-station cave charging point 2](/about/configuration/equipment/eq-011/) | Nav station cave | {{< equipment-status id="EQ-011" >}} | Source explicitly states x4; provisional item 2 of 4. |
| [`EQ-012`](/about/configuration/equipment/eq-012/) | [Navigation-station cave charging point 3](/about/configuration/equipment/eq-012/) | Nav station cave | {{< equipment-status id="EQ-012" >}} | Source explicitly states x4; provisional item 3 of 4. |
| [`EQ-013`](/about/configuration/equipment/eq-013/) | [Navigation-station cave charging point 4](/about/configuration/equipment/eq-013/) | Nav station cave | {{< equipment-status id="EQ-013" >}} | Source explicitly states x4; provisional item 4 of 4. |
| [`EQ-014`](/about/configuration/equipment/eq-014/) | [Navigation-station hutch charging point 1](/about/configuration/equipment/eq-014/) | Nav station hutch | {{< equipment-status id="EQ-014" >}} | Source explicitly states x2; provisional item 1 of 2. |
| [`EQ-015`](/about/configuration/equipment/eq-015/) | [Navigation-station hutch charging point 2](/about/configuration/equipment/eq-015/) | Nav station hutch | {{< equipment-status id="EQ-015" >}} | Source explicitly states x2; provisional item 2 of 2. |
| [`EQ-016`](/about/configuration/equipment/eq-016/) | [Forward-cabin charging point](/about/configuration/equipment/eq-016/) | Fore cabin | {{< equipment-status id="EQ-016" >}} | Source: Fore Cabin under Charging. |
| [`EQ-017`](/about/configuration/equipment/eq-017/) | [Aft-cabin charging point](/about/configuration/equipment/eq-017/) | Aft cabin | {{< equipment-status id="EQ-017" >}} | Source: Aft Cabin under Charging. |

## Topside and navigation lighting

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-018`](/about/configuration/equipment/eq-018/) | [Osculati bow bicolour LED](/about/configuration/equipment/eq-018/) | Bow | {{< equipment-status id="EQ-018" >}} | Owner confirms [DC-NAV-04](/about/configuration/circuits/dc-nav-04/) shared with EQ-019; CB-005 10 A. |
| [`EQ-019`](/about/configuration/equipment/eq-019/) | [Osculati stern LED light](/about/configuration/equipment/eq-019/) | Stern | {{< equipment-status id="EQ-019" >}} | Owner confirms [DC-NAV-04](/about/configuration/circuits/dc-nav-04/) shared with EQ-018; CB-005 10 A. |
| [`EQ-020`](/about/configuration/equipment/eq-020/) | [Osculati 13.243.88 combined steaming/deck LED](/about/configuration/equipment/eq-020/) | Mast (height unconfirmed) | {{< equipment-status id="EQ-020" >}} | **Osculati 13.243.88 installed model owner-confirmed**; separate 10 A steaming and deck circuits, one physical housing; wiring not electrically verified. |
| [`EQ-021`](/about/configuration/equipment/eq-021/) | [NASA Marine Combi masthead tricolour/anchor LED](/about/configuration/equipment/eq-021/) | Masthead | {{< equipment-status id="EQ-021" >}} | One polarity-switched dual-mode LED fed via SW-001; breaker CB-001 10 A; model suffix unverified. |
| [`EQ-022`](/about/configuration/equipment/eq-022/) | [Legacy deck-lights group (not an additional confirmed fitting)](/about/configuration/equipment/eq-022/) | Unreconciled historical grouping | {{< equipment-status id="EQ-022" >}} | Known deck-light function belongs to EQ-020; further separate fittings unconfirmed. |
| [`EQ-023`](/about/configuration/equipment/eq-023/) | [Compass light](/about/configuration/equipment/eq-023/) | Compass (position unsurveyed) | {{< equipment-status id="EQ-023" >}} | Source: Compass Light. |
| [`EQ-024`](/about/configuration/equipment/eq-024/) | [Cockpit light](/about/configuration/equipment/eq-024/) | Cockpit | {{< equipment-status id="EQ-024" >}} | Bracketed [Cockpit Light] in source; presence and plan status unconfirmed. |
| [`EQ-025`](/about/configuration/equipment/eq-025/) | [Boom light](/about/configuration/equipment/eq-025/) | Boom | {{< equipment-status id="EQ-025" >}} | Bracketed [Boom Light] in source; presence and plan status unconfirmed. |

## Fresh-water equipment

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-026`](/about/configuration/equipment/eq-026/) | [Fresh-water supply pump](/about/configuration/equipment/eq-026/) | Unsurveyed | {{< equipment-status id="EQ-026" >}} | Source: Supply Pump. |
| [`EQ-027`](/about/configuration/equipment/eq-027/) | [Shower drain pump](/about/configuration/equipment/eq-027/) | Unsurveyed | {{< equipment-status id="EQ-027" >}} | Source: Shower Drain Pump. |
| [`EQ-028`](/about/configuration/equipment/eq-028/) | [Fresh-water tank level sensor](/about/configuration/equipment/eq-028/) | Unsurveyed | {{< equipment-status id="EQ-028" >}} | Source: Tank Level Sensor. |
| [`EQ-029`](/about/configuration/equipment/eq-029/) | [Fresh-water level indicator panel](/about/configuration/equipment/eq-029/) | Unsurveyed | {{< equipment-status id="EQ-029" >}} | Source: Tank Level Indicator Panel. |

## Bilge equipment

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-030`](/about/configuration/equipment/eq-030/) | [Bilge pump A](/about/configuration/equipment/eq-030/) | Bilge (exact position unsurveyed) | {{< equipment-status id="EQ-030" >}} | Bracketed [Pump A]; location and physical identity to confirm. |
| [`EQ-031`](/about/configuration/equipment/eq-031/) | [Bilge pump B](/about/configuration/equipment/eq-031/) | Bilge (exact position unsurveyed) | {{< equipment-status id="EQ-031" >}} | Bracketed [Pump B]; location and physical identity to confirm. |

## Engine-compartment equipment

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-032`](/about/configuration/equipment/eq-032/) | [Engine compartment extractor fan](/about/configuration/equipment/eq-032/) | Engine compartment | {{< equipment-status id="EQ-032" >}} | Source: Extractor Fan. |
| [`EQ-033`](/about/configuration/equipment/eq-033/) | [Engine compartment forward striplight](/about/configuration/equipment/eq-033/) | Engine compartment, forward | {{< equipment-status id="EQ-033" >}} | Source: Forward Striplight. |
| [`EQ-034`](/about/configuration/equipment/eq-034/) | [Engine compartment aft striplight](/about/configuration/equipment/eq-034/) | Engine compartment, aft | {{< equipment-status id="EQ-034" >}} | Source: Aft Striplight. |
| [`EQ-035`](/about/configuration/equipment/eq-035/) | [Engine compartment sensor node](/about/configuration/equipment/eq-035/) | Engine compartment | {{< equipment-status id="EQ-035" >}} | Bracketed [Sensor Node]; physical presence unconfirmed. |

## Local area network

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-036`](/about/configuration/equipment/eq-036/) | [RUTX50 router](/about/configuration/equipment/eq-036/) | Unsurveyed | {{< equipment-status id="EQ-036" >}} | Source: RUTX50; no other identifying particulars assumed. |
| [`EQ-037`](/about/configuration/equipment/eq-037/) | [LAN network switch](/about/configuration/equipment/eq-037/) | Unsurveyed | {{< equipment-status id="EQ-037" >}} | Source: Switch in Local Area Network group, not a DC control switch. |
| [`EQ-038`](/about/configuration/equipment/eq-038/) | [Odroid N2 computer](/about/configuration/equipment/eq-038/) | Unsurveyed | {{< equipment-status id="EQ-038" >}} | Source: Odroid N2. |
| [`EQ-039`](/about/configuration/equipment/eq-039/) | [LAN monitor](/about/configuration/equipment/eq-039/) | Unsurveyed | {{< equipment-status id="EQ-039" >}} | Source: Monitor under Local Area Network. |

## Wide area network

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-040`](/about/configuration/equipment/eq-040/) | [TRB500 mobile network device](/about/configuration/equipment/eq-040/) | Unsurveyed | {{< equipment-status id="EQ-040" >}} | Source: TRB500; associated 30 W PoE injector. |
| [`EQ-041`](/about/configuration/equipment/eq-041/) | [30 W PoE injector](/about/configuration/equipment/eq-041/) | Unsurveyed | {{< equipment-status id="EQ-041" >}} | Source: 30w PoE Injector on TRB500 path; stated value not independently verified. |
| [`EQ-042`](/about/configuration/equipment/eq-042/) | [Starlink terminal](/about/configuration/equipment/eq-042/) | Unsurveyed | {{< equipment-status id="EQ-042" >}} | Source: Starlink; associated 150 W PoE injector. |
| [`EQ-043`](/about/configuration/equipment/eq-043/) | [150 W PoE injector](/about/configuration/equipment/eq-043/) | Unsurveyed | {{< equipment-status id="EQ-043" >}} | Source: 150w POE Injector on Starlink path; stated value not independently verified. |

## Entertainment

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-044`](/about/configuration/equipment/eq-044/) | [TV](/about/configuration/equipment/eq-044/) | Unsurveyed | {{< equipment-status id="EQ-044" >}} | Source: TV. |
| [`EQ-045`](/about/configuration/equipment/eq-045/) | [Radio / media player](/about/configuration/equipment/eq-045/) | Unsurveyed | {{< equipment-status id="EQ-045" >}} | Bracketed [Radio/Media Player]; presence unconfirmed. |

## Interior and compartment lighting

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-046`](/about/configuration/equipment/eq-046/) | [Forward-cabin downlights (group)](/about/configuration/equipment/eq-046/) | Fore cabin | {{< equipment-status id="EQ-046" >}} | Quantity unknown; individual lights not yet itemised. |
| [`EQ-047`](/about/configuration/equipment/eq-047/) | [Saloon downlights (group)](/about/configuration/equipment/eq-047/) | Saloon | {{< equipment-status id="EQ-047" >}} | Quantity unknown; individual lights not yet itemised. |
| [`EQ-048`](/about/configuration/equipment/eq-048/) | [Saloon starboard bunk reading light / USB](/about/configuration/equipment/eq-048/) | Saloon, starboard bunk | {{< equipment-status id="EQ-048" >}} | Source explicitly names starboard bunk. |
| [`EQ-049`](/about/configuration/equipment/eq-049/) | [Saloon port bunk reading light / USB](/about/configuration/equipment/eq-049/) | Saloon, port bunk | {{< equipment-status id="EQ-049" >}} | Source explicitly names port bunk. |
| [`EQ-050`](/about/configuration/equipment/eq-050/) | [Aft-cabin downlights (group)](/about/configuration/equipment/eq-050/) | Aft cabin | {{< equipment-status id="EQ-050" >}} | Quantity unknown; individual lights not yet itemised. |
| [`EQ-051`](/about/configuration/equipment/eq-051/) | [Aft-cabin striplight](/about/configuration/equipment/eq-051/) | Aft cabin | {{< equipment-status id="EQ-051" >}} | Source: Striplight. |
| [`EQ-052`](/about/configuration/equipment/eq-052/) | [Aft-cabin port bunk reading light / USB](/about/configuration/equipment/eq-052/) | Aft cabin, port bunk | {{< equipment-status id="EQ-052" >}} | Source: Port Bunk Reading Light/USB. |
| [`EQ-053`](/about/configuration/equipment/eq-053/) | [Aft-cabin other bunk reading light / USB](/about/configuration/equipment/eq-053/) | Aft cabin, bunk not specified | {{< equipment-status id="EQ-053" >}} | Source separately lists Bunk Reading Light/USB; do not infer starboard until surveyed. |
| [`EQ-054`](/about/configuration/equipment/eq-054/) | [Heads striplight](/about/configuration/equipment/eq-054/) | Heads | {{< equipment-status id="EQ-054" >}} | Source: Striplight. |
| [`EQ-055`](/about/configuration/equipment/eq-055/) | [Navigation-station red/white striplight](/about/configuration/equipment/eq-055/) | Nav station | {{< equipment-status id="EQ-055" >}} | Source: Striplight (Red/White). |
| [`EQ-056`](/about/configuration/equipment/eq-056/) | [Galley striplight](/about/configuration/equipment/eq-056/) | Galley | {{< equipment-status id="EQ-056" >}} | Source: Striplight. |

## Outstanding distinctions and survey actions

- The combined **masthead anchor/tricolour lamp is one physical item** with two modes, not two independent lights. The steering, navigation and electrical circuits should link to its single equipment ID.
- **NMEA2000 A and NMEA2000 B** are **two segments of one NMEA 2000 network**, with **power injection for both behind DCP** (owner-confirmed, 6 November 2026), not individual devices or two established separate networks. See the [network and power record](/about/configuration/nmea2000-configuration/). A [power isolator (EQ-063)](/about/configuration/equipment/eq-063/) passes CAN data and separates the segment positive supplies (owner-confirmed). Source circuits, protection, isolator model/location, backbone components and connected instruments remain to be documented; no fictitious equipment records have been created for the segment labels.
- **Seven-core cable and conductor colours** describe wiring, not equipment. The source gives blue, black and yellow cores for particular lighting paths; retain these in a future Circuit Register without turning each conductor into equipment.
- The source refers to a **battery negative** and an **engine block** as return connection points but does not identify an individual battery or complete engine. Do not allocate a battery/engine asset ID from those incidental references until surveyed.
- Verify whether the navigation-lights illuminated panel section and the four-way connector are distinct serviceable components, and whether terminal aliases `B2`, `Y2` and `Y3` map to the assumed DIN block numbers. Preserve physical aliases even if the interpretation changes.
- Identify each downlight and deck light individually, confirm tentative bracketed entries, capture physical locations, models, serials and photographs, and record survey dates before marking anything as verified.


## NMEA 2000 network hardware

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-063`](/about/configuration/equipment/eq-063/) | [NMEA 2000 segment A/B power isolator](/about/configuration/equipment/eq-063/) | Not yet reported | {{< equipment-status id="EQ-063" >}} | Owner confirms CAN data passes and positive supplies are separated; model and physical location pending. |
| [`EQ-064`](/about/configuration/equipment/eq-064/) | [Yacht Devices YDWG-02 wireless gateway](/about/configuration/equipment/eq-064/) | Not yet reported | {{< equipment-status id="EQ-064" >}} | Segment A data and bus power, owner-confirmed 6 November 2026; exact variant, load and drop route pending. |
