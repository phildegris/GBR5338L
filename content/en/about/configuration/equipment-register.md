---
title: "Equipment Register"
description: "Equipment and components identified from Ragtime’s DC Logical Circuits inventory"
date: 2026-10-31
summary: "Provisional equipment identifiers, locations and survey status for electrical and electronic equipment aboard Ragtime."
---

> **Inventory imported from the [DC Logical Circuits](/about/configuration/logical-circuits/) page; not an as-built survey.** The source lists equipment, possible devices and grouped loads. No make, model, wiring rating, physical presence or condition has been independently verified for this register.

This register uses the permanent equipment IDs proposed in the [Electrical Reference System](/about/configuration/electrical-reference-system/). IDs identify *equipment*, not circuits or panel positions. Legacy breaker, busbar and terminal designations are retained in the notes. Circuit protection belongs in a future Circuit Register rather than being inferred from this inventory.

**Survey state:** `U` = mentioned on the source page; not physically verified. `T` = tentative bracketed entry; installation or proposal status unknown. `G` = grouped equipment with unspecified individual quantity; a survey must allocate separate IDs to actual devices. These are *documentation states*, not proof of installation.

**Current inventory:** 64 register records (56 EQ, 2 BB, 2 CB, 1 SW, 3 TB). Four entries represent groups with unknown individual counts; all other records identify one candidate device or subassembly each.

**Source:** [DC Logical Circuits](/about/configuration/logical-circuits/) (original notes, including physical connection aliases). The equipment names below are functional descriptions; product identity and serial numbers remain to be surveyed.

## DC distribution and controls

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-001` | Main DC panel (DCP) | Chart table | `U` | Parent panel assembly; individual breakers recorded separately. |
| `EQ-002` | Navigation-lights illuminated graphic/control section | DCP | `U` | Panel section labelled NAV LTS; verify whether separately serviceable. |
| `BB-001` | Main negative busbar | Aft engine-bay frame | `U` | Legacy alias DC-BB-M; linked to engine block/battery negative according to source; capacity to check. |
| `BB-002` | DC panel negative busbar | DCP | `U` | Legacy alias DC-BB-A; source records link to DC-BB-M; legacy cable condition/capacity to check. |
| `CB-001` | Masthead-light circuit breaker | DCP, position 1,1 | `U` | Physical alias Breaker 1,1; source traces to DPDT selector; rating unknown. |
| `CB-002` | Steaming-light circuit breaker | DCP, position 1,2 | `U` | Physical alias Breaker 1,2; source traces via Y2; rating unknown. |
| `SW-001` | Masthead anchor/tricolour polarity selector | Unsurveyed | `U` | DPDT On-Off-On switch; source pin numbers 1–6; feeds combined masthead lamp. |
| `TB-001` | DIN connector block no. 2 | Behind DCP | `U` | Source terminal aliases B2 (masthead) and Y2 (steaming); interpreted as colour positions on block 2, verify. |
| `TB-002` | DIN connector block no. 3 | Behind DCP | `U` | Source terminal alias Y3 (masthead); verify physical block. |
| `TB-003` | Four-way connector block | Unsurveyed | `U` | Source notes a 4-way connector on the DPDT 2 to DC-BB-A path; verify identity/location. |

## Communications

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-003` | Radio transceiver | Unsurveyed | `U` | Source: Tranciever; make/model not stated. |
| `EQ-004` | AIS equipment | Unsurveyed | `U` | Source: AIS; device identity not stated. |
| `EQ-005` | Communications splitter | Unsurveyed | `U` | Source: Splitter; type/model unverified. |

