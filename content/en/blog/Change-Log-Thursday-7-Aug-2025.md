---
title: "Changelog Thursday 7 Aug 2025"
description: ""
date: 2025-08-08
author: Phil
summary: Final push to clear main backlog tasks ahead of our cruise.
---

The safety of the DC system has always been a concern, on a 35 year old boat with a number of previous owners there are many things that could go wrong, from corroded wiring, poorly planned additions, and the use of substandard wiring and components, there is a lot to worry about.

{{< figure
  src="../Chart-Table-Wiring-Pile.jpg"
  alt="The Chart table piled with a mess of wiring"
  width="50%"
>}}

Since our lase visit we have been busy planning the replacement of the DC supply to the DC distribution panel, procuring and preparing components, and materials.  The design of [the new DC Supply is detailed here.](./technical/dc-distribution-panel)

## Aims

1. Complete the installation and commissioning of the new Battery Monitor.
2. Ensure all circuits distributed from the House Batteries are fused according ABYC standards i.e. below the cable ampacity and above 125% of maximum expected continnious current.
3. Replace the old battery supply cables to the distribution panel.
4. Install a remote battery switch and decommission the old battery master switch (to be relpaced with an alarms display panel later).
5. Replace under spec -VE return cables with appropriate sized cabling.

## Work completed

* Reconfigured the DHCP server static leases for ADB1, YDWG, ORCA, and M510 as 192.168.1.11,12,15 and 15.
* Reconfigured AIS Data as Ragtime
* Created and Labeled 2 SD cards for ATB-1 config, Ragtime, and Ragtime Solo Sail (labelled SS)
* Reposittioned the ATB1 in its bay to make USB port access easier.
* Added an SPST switch at engine control panel and wired in to allow switching the Compas light.
* Added a PoE splitter to power the RUTX50 - the strange behaviour we saw with it working directly via PoE but needing an -12v connection as well, was checked and found to be not a recommended way to power the device due to the risk of ground loops. (note to self... Find out what a Ground Loop Is all about)
* Moved the batteries aft and installed the new -ve link bar connecting both -ve terminals and the Battery side of the new Shunt.
* Installed the Sub-Circuit distribution panel in the forward end of the battery compartment
* Removed the supply to the Engine Start Emergency House Switch.
* Provided a new supply to the Engine Start Emergency House Switch directly from the unfused side of the House Battery Bank
* Removed the two supply cables from the battery bank to the master switch
* Installed 16mm Cable from Distribution panel to the Primary Circuit Fuse
* Installed 16mm Cable from Distribution panel to the Auxilliary Circuit Fuse
* Decommissioned the old battery master switch
* Installed an 8mm terminal post on the rear of the old battery master switch
* Connected the two new Circuit supplies and existing feeds to circuit breakers, and gas alarm to the new temporary terminal post.
* Removed the old -12v connection from the -12v bus in the Distribution panel to the engine -ve bus.
* Installed 2x 16mm cables to upgrade the capacity of the return feeds to the capacity of the supply feeds
* Terminated the new return cables on the -12v Panel bus, and the Load side of the new Shunt
* installed Terminal Posts and MRBF fuses on each battery positive terminal
* Installed two equal length 25mm supply cables one from each terminal fuse connecting the batteries in parallell to the supply side of the Remote Battery Switch
* Reconnected the windlass -ve cable to the Load side of the new shunt
* Installed a new 25mm cable connecting the new 100A Windlass fuse to the existing 70A windlass circuit breaker in the drive shaft compartment.
* Connected the smart shunt to the switched side of the new Remote Batery switch.
* commissioned the new battery monitor.
* Installed a momentary DPDT illuminated rocker switch alongside the battery monitor.
* installed a 4 core signal wire (old nmea 0183 cable) and connected to Remote Battery Switch and the new DPDT switch at the Panel
* Secured cabling in the battery and adjacent compartment.

{{< figure
  src="../Battery-Monitor-And-Remote-Switch.jpg"
  alt="The new battery monitor and remote switch control switch"
  width="50%"
>}}
{{< figure
  src="../Sub-Circuit-Distribution-Panel.jpg"
  alt="The new DC Sub-Circuit distribution Panel"
  width="50%"
>}}


## Issues arrising

* Compass light still not working despite checking polarity - Resolve when re-sealing the housing to the pedestal.
* Some of the battery terminations do not have spring washers. - RESOLVED
* Some battery terminals are unprotected.
* Temporary Terminal Post on the rear of the old master switch.
* Cable support below the chart table and in the DC panel needs addressing.
* Critical cable runs in the space beneath the aft bunk need better protection.
* The 240v supply to the battery charger is domestic flex and should be replaced with marine grade and run in a dedicated conduit for  its entire length
* We are unable to connect Boating app to the YDWG-02 UDP server
* YDWG-02 is not serving AIS Target PGNs
* ATB-1 is awful due to difficulty configuring via the App / Website - Replace??

## TO DO before we leave

* [x] Spring Washers
* [x] Clear Bilge Water
* [x] Replace Cielings
* [x] Setup YDAP-04 via CAN View
* Calibrate AP
