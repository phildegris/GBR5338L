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

| Group | Circuit | Devices | Max Draw | Circuit length | Wire Guage | Circuit Protection 
|------ | ------ | -------- | ------ | ------ | ------ | ------ 
| Navigation | Bow Light | Osculati Sphera II Bicolour LED | 166mA | 8m 
| Navigation | Stern Light | Osculati Sphera II LED Stern Light | 166mA | 4m
| Navigation | Masthead Tricolour / Anchor | NASA Marine Supernova Combi LED | 200mA | 20m
| Navigation | Steaming Light | Osculati Navigation and deck LED-light | 370mA | 15m
| Navigation | Instruments | NMEA 2000 network LEN-30 | 1500mA | 0.2m
| IP Networks | Router | Teltonika RUTX50 | TBC | 
| IP Networks | PoE Switch | Linovision 5 Port Gigabit PoE Switch | TBC | 0.3m
| IP Networks | LTE WAN Gateway | Teltonika TRB500 | TBC | 4m
| IP Networks | SAT WAN Gateway | Starlink Mini | TBC | 4m
| Cabin Lighting | Forecabin Lights | 4 x Acegoo DC 12v LED Recessed Ceiling Lights | 1000mA | 5m |
| Cabin Lighting | Saloon Lights A | 3 x Acegoo DC 12v LED Recessed Ceiling Lights | 750mA | 5m |
| Cabin Lighting | Saloon Lights B | 5 x Acegoo DC 12v LED Recessed Ceiling Lights | 1250mA | 5m |
| Cabin Lighting | Saloon Lights C | 4 x Acegoo DC 12v LED Recessed Ceiling Lights | 1000mA | 5m |
| Cabin Lighting | Saloon Stbd Bunk Reading Light |  | 1000mA | 5m |
| Cabin Lighting | Saloon Port Bunk Reading Light |  | 1000mA | 5m |
| Cabin Lighting | Aft Cabin Lights | 4 x Acegoo DC 12v LED Recessed Ceiling Lights | 1000mA | 5m |
| Cabin Lighting | Galley Work Light | | 1000mA | 5m |
| Cabin Lighting | Chart Table Work Light - White/Red | | 1000mA | 5m |
| Cabin Lighting | Heads Light | | 1000mA | 5m |






## Circuit termination

An array of DIN rail mounted fused terminal connectors linked to the positive supply via jumper bars will supply each circuit via a spdt switch enabling selection of on, off, or auto. 

### Selected Components
- Terminal connectors [Wago 2006-1681 22](https://uk.rs-online.com/web/p/din-rail-terminal-blocks/2815884)
- End and intermediate plates [Wago 2006 Series end plates](https://uk.rs-online.com/web/p/products/5076816/)
- Jumper Bars [Wago 2006 Series Double Jumper Bar ](https://uk.rs-online.com/web/p/products/7581770/)
- Jumper Bars [Wago 2006 Series Triple Jumper Bar ](https://uk.rs-online.com/web/p/products/2475845/)
- Jumper Bars [Wago 2006 Series Quadrouple Jumper Bar ](https://uk.rs-online.com/web/p/products/7581773/)