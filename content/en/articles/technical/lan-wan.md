---
title: "LAN and WAN"
description: ""
date: 2025-07-10
author: Phil
summary: Internet connection via the WiFi network depends on a single device carrying a single newwork sim.  This single point of failure is now obsolete with better 5g networks and Starlink now widely available at reasonalable prices, it is time to upgrade to always on broadband internet capability.
---

![Ragtime Off Falmouth](/img/off-falmouth.jpg)

## Situation
**2025, Early summer in the UK - Glorious**. We are enjoying spending time aboard Ragtime in and around our temporary base at Haslar Marina, Gosport. With our summer cruise with the grandchildren looming and spending much more liesure time, and potentially working more while away on the boat means that we need a more dependable solution for internet access.  Marina wifi does not work well and 4g signal is workable but not relaible for streaming video.

Internet connection via the WiFi network depends on a single device carrying a single newwork sim.  This single point of failure is now obsolete with better 5g networks and Starlink now widely available at reasonalable prices, it is time to upgrade to always on broadband internet capability.

## Solution
1. Replace the Digital Yacht 4G Connect with Teltonika RUTX50
2. Add a Teltonika TRB500 for 4/5g Cellular WAN
2. Add a Starlink Mini Dish for Sattellite WAN

We have upgraded our TCP network components and configuration to provide better WAN connectivity and bandwidth to support working aboard and to enhance the streaming entertainment services we use aboard

The new sustem is built around an industral grade RUTX50 router form teltonika which has been configured to provide:

1. DHCP Server
2. 2.4 and 5.8 Ghz Wifi
3. WAN connection failover rules

We want to be able to switch off LAN, Cellular WAN, and Sattellite WAN independently. While the RUTX50 can support Cellular connections we have chosen to add a separate Teltonika TRB500 5g router.

The Cellular connection via the TRB500 provides an alternative to the new primary WAN service provider, a new Starlink Mini device.

WAN connection failover rules in the RUTX50 use the Starlink WAN as primary, TRB500 as secondary, and the internal cellular capability as a third failover WAN interface.

## Starlink
The Starlink Mini is connected to an Unlimited Roam Account. This provides uninterupted connection within the 12mile limit in all supported countries, this includes the UK, all countries in the EU, and many more. The account has the option to enable "Ocean mode" via the account control panel, which, for a metered cost, provides connectivity anywhere on the high seas.
Note: Starlink, while very good, can suffer from performance issues in heavy rain, and should not be relied on for emergency sattellite communication alone.

## Cellular
The TRB500 carries a Lebara SIM (Vodafone Network) in its single SIM slot.

The RUTX50 carries a GiffGaff (O2 network) SIM in its first SIM slot.

Failover to GiffGaff is disabled as this is an emergency fallback connection.

## Wifi hotspot connections
The RUTX50 does support connection to wifi hotspots. None have been configured, but the facility, even if a bit clukny, is there if needed.

## Power and switching
We have reconfigured a couple of circuit breakers on the DC distribution panel.

## LAN
This circuit now provides power to:

1. PoE Network Switch

The RUTX50 is powered via the PoE connection to the LAN1 port - Note the RUTX50 seems to need a negative connection for this to work, seems odd.

*TODO:* Add separate fuses for the supply to each of these devices.

## WAN
This circuit provides power to a panel mounted DPDT On-Off-On Switch. The On circuits from the new switch provide power to the TRB500 and Starlink Mini. This allows switching between WAN connection devices, or disabling both.