## Charging outlets / devices

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-006` | Handheld VHF charging point | Unsurveyed | `U` | Source: Handheld VHF under Charging; determine charger versus socket. |
| `EQ-007` | Instrument-panel charging point | Instrument panel | `U` | Source: Instrument Panel under Charging. |
| `EQ-008` | Companionway charging point | Companionway | `U` | Source: Companionway under Charging. |
| `EQ-009` | Pedestal magnetic-mount charging point | Pedestal | `U` | Source: Pedestal Mag Mount under Charging. |
| `EQ-010` | Navigation-station cave charging point 1 | Nav station cave | `U` | Source explicitly states x4; provisional item 1 of 4. |
| `EQ-011` | Navigation-station cave charging point 2 | Nav station cave | `U` | Source explicitly states x4; provisional item 2 of 4. |
| `EQ-012` | Navigation-station cave charging point 3 | Nav station cave | `U` | Source explicitly states x4; provisional item 3 of 4. |
| `EQ-013` | Navigation-station cave charging point 4 | Nav station cave | `U` | Source explicitly states x4; provisional item 4 of 4. |
| `EQ-014` | Navigation-station hutch charging point 1 | Nav station hutch | `U` | Source explicitly states x2; provisional item 1 of 2. |
| `EQ-015` | Navigation-station hutch charging point 2 | Nav station hutch | `U` | Source explicitly states x2; provisional item 2 of 2. |
| `EQ-016` | Forward-cabin charging point | Fore cabin | `U` | Source: Fore Cabin under Charging. |
| `EQ-017` | Aft-cabin charging point | Aft cabin | `U` | Source: Aft Cabin under Charging. |

## Topside and navigation lighting

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-018` | Bow navigation light | Bow | `U` | Source: Bow. |
| `EQ-019` | Stern navigation light | Stern | `U` | Source: Stern. |
| `EQ-020` | Steaming light | Unsurveyed | `U` | Source: Steaming; linked to Breaker 1,2 via terminal Y2, seven-core yellow conductor. |
| `EQ-021` | Combined masthead tricolour/anchor light | Masthead | `U` | One dual-mode physical lamp in circuit notes, not separate tricolour and anchor devices; switched by polarity. |
| `EQ-022` | Deck lights (group) | Unsurveyed | `G` | Source uses plural; number and individual mounting points unknown. |
| `EQ-023` | Compass light | Compass (position unsurveyed) | `U` | Source: Compass Light. |
| `EQ-024` | Cockpit light | Cockpit | `T` | Bracketed [Cockpit Light] in source; presence and plan status unconfirmed. |
| `EQ-025` | Boom light | Boom | `T` | Bracketed [Boom Light] in source; presence and plan status unconfirmed. |

## Fresh-water equipment

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-026` | Fresh-water supply pump | Unsurveyed | `U` | Source: Supply Pump. |
| `EQ-027` | Shower drain pump | Unsurveyed | `U` | Source: Shower Drain Pump. |
| `EQ-028` | Fresh-water tank level sensor | Unsurveyed | `U` | Source: Tank Level Sensor. |
| `EQ-029` | Fresh-water level indicator panel | Unsurveyed | `U` | Source: Tank Level Indicator Panel. |

## Bilge equipment

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-030` | Bilge pump A | Bilge (exact position unsurveyed) | `T` | Bracketed [Pump A]; location and physical identity to confirm. |
| `EQ-031` | Bilge pump B | Bilge (exact position unsurveyed) | `T` | Bracketed [Pump B]; location and physical identity to confirm. |

## Engine-compartment equipment

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-032` | Engine compartment extractor fan | Engine compartment | `U` | Source: Extractor Fan. |
| `EQ-033` | Engine compartment forward striplight | Engine compartment, forward | `U` | Source: Forward Striplight. |
| `EQ-034` | Engine compartment aft striplight | Engine compartment, aft | `U` | Source: Aft Striplight. |
| `EQ-035` | Engine compartment sensor node | Engine compartment | `T` | Bracketed [Sensor Node]; physical presence unconfirmed. |

## Local area network

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-036` | RUTX50 router | Unsurveyed | `U` | Source: RUTX50; no other identifying particulars assumed. |
| `EQ-037` | LAN network switch | Unsurveyed | `U` | Source: Switch in Local Area Network group, not a DC control switch. |
| `EQ-038` | Odroid N2 computer | Unsurveyed | `U` | Source: Odroid N2. |
| `EQ-039` | LAN monitor | Unsurveyed | `U` | Source: Monitor under Local Area Network. |

