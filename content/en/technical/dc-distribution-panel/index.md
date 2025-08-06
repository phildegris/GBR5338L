---
title: "DC Distribution Panel Upgrade"
description: "Technical details of the re-design of our DC Distribution panel."
date: 2025-08-05
summary: With a longer than usual period on the hard planned for next winter, planning is underway to complete the modernisation of Ragtimes electrical systems.  This will finally see removal of the rats nest of old, poorly terminated and slowly corroding wiring behind the classic 1980's DC panel.
---

## Situation
**Summer 2025** With a longer than usual period on the hard planned for next winter, planning is underway to complete the modernisation of Ragtimes electrical systems.  This will finally see removal of the rats nest of old, poorly terminated and slowly corroding wiring behind the classic 1980's DC panel.

{{< figure
  src="rats-nest.jpg"
  alt="A photograph of the mess of wires behind the DC panel"
  caption="Rats Nest"
  width="50%"
>}}

We are starting with the DC Supply from the house batteries which is currently two very large gauge battery cables allowing switching between battery one and battery two, and a significantly smaller gauge -ve return run.

Modern battery monitoring solutions make the need to switch between batteries redundant, along with the extra heavy cable, and lower power demands from modern lighting and instruments mean that the old supply is over specified.

When planning DC power distribution there is a tendency to focus on the supply runs to devices but they must also we wired back to the battery negative terminal via cable with sufficient capacity.    

Each device is supplied via a separate circuit with wire gauge chosen to support the current demand and keep voltage drop < 3%.  Each circuit must be protected with a breaker or fuse above the maximum surge demand for the devices connected, but below the amperage rating for the wire supplying it.

We are following ABYC standards as closely as possible, therefore all unprotected wiring longer that 170mm will be protected by a slow blow fuse rated below the ampacity of the cable and at least 125% of the circuit demand. 

## Battery Bank
The battery bank currently comprises 2 85AH Spiral Wound Gel AGM batteries wired in parallell. These were installed in 2021 and we do plan to replace these with a larger capacity LifePo4 bank, which is the subject of a [separate project.](./lithium-upgrade.md).


## Sub-Circuits
In order to reduce the need for very heavy and expensive wiring we have chosen to break the DC supply circuits down into a number of sub-circuits, each supplied from the house battery bank by smaller gauge wire, together with appropriate circuit protection. All circuits except for the Bilge Pumps are switched via a remote switch. Downstream switching allows manual disconnection of individual circuits.

| Circuit | Max Draw | Supply Length | Wire gauge | Ampacity | Circuit Protection | Switching | Purpose
| ------ | ------ | ------ | ------ | ------ | ------ |------ |------
| Primary Systems | 52A | 4M | 16mm | 110A | 80A ANL | Remote | Systems required to operate the vessel at sea
| Auxilliary Systems | 66A | 4M | 16mm | 110A | 80A ANL| Remote | Systems required for domestic services and enhanced operations 
| Windlass | 80A-100A | 10M | 25mm | 170A | 100A ANL | Remote | Dedicated circuit to power the Lewmar HX1 windlass
| Watchkeeper | 20A | 3M | 6mm | 50A |40A ANL | None | Systems which are connected at all times, Bilge Pumps, Alarms, remote monitoring and remote access bootstrap node.

A remotely operated battery switch rated at 500A is used to connect all sub circuits except the backbone sub circuit.

The following sections detail the circuits supported by each for these sub-circuits.

## Primary Systems

The 16mm Primary systems supply feed from the House Battery Distribution board terminates in the Chart Table DC panel where it supplys the following individually switched and protected circuits. 

### Navigation
| Circuit | Devices | Max Draw | Circuit Length | Wire Gauge | Circuit Protection 
|------ | ------ | -------- | ------ | ------ | ------  
| Bow Light | Osculati Sphera II Bicolour LED | 0.17A | 8m 
| Stern Light | Osculati Sphera II LED Stern Light | 0.17A | 4m
| Masthead Tricolour / Anchor | NASA Marine Supernova Combi LED | 0.2mA | 20m
| Steaming Light | Osculati Navigation and deck LED-light | 0.37A | 15m
| Instruments | NMEA 2000 network LEN-30 | 1.5A | 0.2m |
| Navigation Computer | Odroid N2 | 1.4A | 0.5m
| Computer Monitor | Beetronics 15TS7M | 1.3A | 0.5m |
| Helm Device Charger | HKY C140C PD3.1| 10A  | 5m | 
| Coachroof Charger | HKY C140C PD3.1 | 10A | 4m | 

### Pilot
| Circuit | Devices | Max Draw | Circuit Length | Wire Gauge | Circuit Protection 
| ------ | -------- | ------ | ------ | ------ | ------ 
| Drive | Jeffa DD-1 **or** Raymarine Wheel Pilot | 15A | |

