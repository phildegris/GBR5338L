---
title: NMEA 2000 Configuration
description: 
date: 2025-07-10
author: Phil
summary: N2K network design and configuration notes
---

## Ocean Signal ATB-1

The ATB-1 AIS transponder produces NMEA2000 PGNs and is also capable of hosting an NMEA 0183 web server that can be used as a data source for connected applications such as the Garmin Boating App, AKA Navionics.

The boating apps connection to the TCP server hosted by the ATB-1 proved far too unreliable, with continnual disconnections, A UDP server would provide a much more stable service, but is not provided by the ATB-1 (or if it is, it is not documented well at all)

Our solution is to use the YDWG-02 NMEA 2000 Wireless gateway which allows us to configure a UDP server on a commonly recoginsed port **10110**.

This server has provided reliable AIS target integration with the boating APP.

The ATB-1 

## Yacht Devices

Configuration settings to YD devices can be made using CANView and udating "Installation Description 2" in the Device properties.

Commands are in the format YD: [Command] [Param 1] [Param 2]

The following configuration setting have been applied:

## YDAP-04

| Setting | Notes 
| ------ | ------ 
| YD:SIMRAD ON | This allows the Autopilot page in the B&G Triton2 MFD to display Autopilot information