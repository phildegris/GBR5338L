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

**Current inventory:** 70 register records (58 EQ, 2 BB, 3 CB, 3 FU, 1 SW, 3 TB). Four entries represent groups with unknown individual counts; all other records identify one candidate device or subassembly each. Two entries (`EQ-057` and `EQ-058`) were added from the owner's 31 October 2026 COM-frame clarification.

**Sources:** [DC Logical Circuits](/about/configuration/logical-circuits/) (original notes), plus owner-supplied updates on 31 October 2026. See the [COM-frame supply and RF overview](/about/configuration/com-frame/). Individual equipment IDs are independent of circuit and location IDs; unverified nameplates and electrical values remain open.

## DC distribution and controls

| ID | Equipment | Reported location | Status | Source / survey note |
| --- | --- | --- | :---: | --- |
| [`EQ-001`](/about/configuration/equipment/eq-001/) | [Main DC panel (DCP)](/about/configuration/equipment/eq-001/) | Chart table | {{< equipment-status id="EQ-001" >}} | Parent panel assembly; individual breakers recorded separately. |
| [`EQ-002`](/about/configuration/equipment/eq-002/) | [Navigation-lights illuminated graphic/control section](/about/configuration/equipment/eq-002/) | DCP | {{< equipment-status id="EQ-002" >}} | Panel section labelled NAV LTS; verify whether separately serviceable. |
| [`BB-001`](/about/configuration/equipment/bb-001/) | [Main negative busbar](/about/configuration/equipment/bb-001/) | Aft engine-bay frame | {{< equipment-status id="BB-001" >}} | Legacy alias DC-BB-M; linked to engine block/battery negative according to source; capacity to check. |
| [`BB-002`](/about/configuration/equipment/bb-002/) | [DC panel negative busbar](/about/configuration/equipment/bb-002/) | DCP | {{< equipment-status id="BB-002" >}} | Legacy alias DC-BB-A; source records link to DC-BB-M; legacy cable condition/capacity to check. |
| [`CB-001`](/about/configuration/equipment/cb-001/) | [Masthead-light circuit breaker](/about/configuration/equipment/cb-001/) | DCP, position 1,1 | {{< equipment-status id="CB-001" >}} | Physical alias Breaker 1,1; source traces to DPDT selector; rating unknown. |
| [`CB-002`](/about/configuration/equipment/cb-002/) | [Steaming-light circuit breaker](/about/configuration/equipment/cb-002/) | DCP, position 1,2 | {{< equipment-status id="CB-002" >}} | Physical alias Breaker 1,2; source traces via Y2; rating unknown. |
| [`CB-003`](/about/configuration/equipment/cb-003/) | [VHF AIS panel circuit breaker — 10 A](/about/configuration/equipment/cb-003/) | `CT-P`, position `3,4` | {{< equipment-status id="CB-003" >}} | Panel feeder breaker to COM frame; see [DC-COM-01](/about/configuration/circuits/dc-com-01/) for protection and outstanding checks. |
| [`SW-001`](/about/configuration/equipment/sw-001/) | [Masthead anchor/tricolour polarity selector](/about/configuration/equipment/sw-001/) | Unsurveyed | {{< equipment-status id="SW-001" >}} | DPDT On-Off-On switch; source pin numbers 1–6; feeds combined masthead lamp. |
| [`TB-001`](/about/configuration/equipment/tb-001/) | [DIN connector block no. 2](/about/configuration/equipment/tb-001/) | Behind DCP | {{< equipment-status id="TB-001" >}} | Source terminal aliases B2 (masthead) and Y2 (steaming); interpreted as colour positions on block 2, verify. |
| [`TB-002`](/about/configuration/equipment/tb-002/) | [DIN connector block no. 3](/about/configuration/equipment/tb-002/) | Behind DCP | {{< equipment-status id="TB-002" >}} | Source terminal alias Y3 (masthead); verify physical block. |
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
| [`EQ-018`](/about/configuration/equipment/eq-018/) | [Bow navigation light](/about/configuration/equipment/eq-018/) | Bow | {{< equipment-status id="EQ-018" >}} | Source: Bow. |
| [`EQ-019`](/about/configuration/equipment/eq-019/) | [Stern navigation light](/about/configuration/equipment/eq-019/) | Stern | {{< equipment-status id="EQ-019" >}} | Source: Stern. |
| [`EQ-020`](/about/configuration/equipment/eq-020/) | [Steaming light](/about/configuration/equipment/eq-020/) | Unsurveyed | {{< equipment-status id="EQ-020" >}} | Source: Steaming; linked to Breaker 1,2 via terminal Y2, seven-core yellow conductor. |
| [`EQ-021`](/about/configuration/equipment/eq-021/) | [Combined masthead tricolour/anchor light](/about/configuration/equipment/eq-021/) | Masthead | {{< equipment-status id="EQ-021" >}} | One dual-mode physical lamp in circuit notes, not separate tricolour and anchor devices; switched by polarity. |
| [`EQ-022`](/about/configuration/equipment/eq-022/) | [Deck lights (group)](/about/configuration/equipment/eq-022/) | Unsurveyed | {{< equipment-status id="EQ-022" >}} | Source uses plural; number and individual mounting points unknown. |
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
- **NMEA2000 A and NMEA2000 B** are listed under Instruments in the source but describe two networks, not individual devices. Their power feeds, backbone components and connected instruments require a separate network/circuit inventory; no fictitious equipment records have been created for the networks themselves.
- **Seven-core cable and conductor colours** describe wiring, not equipment. The source gives blue, black and yellow cores for particular lighting paths; retain these in a future Circuit Register without turning each conductor into equipment.
- The source refers to a **battery negative** and an **engine block** as return connection points but does not identify an individual battery or complete engine. Do not allocate a battery/engine asset ID from those incidental references until surveyed.
- Verify whether the navigation-lights illuminated panel section and the four-way connector are distinct serviceable components, and whether terminal aliases `B2`, `Y2` and `Y3` map to the assumed DIN block numbers. Preserve physical aliases even if the interpretation changes.
- Identify each downlight and deck light individually, confirm tentative bracketed entries, capture physical locations, models, serials and photographs, and record survey dates before marking anything as verified.