### Communications
| Circuit | Devices | Max Draw | Circuit Length | Wire Gauge | Circuit Protection 
|------ | ------ | -------- | ------ | ------ | ------ 
| VHF Tranciever | iCom M510 | 5A | 1m |
| AIS Transponder | Ocean Signal ATB1 | 2A | 1m |
| Antenna Splitter | Digital Yacht SPL2000 | 0.25A | 1m |
| Handheld VHF Charger | iCom M94DE | 0.3A | 1m |

### IT Networks
| Group | Circuit | Devices | Max Draw | Circuit Length | Wire Gauge | Circuit Protection 
|------ | ------ | -------- | ------ | ------ | ------ | ------ 
| Router | Teltonika RUTX50 | 0.8mA | 
| PoE Switch | Linovision 5 Port Gigabit PoE Switch | 1.2A | 0.3m
| WAN Gateway | Teltonika TRB500 **Or** Starlink Mini | 2.5A | 4m


## Auxilliary Systems

The 16mm Auxilliuary systems supply feed from the House Battery Distribution board terminates in the Chart Table DC panel where it supplys the following individually switched and protected circuits.

### Cabin Lighting
| Circuit | Devices | Max Draw | Circuit Length | Wire Gauge | Circuit Protection 
|------ | ------ | -------- | ------ | ------ | ------ 
| Forecabin Lights | 4 x Acegoo DC 12v LED Recessed Ceiling Lights | 1A | 5m 
| Saloon Lights A | 3 x Acegoo DC 12v LED Recessed Ceiling Lights | 0.75A | 5m |
| Saloon Lights B | 5 x Acegoo DC 12v LED Recessed Ceiling Lights | 1.25A | 5m |
| Saloon Lights C | 4 x Acegoo DC 12v LED Recessed Ceiling Lights | 1A | 5m |
| Saloon Stbd Bunk Reading Light | 12v LED Reading light & USB Charger | 1A | 5m |
| Saloon Port Bunk Reading Light | 12v LED Reading light & USB Charger | 1A | 5m |
| Aft Cabin Lights | 4 x Acegoo DC 12v LED Recessed Ceiling Lights | 1A | 5m |
| Aft Cabin Stbd Bunk Reading Light | 12v LED Reading light & USB Charger | 1A | 5m |
| Aft Cabin Port Bunk Reading Light | 12v LED Reading light & USB Charger | 1A | 5m |
| Galley Work Light | 12V LED Interior Strip Light 770mm | 1.4A | 5m |
| Chart Table Work Light - White/Red | 12V LED Interior Strip Light 410mm | 1A | 5m |
| Heads Light | 12V LED Interior Strip Light 410mm | 1A | 5m |

### Cabin Device Charging
| Circuit | Devices | Max Draw | Circuit Length | Wire Gauge | Circuit Protection 
| ------ | -------- | ------ | ------ | ------ | ------ 
| Forward Cabin Chargers | 2 x Dash Mount Dual Charger | 7A | 4m |
| Chart table Chargers | 2 x Dash Mount Dual Charger | 7A | 4m |
| Nav Station Chargers | 2 x Dash Mount Dual Charger | 7A | 4m |
| Saloon Table Chargers | 2 x Dash Mount Dual Charger | 7A | 4m |
| Aft Cabin Chargers | 2 x Dash Mount Dual Charger | 7A | 4m |

### Domestic Services
| Circuit | Devices | Max Draw | Circuit length | Wire Gauge | Circuit Protection 
| ------ | -------- | ------ | ------ | ------ | ------ 
| Fresh Water Pump | Jabsco Par Max 3 | 7.5A | 2m
| Shower Discharge Pump | Jabsco Par Max 3 | 7.5A | 2m
| Fridge | Isotherm Cruise 35 | 2.7A | 2m
| TV | LG 24TN510S | 2.3A | 4m

## Circuit termination

An array of DIN rail mounted fused terminal connectors linked to the positive supply via jumper bars will supply each circuit via a spdt switch enabling selection of on, off, or auto. 

### Selected Components
- Terminal connectors [Wago 2006-1681 22](https://uk.rs-online.com/web/p/din-rail-terminal-blocks/2815884)
- End and intermediate plates [Wago 2006 Series end plates](https://uk.rs-online.com/web/p/products/5076816/)
- Jumper Bars [Wago 2006 Series Double Jumper Bar ](https://uk.rs-online.com/web/p/products/7581770/)
- Jumper Bars [Wago 2006 Series Triple Jumper Bar ](https://uk.rs-online.com/web/p/products/2475845/)
- Jumper Bars [Wago 2006 Series Quadruple Jumper Bar ](https://uk.rs-online.com/web/p/products/7581773/)