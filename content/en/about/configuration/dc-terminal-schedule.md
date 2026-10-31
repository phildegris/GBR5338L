---
title: "DC panel — original handwritten connector schedule"
description: "Owner's Y/R/B cage-clamp schedule and Oceanflex seven-core distribution trunk"
date: 2026-10-31
summary: "Handwritten panel allocations and the forward Oceanflex 7 × 1.5 mm² distribution trunk."
---

[← Configuration](/about/configuration/) · [Electrical reference convention](/about/configuration/electrical-reference-system/) · [Navigation lighting](/about/configuration/navigation-lights/)

> **Source:** Owner's photographed handwritten connector schedule and routing explanation, 31 October 2026. This is a **transcription of historical notes plus an owner-confirmed routing statement**, not a present-day continuity survey. The original photo was shared in the audit conversation; this public page contains the transcription. Ambiguous writing remains flagged.

## How to read the original card

The handwritten columns are **CB / rail / circuit**. The middle column uses the owner's original **individual Yellow–Red–Blue cage-clamp connectors in numbered groups**. A reference like `R2` means red **lever** in group 2, which does not inherently indicate red insulated wire. The left `CB` column indicates a **label or breaker association**, not a verified individual breaker ID.

## Entire legible connector schedule

| Handwritten CB/function | Rail connector | Handwritten circuit / cable | Interpretation or uncertainty |
| --- | --- | --- | --- |
| NAV LTS (stern, partially overwritten) | `B1` | “RG STERN LT” | Stern-light label; “RG” prefix uncertain |
| NAV INSTR | `Y1` | “NMEA 2K B” | NMEA 2000 network B legacy label |
| NAV INSTR | `R1` | “NMEA 2K A” | NMEA 2000 network A legacy label |
| MAST HD | `B2` | “7× BLUE” | Oceanflex blue core, originally labelled masthead |
| STEAM. | `Y2` | “7× YELLOW” | Oceanflex yellow core, originally labelled steaming |
| DECK | `R2` | “7× RED” | Oceanflex red core, originally labelled deck |
| NAV LTS (BOW) | `B3` | “7× GREEN” | Oceanflex green core, originally labelled bow |
| NC | `Y3` | “7× BLACK” | Oceanflex black core; **NC is in CB column**, not proof of disconnect |
| NC | `R3` | “7× BROWN” | Oceanflex brown core; downstream connection unknown |
| NC | `B4` | “7× WHITE” | Oceanflex white core; downstream connection unknown |
| VHF AIS (edited/crossed text) | `Y4` | “RADIO BUS” | Older label; actual connection untraced |
| RADAR | `R4` | “RADAR +” | Older label, no protective device established |
| Cabin/bunk lights (overwritten) | `B5` | “2× RED” | Separate cable reference; exact cable construction unknown |
| SAL LIGHTS | `Y5` | “2× BLACK” | Separate cable reference; conductor dimensions unknown |
| BUNK LIGHTS | `R5` | “AFT CABIN” | Aft cabin label; route unknown |

A crossed-out mark between `Y4` and `R4` **does not justify allocating an additional rail position**. The first-row lettering and corrected lower-left labels should be treated as provisional until the owner confirms them. `NC` is **not** automatically “spare”, “not connected” or “disconnected”.

## Oceanflex 7 × 1.5 mm² distribution trunk

The owner explicitly confirms that **7×** denotes one **Oceanflex 7-core cable**, with **1.5 mm² cross-section for each conductor**. All seven panel-end core identities are now accounted for:

| Core insulation | Panel clamp | Original handwritten function |
| --- | --- | --- |
| Blue | `B2` | Masthead |
| Yellow | `Y2` | Steaming |
| Red | `R2` | Deck |
| Green | `B3` | Bow navigation |
| Black | `Y3` | NC in CB column; older DPDT notes also mention masthead |
| Brown | `R3` | NC in CB column |
| White | `B4` | NC in CB column |

**Owner-confirmed physical routing:**

1. **Origin:** the cage-clamp rail behind the chart-table DC panel (`CT-R`).
2. **Common trunk:** the single **Oceanflex 7 × 1.5 mm²** cable runs **forward to the forecabin starboard locker**, *not directly up the mast*.
3. **Second distribution point:** the seven incoming wires are split through **another set of similar cage-clamp connectors** in that locker.
4. **Distinct outgoing cable runs:** some feed the **bow light and forecabin lighting**, some return aft into the **saloon** space, and some run **via the swan neck up the mast**. These are **different wire runs**, with no individual secondary cable colours or connector allocations yet established.

### Reconciliation with previous “seven-core mast cable” notes

Older [DC Logical Circuits](/about/configuration/logical-circuits/) notes described `B2`, `Y2`, `Y3` as seven-core *mast* wires. That was a functional shorthand and **is not their direct physical route**. These are panel-end cores of the **forecabin-bound trunk**. The onward mast run begins beyond the forecabin secondary connector distribution.

One uncertainty remains: older polarity-selector notes refer to `Y3`/black as a NASA masthead conductor, whereas the photographed hand note has **NC** in its *CB column* for the same black conductor. Preserve both statements without equating NC with an electrically open circuit.

See [DC-NAV-01](/about/configuration/circuits/dc-nav-01/), [DC-NAV-02](/about/configuration/circuits/dc-nav-02/), [DC-NAV-03](/about/configuration/circuits/dc-nav-03/) and [DC-NAV-04](/about/configuration/circuits/dc-nav-04/) for functional protection.

## Next physical survey

Trace the **forecabin starboard-locker secondary cage-clamp connectors**, record each Oceanflex incoming colour, associated outgoing cables, terminal references, joins/bridges, actual returns and destinations. Until then, **panel-end assignment is documented**, but **end-to-end circuit continuity remains unverified**.