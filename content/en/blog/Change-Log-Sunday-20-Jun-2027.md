---
title: "Changelog Sunday 20 Jun 2027"
description: ""
date: 2025-07-20
author: Phil
summary: A full three days of work has been carried out in order to complete a number of upgrades, primary focus has been the ongoing LAN and Wan upgrade, and the Autopilot upgrade, see separate entries for design choices and rationale.
---

A full three days of work has been carried out in order to complete a number of upgrades, primary focus has been the ongoing [LAN and WAN upgrade](./technical/LAN-WAN), and the Autopilot upgrade, see separate entries for design choices and rationale.

## Work completed

* Cancelled Vodafone Sim contract, replaced with Lebara - Lebara Sim in TRB500, Vodafone Sim in the bin.
* Modified the Starlink poe splitter so it will fit inside the temporary comms pole.
* Installed the starlink Mini dish(y)
* Replaced the old cable glands on the cockpit starboard quarter coaming with 2 x Black Scanstrut, re routed the stern light cable through the lower of the pair, and the Starlink mini thwough the upper one. Routed cables through the Jonbouy rail mounting clamps.
* Having spent two hours trying to connect RJ45 connectors, I used a pre-assembled Orange LAN Cable from PoE Switch in Chart table Hutch through the starboard access below the side deck to the RUTX50 installed in the deckhead space above the aft cabin outboard berth. 
* Surprised to find the RUTX50 is powered by the PoE from the Main PoE switch, but does need its own connection to -Ve.
* Repurposed the new White supply previously installed  for the RUTX50 to replace the legacy wiring to the stern light, removed the legacy supply and return wires.
* Connected stern light -ve to the new aft -Ve Busbar
* Labelled the re-purposed Circuit breakers LAN and WAN, Labelled the Autopilot Circuit Breaker "Pilot", labelled the WAN Access Interface Switch, SAT - LTE.
* Connected the RUTX50 Wifi Antenna 1 to the existing Wifi antenna under the companionway hatch garage.  Routed by the shortest possible route below the deck head in the heads, and through the aft bulkhead.
* Removed all legacy and redundant wiring leading aft from the DC Distribution panel area, this included heavy 7 core used for NMEA0183, and wiring for the redundant Webasto heater.
* Removed fuel guage and all associated wiring.
* Removed all the wiring to the legacy battery monitor.
* Removed the legacy Shunt
* Doubled the connection from the main -ve busbar to the engine block - need to check and replace this with an appropriately sized single cable.
* Installed the new Victron battery monitor in the hole left by the fuel guage
* Ran the data cable from the BM aft through the starboard floor conduit from the locker under the chart table to the battery compartment.  
* Replaced the Autopilot selector switch with high quality APEM component.
* Replaced the WAN selector switch with a high quality APEM component
* Connected the Oraca Core to the network with a pre-assembled Blue network cable.
* Connected the TV to the network with a pre-assembled Flat White network cable. This cable is routed through the saloon deckhead and through a new hole bored in the forward bulkhead and run down the bulkhead behind the mirror. The TV mount is very close to the bulkhead so the hole bacj through it needed to be carefully aligned with the position of the TV LAN port, when plugged in the connector mostly is housed in the hole.
* Installed extra folding hook in the shower area,  
* Installed folding hook inside the door of the aft cabin, above the fire extinguisher.
* Diagnosed the engine start button issue.  This resulted in building a new harness to connect the engine electrical system to the "umbilical" cable which runs aft and connects to the engine control panel.  The new harness was terminated with an 8 pin Deutch connector. The Umbilacal cable has a large number of unused cables, those in use were connected to the other part of the Deutch connector.  TODO: Replace the umbillical with a lighter seven core tinned cable.:  
** Result:** the botton on the control panel now works through the umbilical wiring, so I removed the jury rigged power supply line, Bonus: the temp and oil pressure warning lights, and the Tachometer, and alarms, and alarm test now all work correctly.
* Added to the AP button panel wiring daisy chained connections for the button back lights. The circuit is supplied from the YDAP pole of the selector switch, so the light s will only work when the YDAP-04 is in use, the circuit is completed to ground via the latching Light button, so they can be turned off if not needed. TODO: Build the LED brightness and Nav Light controller Node and get the lights mode and backlight mode selector buttons working.
* Note: The YDAP Mode Led output is a fairly low voltage and the mode led backlight is quite dim, and hard to see in daylight.  We should look to resolve this by a PWM driven Mosfet as part of the panel micro controller logic. 
* Fixed the DC panel LEDs which became disconnected from -12v during the wiring purge. Soldered a new line run to the -Ve Bus bar.
* Repurposed and relabelled the "Compass Light" circut breaker as Helm, replaced the legacy purple wire run to provide a feed for the Compass Light and to a newly installed high output USB charger, mounted at the aft end of the aft cabin.
* Removed the RAM ball mount anc clamp from the helm guardrail, and installed the new Peak Design mag mount wireless phone charger.
* Connected the phone mount to the high output charger.
* Fixed the Aft Cabin USB socked supply, connected to Bunk Lights Circuit breaker.
* ToDo: refine and balance lighting and charging circuit loads.
* Bagan documenting [Logical Circuits here.](./technical/logical-circuit)

## Issues arrising:

* Fuel level guage - what to do to make monitoring fuel level easier
* Engine start relay and fuse wiring really needs replacing as it is badly corroded with poor connetions
* Engine oil pressure and temp senders are badly corroded and need replacing
* Raw water flow sensor is not wired into the engine panel as it used to be.
* We really need to build the Engine Sensor Boat Toy Node and replacement engine control panel as a higher priority than other Boat Toy projects:

>   
> ### Boat Toy Engine Sensor Node Features:
>   * Engine Temp
>   * Oil Pressure
>   * Compartment Temp and Humidity
>   * Exhaust Temp
>   * Raw water flow
>   * RPM
>   * Fwd and Aft Hatch open/closed sensor

### DC Panel
We should preserve the original DC Panel face plate by replacing sections with screw in sub panels.
Key features to preserve are the builder details and build number tag and the overall look and feel.

> We should prioritize mounting the existing panel onto a new hinged back panel.  This will make accessing the wiring easier and kinder to the wiring. 

### DC Power supply

> Add a battery isolator switch near the battery bank in the aft cabin. Possibly use a remote switch which can ultimately be operated from the new DC panel or via automation projects.

> Add a battery fuse

> Add spare fuses

> 
