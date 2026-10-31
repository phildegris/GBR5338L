---
title: DC Logical Circuits
description:
date: 2025-07-10
author: Phil
summary: Details about each electrical circuit, its wiring and protection 
---

See the [Equipment Register](/about/configuration/equipment-register/) for equipment-level records derived from this page. The records are provisional pending an onboard survey.

> **2026 owner clarification:** The historic `7 Core` wiring entries below describe **panel-end cores of an Oceanflex 7 × 1.5 mm² distribution trunk** that travels forward to a **second clamp connector set in the forecabin starboard locker**, **not a continuous cable running directly up the mast**. The original text is deliberately retained as historical evidence. See the [owner's transcribed handwritten connector schedule](/about/configuration/dc-terminal-schedule/) for all seven cores, including the newly identified R2/deck and B3/bow assignments. Downstream runs to bow/forecabin, saloon and the mast via the swan neck have not been traced.

| Control Zone | Abbreviation | Location | Description |
| -------- | -------- | -------- | -------- |
| DC Panel | DCP | Chart Table | The main DC Panel at the chart table |
| Navigation Lights | NAV LTS | DCP | The classic section with illuminated graphic of the boat and its lights |

| Busbar Code | Description | Location | Source / Destination | Notes |
| -------- | -------- | -------- | -------- | -------- |
| DC-BB-M | Main -12V Busbar | Aft engine bay frame | Engine Block | Connected to foot mounting bracket at the same bolt as connected to battery negative using doubled up cables - check required capacity |
| DC-BB-A | -12V Busbar | DCP | DC-BB-M | Check Legacy Cable condition and capacity |

## Circuits

* Circuit breakers on the main DC Panel are identified by Column and Row number, e.g. Breaker 1,1 is the top left Circuit breaker.
* **Owner clarification (31 October 2026):** Most breaker circuits pass through individual generic cage-clamp connectors on a DIN rail behind the DC panel. The owner organised the **separate connectors** in vertically repeating sets of **Yellow, Red, Blue** levers (Y / R / B) and numbered each *group* from the **top down**. Thus **B1** is the blue connector in group 1, **Y2** the yellow connector in group 2, and **R4** the red connector in group 4. The group number does **not** mean a single three-way connector block, and lever colour does **not** identify the insulation colour of the connected wire. A recently supplied photograph is **incomplete** and cannot establish total group count or all wire assignments. Legacy downstream wiring entries remain subject to physical tracing.

| Circuit Name | Path | Notes |
| -------- | -------- | -------- |
| Masthead Lt | Breaker 1,1  -> ?? -> DPDT 1 pin 5 | Masthead light is combined Anchor and tricolor light. Mode selected by the polarity of the power supply - polarity is switched by a Double pole Double throw (DPDT) switch On-Off-On |
|| DPDT 4 -> DPDT 3 ||
|| DPDT 1 -> DPDT 6 ||
|| DPDT 2 -> DC-BB-A | via 4 way connector block |
|| DPDT 3 -> B2 -> 7 Core - Blue -> Masthead light A ||
|| DPDT 6 -> Y3 -> 7 Core - Black -> Masthead light B ||
| Steaming Light | Breaker 1, 2 - > Y2 -> 7 Core - Yellow -> Steaming Light ||



- Communications
  - Tranciever
  - AIS
  - Splitter

- Charging
  - Handheld VHF
  - Instrument Panel
  - Companionway
  - Pedestal Mag Mount
  - Nav Station Cave x 4
  - Nav Station Hutch x 2
  - Fore Cabin
  - Aft Cabin

- Topside Lights
  - Bow
  - Stern
  - Steaming
  - Mathead Tricolour
  - Anchor Light
  - Deck Lights
  - Compass Light
  - [Cockpit Light]
  - [Boom Light]

- Fresh Water System
  - Supply Pump
  - Shower Drain Pump
  - Tank Level Sensor
  - Tank Level Indicator Panel

- Bilge Pumps
    - [Pump A]
    - [Pump B]

- Engine Compartment
  - Extractor Fan
  - Forward Striplight
  - Aft Striplight
  - [Sensor Node]

- Local Area Network
  - RUTX50
  - Switch
  - Odroid N2
  - Monitor

- Wide Area Network
  - TRB500 - via 30w PoE Injector
  - **OR**
  - Starlink - via 150w POE Injector

- Entertinment
  - TV
  - [Radio/Media Player]

- Instruments
  - NMEA2000 A
  - NMEA2000 B

- Compartment Lighting
  - Fore Cabin
    - Downlights
  - Saloon
    - Downlights
    - Saloon Stbd Bunk Reading Light/USB
    - Saloon Port Bunk Reading Light/USB
  - Aft Cabin
    - Downlights
    - Striplight
    - Port Bunk Reading Light/USB
    - Bunk Reading Light/USB
  - Heads
    - Striplight
  - Nav Station
    - Striplight (Red/White)
  - Galley
    - Striplight
  - 
  