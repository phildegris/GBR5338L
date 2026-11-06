---
title: NMEA 2000 Configuration
description: "NMEA 2000 network segments, power injection and configuration notes"
date: 2025-07-10
author: Phil
summary: N2K network design and configuration notes
---

[← Configuration](/about/configuration/) · [Equipment Register](/about/configuration/equipment-register/) · [Circuit Register](/about/configuration/circuit-register/)

## Network segments and power

**Owner-confirmed, 6 November 2026:** Ragtime has **one NMEA 2000 network with two segments, A and B**. **Both segments have power injection behind the DC panel (DCP).** The segments are joined by a **[power isolator (EQ-063)](/about/configuration/equipment/eq-063/)** that **passes CAN data while separating their positive supplies** (owner-confirmed). This describes the owner-reported arrangement, not an independently traced electrical installation.

| Segment | Power injection location | Historical panel reference | Still to establish |
| --- | --- | --- | --- |
| A | Behind DCP — owner-confirmed | `R1`, handwritten “NMEA 2K A” under NAV INSTR | Actual source circuit, protection, feed wiring and power-injection hardware (complete device list below) |
| B | Behind DCP — owner-confirmed | `Y1`, handwritten “NMEA 2K B” under NAV INSTR | Actual source circuit, protection, feed wiring, power-injection hardware and device power classifications (inventory below) |

The panel aliases come from the [historical connector schedule](/about/configuration/dc-terminal-schedule/); the latest confirmation establishes the **two segment names and injection locations**, not continuity through those particular connectors. `R1` and `Y1` identify clamp lever colours and group positions, not conductor insulation colours.

### Network and equipment inventory to complete

- Record the physical backbone and drop routes, junctions and terminator positions.
- Identify the power isolator’s manufacturer/model and physical location, and document its pin-level connections. CAN data continuity and positive-supply separation are owner-confirmed; negative/shield continuity and galvanic isolation have not been established.
- Identify the supply circuit, fuse/breaker, switching and return path for each injection point; allocate circuit and physical component IDs once identified.
- Link each connected device to its equipment record, segment and drop connection. Record **bus power**, **separate operating supply**, and any bus-interface power requirement independently; network attachment alone does not establish how a device is powered.
- Record manufacturer power/load figures separately from onboard measurements and calculate segment loads once device allocation and power boundaries are known.

A and B are **network segment labels**, not physical equipment IDs. The physical power isolator is recorded separately as EQ-063. Segment A and B device allocations are recorded below; power classifications for B, physical connections, cable lengths, protection ratings and the isolator’s model/location still require documentation.

## Segment A — connected equipment and power

**Owner-confirmed, 6 November 2026:** Segment A provides **data-only connections** for the Icom M510 VHF and ATB-1 AIS, and **data plus bus power** for the previously documented Yacht Devices YDWG-02 wireless gateway. The owner subsequently confirmed this is the complete segment A device list.

| Equipment | NMEA 2000 segment | Connection role | Operating power source |
| --- | --- | --- | --- |
| [EQ-003 — Icom M510 VHF](/about/configuration/equipment/eq-003/) | A | Data only (owner-confirmed) | Separate DC supply: [DC-COM-02](/about/configuration/circuits/dc-com-02/), FU-001, EQ-057 way 1 |
| [EQ-004 — ATB-1 AIS](/about/configuration/equipment/eq-004/) | A | Data only (owner-confirmed) | Separate DC supply: [DC-COM-04](/about/configuration/circuits/dc-com-04/), FU-003, EQ-057 way 3 |
| [EQ-064 — Yacht Devices YDWG-02 wireless gateway](/about/configuration/equipment/eq-064/) | A | Data and power (owner-confirmed) | NMEA 2000 segment A bus supply, injected behind DCP |

The data-only classifications above record the owner's installation description; interface/adapter details and pin-level power connections have not been traced. Gateway load/LEN, drop-cable routes, junction positions and the segment A injection circuit/protection remain to be documented. Separate COM power circuits remain distinct from the NMEA 2000 data connection.

## Segment B — connected equipment

**Owner-confirmed, 6 November 2026:** The following ten items are allocated to segment B. Unlike segment A, their individual bus-power versus separate-supply arrangements have **not yet been confirmed** in this inventory. Network attachment does not imply that all operating power comes from the bus.

| Equipment / owner label | Segment | Bus power / separate supply |
| --- | --- | --- |
| [EQ-065 — Garmin GPS 24xd](/about/configuration/equipment/eq-065/) | B | To confirm |
| [EQ-066 — B&G WS310](/about/configuration/equipment/eq-066/) | B | To confirm |
| [EQ-067 — B&G DST-810](/about/configuration/equipment/eq-067/) | B | To confirm |
| [EQ-068 — Orca Core 2](/about/configuration/equipment/eq-068/) | B | To confirm |
| [EQ-069 — B&G Triton 2 autopilot controller](/about/configuration/equipment/eq-069/) | B | To confirm |
| [EQ-070 — B&G Triton 2 MFD 1](/about/configuration/equipment/eq-070/) | B | To confirm |
| [EQ-071 — B&G Triton 2 MFD 2](/about/configuration/equipment/eq-071/) | B | To confirm |
| [EQ-072 — B&G Triton 2 MFD 3](/about/configuration/equipment/eq-072/) | B | To confirm |
| [EQ-073 — B&G NAC-3](/about/configuration/equipment/eq-073/) | B | To confirm |
| [EQ-074 — Yacht Devices “YD RA?” — model to confirm](/about/configuration/equipment/eq-074/) | B | To confirm |

The three Triton 2 MFDs have separate stable equipment IDs. Their physical positions remain to be assigned to MFD 1, 2 and 3. “YD RA?” is retained as an uncertain owner label; YDRA-01 rudder adaptor is a tentative match to earlier discussion, pending model confirmation. Sensor interface hardware, including the WS310 connection into the network, has not yet been inventoried. Equipment names reproduce the owner’s labels; exact nameplate variants remain to be recorded.

## Historical configuration notes — July 2025

The notes below are retained as historical configuration information. They do not establish the current device inventory, segment allocation or power arrangement; the YDAP-04 notes require reconciliation with the later NAC-3 installation.

### Ocean Signal ATB-1

The ATB-1 AIS transponder produces NMEA2000 PGNs and is also capable of hosting an NMEA 0183 web server that can be used as a data source for connected applications such as the Garmin Boating App, AKA Navionics.

The boating apps connection to the TCP server hosted by the ATB-1 proved far too unreliable, with continnual disconnections, A UDP server would provide a much more stable service, but is not provided by the ATB-1 (or if it is, it is not documented well at all)

Our solution is to use the YDWG-02 NMEA 2000 Wireless gateway which allows us to configure a UDP server on a commonly recoginsed port **10110**.

This server has provided reliable AIS target integration with the boating APP.

The ATB-1 

### Yacht Devices

Configuration settings to YD devices can be made using CANView and udating "Installation Description 2" in the Device properties.

Commands are in the format YD: [Command] [Param 1] [Param 2]

The following configuration setting have been applied:

### YDAP-04

| Setting | Notes 
| ------ | ------ 
| YD:SIMRAD ON | This allows the Autopilot page in the B&G Triton2 MFD to display Autopilot information