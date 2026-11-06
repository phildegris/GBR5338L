---
title: NMEA 2000 Configuration
description: "NMEA 2000 network segments, power injection and configuration notes"
date: 2025-07-10
author: Phil
summary: N2K network design and configuration notes
---

[← Configuration](/about/configuration/) · [Equipment Register](/about/configuration/equipment-register/) · [Circuit Register](/about/configuration/circuit-register/)

## Network segments and power

**Owner-confirmed, 6 November 2026:** Ragtime has **one NMEA 2000 network with two segments, A and B**. **Both segments have power injection behind the DC panel (DCP).** This describes the owner-reported arrangement, not an independently traced electrical installation.

| Segment | Power injection location | Historical panel reference | Still to establish |
| --- | --- | --- | --- |
| A | Behind DCP — owner-confirmed | `R1`, handwritten “NMEA 2K A” under NAV INSTR | Actual source circuit, protection, feed wiring, power-injection hardware and connected devices |
| B | Behind DCP — owner-confirmed | `Y1`, handwritten “NMEA 2K B” under NAV INSTR | Actual source circuit, protection, feed wiring, power-injection hardware and connected devices |

The panel aliases come from the [historical connector schedule](/about/configuration/dc-terminal-schedule/); the latest confirmation establishes the **two segment names and injection locations**, not continuity through those particular connectors. `R1` and `Y1` identify clamp lever colours and group positions, not conductor insulation colours.

### Network and equipment inventory to complete

- Record the physical backbone and drop routes, junctions and terminator positions.
- Establish how A and B are interconnected for data and whether their power conductors are isolated. Two injection points alone do not establish separate power domains or two separate CAN networks.
- Identify the supply circuit, fuse/breaker, switching and return path for each injection point; allocate circuit and physical component IDs once identified.
- Link each connected device to its equipment record, segment and drop connection. Record **bus power**, **separate operating supply**, and any bus-interface power requirement independently; network attachment alone does not establish how a device is powered.
- Record manufacturer power/load figures separately from onboard measurements and calculate segment loads once device allocation and power boundaries are known.

A and B are **network segment labels**, not physical equipment IDs. Device allocation, cable lengths, protection ratings and power-isolation hardware have not yet been supplied for this network record.

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