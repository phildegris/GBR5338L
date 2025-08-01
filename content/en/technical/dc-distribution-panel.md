---
title: "DC Distribution Panel Upgrade"
description: "Technical details of the re-design of our DC Distribution panel."
---

## Situation
**Summer 2025** With a longer than usual period on the hard planned for next winter planning is underway to complete the modernisation of Ragtimes electrical systems.  This will finally see removal of the rats nest of old, poorly terminated and slowly corroding wiring behind the classic 1980's DC panel.

{{< figure
  src="[/images/dc-distribution-panel/rats-nest.jpg]"
  alt="A photograph of the mess of wires behind the DC panel"
  caption="Rats Nest"
  width="50%"
>}}

We are starting with the DC Supply from the house batteries which is currently two very large guage battery cables allowing switching between battery one and battery two, and a significantly smaller guage -ve return run.

Modern battery monitoring solutions make the need to switch between batteries redundant, along with the extra heavy cable, and lower power demands from modern lighting and instruments mean that the old supply is over specified.

When planning DC power distribution there is a tendancy to focus on the supply runs to devices but must also have a safe path back to the battery negative terminal.    

The first step is to determine the maximum current draw, the following table details all the devices supplied from the DC panel. Note: The Windlass and electric bilge pumps are supplied by separate feeds from the house batteries.

Each device is supplied via a separate circuit with wire guage chosen to support the current demand and keep voltage drop < 3%.  Each circuit must be protected with a breaker or fuse above the maximum surge demand for the devices connected, but below the amperage rating for the wire supplying it.  

## DC Device Circuits

### Navigation
| Circuit | Devices | Max Draw | Circuit length | Wire Guage | Circuit Protection 
|------ | ------ | -------- | ------ | ------ | ------  
| Bow Light | Osculati Sphera II Bicolour LED | 166mA | 8m 
| Stern Light | Osculati Sphera II LED Stern Light | 166mA | 4m
| Masthead Tricolour / Anchor | NASA Marine Supernova Combi LED | 200mA | 20m
| Steaming Light | Osculati Navigation and deck LED-light | 370mA | 15m
| Instruments | NMEA 2000 network LEN-30 | 1500mA | 0.2m |
| Navigation Computer | Odroid N2 | 1400mA | 0.5m
| Computer Monitor | Beetronics 15TS7M | 1300mA | 0.5m |
| Helm Device Charger | HKY C140C PD3.1| 10000ma  | 5m | 
| Coachroof Charger | HKY C140C PD3.1 | 10000ma | 4m | 

### Pilot
| Circuit | Devices | Max Draw | Circuit length | Wire Guage | Circuit Protection 
| ------ | -------- | ------ | ------ | ------ | ------ 
| Drive | Jeffa DD-1 **or** Raymarine Wheel Piliot | TBC | |

### Communications
| Circuit | Devices | Max Draw | Circuit length | Wire Guage | Circuit Protection 
|------ | ------ | -------- | ------ | ------ | ------ 
| VHF Tranciever | iCom M510 | 5000mA | 1m |
| AIS Transponder | Ocean Signal ATB1 | TBC | 1m |
| Antenna Splitter | Digital Yacht SPL2000 | TBC | 1m |
| Handheld VHF Charger | iCom M94DE | 300mA | 1m |

### IT Networks
| Group | Circuit | Devices | Max Draw | Circuit length | Wire Guage | Circuit Protection 
|------ | ------ | -------- | ------ | ------ | ------ | ------ 
| Router | Teltonika RUTX50 | TBC | 
| PoE Switch | Linovision 5 Port Gigabit PoE Switch | TBC | 0.3m
| WAN Gateway | Teltonika TRB500 **Or** Starlink Mini | TBC | 4m

### Cabin Lighting
| Circuit | Devices | Max Draw | Circuit length | Wire Guage | Circuit Protection 
|------ | ------ | -------- | ------ | ------ | ------ 
| Forecabin Lights | 4 x Acegoo DC 12v LED Recessed Ceiling Lights | 1000mA | 5m 
| Saloon Lights A | 3 x Acegoo DC 12v LED Recessed Ceiling Lights | 750mA | 5m |
| Saloon Lights B | 5 x Acegoo DC 12v LED Recessed Ceiling Lights | 1250mA | 5m |
| Saloon Lights C | 4 x Acegoo DC 12v LED Recessed Ceiling Lights | 1000mA | 5m |
| Saloon Stbd Bunk Reading Light | 12v LED Reading light & USB Charger | 1000mA | 5m |
| Saloon Port Bunk Reading Light | 12v LED Reading light & USB Charger | 1000mA | 5m |
| Aft Cabin Lights | 4 x Acegoo DC 12v LED Recessed Ceiling Lights | 1000mA | 5m |
| Galley Work Light | 12V LED Interior Strip Light 770mm | 1400mA | 5m |
| Chart Table Work Light - White/Red | 12V LED Interior Strip Light 410mm | 1000mA | 5m |
| Heads Light | 12V LED Interior Strip Light 410mm | 1000mA | 5m |

### Cabin Device Charging
| Circuit | Devices | Max Draw | Circuit length | Wire Guage | Circuit Protection 
| ------ | -------- | ------ | ------ | ------ | ------ 
| Foreward Cabin Chargers | 2 x Dash Mount Dual Charger | 7000mA | 4m |
| Chart table Chargers | 2 x Dash Mount Dual Charger | 7000mA | 4m |
| Nav Station Chargers | 2 x Dash Mount Dual Charger | 7000mA | 4m |
| Saloon Table Chargers | 2 x Dash Mount Dual Charger | 7000mA | 4m |
| Aft Cabin Chargers | 2 x Dash Mount Dual Charger | 7000mA | 4m |

### Domestic Services
| Circuit | Devices | Max Draw | Circuit length | Wire Guage | Circuit Protection 
| ------ | -------- | ------ | ------ | ------ | ------ 
| Fresh Water Pump | Jabsco Par Max 3 |  | 2m
| Shower Discharge Pump | Jabsco Par Max 3 |  | 2m
| Fridge | Isotherm Cruise 35 | 2700mA | 2m
| TV | LG 24TN510S | 2300mA | 4m

## Circuit termination

An array of DIN rail mounted fused terminal connectors linked to the positive supply via jumper bars will supply each circuit via a spdt switch enabling selection of on, off, or auto. 

### Selected Components
- Terminal connectors [Wago 2006-1681 22](https://uk.rs-online.com/web/p/din-rail-terminal-blocks/2815884)
- End and intermediate plates [Wago 2006 Series end plates](https://uk.rs-online.com/web/p/products/5076816/)
- Jumper Bars [Wago 2006 Series Double Jumper Bar ](https://uk.rs-online.com/web/p/products/7581770/)
- Jumper Bars [Wago 2006 Series Triple Jumper Bar ](https://uk.rs-online.com/web/p/products/2475845/)
- Jumper Bars [Wago 2006 Series Quadrouple Jumper Bar ](https://uk.rs-online.com/web/p/products/7581773/)