## Wide area network

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-040` | TRB500 mobile network device | Unsurveyed | `U` | Source: TRB500; associated 30 W PoE injector. |
| `EQ-041` | 30 W PoE injector | Unsurveyed | `U` | Source: 30w PoE Injector on TRB500 path; stated value not independently verified. |
| `EQ-042` | Starlink terminal | Unsurveyed | `U` | Source: Starlink; associated 150 W PoE injector. |
| `EQ-043` | 150 W PoE injector | Unsurveyed | `U` | Source: 150w POE Injector on Starlink path; stated value not independently verified. |

## Entertainment

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-044` | TV | Unsurveyed | `U` | Source: TV. |
| `EQ-045` | Radio / media player | Unsurveyed | `T` | Bracketed [Radio/Media Player]; presence unconfirmed. |

## Interior and compartment lighting

| ID | Equipment | Reported location | State | Source / survey note |
| --- | --- | --- | :---: | --- |
| `EQ-046` | Forward-cabin downlights (group) | Fore cabin | `G` | Quantity unknown; individual lights not yet itemised. |
| `EQ-047` | Saloon downlights (group) | Saloon | `G` | Quantity unknown; individual lights not yet itemised. |
| `EQ-048` | Saloon starboard bunk reading light / USB | Saloon, starboard bunk | `U` | Source explicitly names starboard bunk. |
| `EQ-049` | Saloon port bunk reading light / USB | Saloon, port bunk | `U` | Source explicitly names port bunk. |
| `EQ-050` | Aft-cabin downlights (group) | Aft cabin | `G` | Quantity unknown; individual lights not yet itemised. |
| `EQ-051` | Aft-cabin striplight | Aft cabin | `U` | Source: Striplight. |
| `EQ-052` | Aft-cabin port bunk reading light / USB | Aft cabin, port bunk | `U` | Source: Port Bunk Reading Light/USB. |
| `EQ-053` | Aft-cabin other bunk reading light / USB | Aft cabin, bunk not specified | `U` | Source separately lists Bunk Reading Light/USB; do not infer starboard until surveyed. |
| `EQ-054` | Heads striplight | Heads | `U` | Source: Striplight. |
| `EQ-055` | Navigation-station red/white striplight | Nav station | `U` | Source: Striplight (Red/White). |
| `EQ-056` | Galley striplight | Galley | `U` | Source: Striplight. |

## Outstanding distinctions and survey actions

- The combined **masthead anchor/tricolour lamp is one physical item** with two modes, not two independent lights. The steering, navigation and electrical circuits should link to its single equipment ID.
- **NMEA2000 A and NMEA2000 B** are listed under Instruments in the source but describe two networks, not individual devices. Their power feeds, backbone components and connected instruments require a separate network/circuit inventory; no fictitious equipment records have been created for the networks themselves.
- **Seven-core cable and conductor colours** describe wiring, not equipment. The source gives blue, black and yellow cores for particular lighting paths; retain these in a future Circuit Register without turning each conductor into equipment.
- The source refers to a **battery negative** and an **engine block** as return connection points but does not identify an individual battery or complete engine. Do not allocate a battery/engine asset ID from those incidental references until surveyed.
- Verify whether the navigation-lights illuminated panel section and the four-way connector are distinct serviceable components, and whether terminal aliases `B2`, `Y2` and `Y3` map to the assumed DIN block numbers. Preserve physical aliases even if the interpretation changes.
- Identify each downlight and deck light individually, confirm tentative bracketed entries, capture physical locations, models, serials and photographs, and record survey dates before marking anything as verified.

