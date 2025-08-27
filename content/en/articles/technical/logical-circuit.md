---
title: DC Logical Circuits
description:
---

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
* Most circuits from circuit breakers first pass through a din rail mount cage clamp connector block. Each block has three connections with Red, Yellow and Blue levers.  The blocks are mounted vertically behind the DC panel and are refered to by color, R,Y, or B, and block number, from the top down e.g. B4, blue lever on the fourth block down. 

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
  