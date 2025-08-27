---
title: "Autopilot Upgrade"
description: "Technical details of the re-design of our Autopilot system."
date: 2025-08-27
summary: The Raymarine ST4000 and its Wheel drive has reached the end of its service life, despite new belts and integration with the new N2K instruments it is not able to handle the boat in following seas reliably and the drive is noisy, weak and vulnerable to the elements.
---
# DRAFT CONTENT 

## Situation
**Winter 2025** Autopilot systems are often treated like a crewmember on long offshore passages — quiet, tireless, and critically important. On *Ragtime*, we’ve come to rely on ours more than ever, especially with an eye toward solo and short-handed ocean racing, including the 2027 AZAB.

But our original setup, a venerable Raymarine ST4000 wheel pilot, had started to show its age. While it had served faithfully, it was never designed for sustained offshore duty in heavier weather — and its location on the wheel made it vulnerable and fiddly. It was time for something stronger, smarter, and more redundant.

That decision kicked off a fascinating journey of planning, research, and experimentation — including long evenings with ChatGPT to help compare components, assess compatibility, and clarify CAN bus voodoo.

Here’s how we approached the upgrade, and what we learned along the way.

---

## The Why: Reliability, Capability, and Confidence Offshore

We set out to solve several key problems:

1. **Strength and Reliability**  
   The ST4000 wheel drive couldn’t hold a steady course in heavy weather. Under sail, it struggled with helm load and drained the battery quickly.

2. **Redundancy and Safety**  
   A failure at sea needed a fallback. We didn’t want a single point of failure to jeopardize a passage or race.

3. **Power Efficiency and Autonomy**  
   With limited power aboard and increasing use of solar and lithium, we needed an autopilot that sipped power, not guzzled it — especially when under sail, steering long legs.

4. **Future-Proofing**  
   We wanted flexibility to upgrade sensors, add feedback from sailing processors, and even experiment with AI-driven control logic down the line.

---

## The What: Key Components in the New System

### 1. Drive Unit: Jefa DD1 Direct Drive

The heart of the new system. The Jefa DD1 is a compact, efficient inboard direct drive unit designed for rudder quadrant control. It’s typically oversized for a boat like the Moody 336 — and that’s exactly why we chose it.

- **Why it matters:** Unlike wheel drives, the DD1 applies torque directly to the quadrant, providing fast, positive helm response even under load.  
- **Design features:** The DD1 uses a highly efficient low-power permanent magnet motor mated to a precision *planetary gearbox*, delivering high torque through a compact form factor. The planetary gear system ensures smooth motion with minimal backlash, ideal for autopilot performance where responsiveness and holding power are critical. The integrated *electromagnetic clutch* disengages cleanly when the pilot is off, preserving feel at the helm and reducing drag.  
- **How we chose it:** ChatGPT helped us compare the Jefa DD1 with discontinued Octopus drives and reviewed compatibility with our Whitlock Cobra steering.

### 2. Primary Controller: Yacht Devices YDAP-04

This compact, NMEA 2000-compatible autopilot controller speaks fluently to modern marine networks and handles complex pilot logic with surprising grace.

- **Why it matters:** It integrates well with our existing B&G Triton system and allows real-time control via NMEA 2000. Bonus: it uses PWM to reduce power draw to the clutch.  
- **How we chose it:** After evaluating Pypilot, Raymarine Evolution, and older analog options, we settled on YDAP-04 for its efficiency, open network integration, and compact footprint.

---

## Installation and Custom Tiller Quadrant Design

Installing the Jefa DD1 wasn’t a plug-and-play operation. At **12 kg**, it’s not something you want to keep hoisting in and out of tight lockers to test clearances. Instead, we used **Onshape**, a cloud-based CAD tool, to virtually model the aft locker space and simulate different mounting options.

### Designing for Cobra Steering

The Moody 336 uses a **Whitlock Cobra trailing link system**, meaning the rudder quadrant geometry doesn’t match typical direct-drive setups. We needed a **custom tiller arm** that fit both the available space and the mechanical constraints of the Cobra linkage.

Using Onshape, we modelled the new tiller arm and its integration with the DD1’s drive flange. Once the design was validated, we had the part **CNC machined in aluminium**, then **bead-blasted and hard anodised** for strength and corrosion resistance. We used **JLCNC**, a cost-effective machining service in China, which delivered excellent results on a tight budget.

### Inverted Mounting Through the Deckhead

Rather than mounting the DD1 horizontally, we **inverted it** and bolted it **through the underside of the cockpit deckhead** — saving space and aligning better with the quadrant geometry.

To protect the **balsa-cored floor** from water ingress and compression damage, we:

- Drilled all mounting holes oversize  
- Epoxy-filled the holes to seal the core  
- Re-drilled to final size before fastening the drive with marine-grade stainless hardware

All cabling was routed cleanly into trunking, and connections were made easily accessible for future service — with the clutch and drive power lines routed to the YDAP-04 controller.

---

## The How: Smart Planning, Smarter Questions, and Help from an AI Assistant

We approached the upgrade like any good offshore passage: we planned redundancies, allowed for flexibility, and asked for help.

Instead of trawling through forums and datasheets late into the night, we turned to ChatGPT to:

- Validate electrical compatibility between components  
- Help size wiring and fuses based on load curves  
- Compare CAN bus options and NMEA 2000 sentence compatibility  
- Translate vague manuals into actionable design choices  
- Model performance vs. power consumption tradeoffs

It wasn’t just about buying parts — it was about designing a system that matched the reality of short-handed offshore sailing.

---

## Lessons Learned

- **Redundancy = Peace of Mind**  
  Our two fully independent systems give us confidence that no single failure will force us to hand-steer 500 miles.

- **Direct Drive = Night-and-Day Difference**  
  The DD1 is a beast. Even in gusty conditions, it corrects without hesitation and feels almost like having a human on the helm.

- **Open Networks = Future-Proof**  
  By staying NMEA 2000-native and avoiding brand lock-in, we’ve kept our options open for future upgrades — including full sailing processor integration.

---

## Closing Thoughts

The world of marine electronics is changing rapidly. With systems like YDAP, PyPilot, and Orca Core, it's now possible for owners to build smarter, more efficient boats that respond to their own needs and budgets.

With *Ragtime*, we’ve embraced that DIY spirit — combining proven components, modern interfaces, and a little help from AI — to create a pilot system we can trust from Falmouth to the Azores and back.
