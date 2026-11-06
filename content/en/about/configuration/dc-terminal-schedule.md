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
| NAV INSTR | `Y1` | “NMEA 2K B” | NMEA 2000 segment B historical label; injection behind DCP owner-confirmed, connector continuity untraced |
| NAV INSTR | `R1` | “NMEA 2K A” | NMEA 2000 segment A historical label; injection behind DCP owner-confirmed, connector continuity untraced |
| MAST HD | `B2` | “7× BLUE” | Handwritten masthead label preserved; owner says **NASA switched pair is R3/B4**, not B2 |
| STEAM. | `Y2` | “7× YELLOW” | Oceanflex yellow core, originally labelled steaming |
| DECK | `R2` | “7× RED” | Oceanflex red core, originally labelled deck |
| NAV LTS (BOW) | `B3` | “7× GREEN” | Oceanflex green core, originally labelled bow |
| NC | `Y3` | “7× BLACK” | Original NC preserved; older NASA association **superseded**, common-negative hypothesis untested |
| NC | `R3` | “7× BROWN” | **Original label preserved**; later owner-confirmed NASA Combi switched conductor |
| NC | `B4` | “7× WHITE” | **Original label preserved**; later owner-confirmed NASA Combi switched conductor |
| VHF AIS (edited/crossed text) | `Y4` | “RADIO BUS” | Older label; actual connection untraced |
| RADAR | `R4` | “RADAR +” | Older label, no protective device established |
| Cabin/bunk lights (overwritten) | `B5` | “2× RED” | Separate cable reference; exact cable construction unknown |
| SAL LIGHTS | `Y5` | “2× BLACK” | Separate cable reference; conductor dimensions unknown |
| BUNK LIGHTS | `R5` | “AFT CABIN” | Aft cabin label; route unknown |

A crossed-out mark between `Y4` and `R4` **does not justify allocating an additional rail position**. The first-row lettering and corrected lower-left labels should be treated as provisional until the owner confirms them. `NC` is **not** automatically “spare”, “not connected” or “disconnected”.

**NMEA 2000 clarification (owner, 6 November 2026):** A and B are two segments of one network; each has power injection behind DCP. The owner also confirms a [power isolator (EQ-063)](/about/configuration/equipment/eq-063/) between the segments, passing CAN data while separating positive supplies. This does not independently verify the historical `R1`/`Y1` connections; the isolator’s physical location and model remain unreported. See the [network and power record](/about/configuration/nmea2000-configuration/).

## Oceanflex 7 × 1.5 mm² distribution trunk

The owner explicitly confirms that **7×** denotes one **Oceanflex 7-core cable**, with **1.5 mm² cross-section for each conductor**. All seven panel-end core identities are now accounted for:

| Core insulation | Panel clamp | Original handwritten function |
| --- | --- | --- |
| Blue | `B2` | Masthead (handwritten historical label; **superseded** for NASA Combi switched pair) |
| Yellow | `Y2` | Steaming |
| Red | `R2` | Deck |
| Green | `B3` | Bow navigation |
| Black | `Y3` | NC in CB column; old DPDT note mentions NASA (superseded); **−12 V common connection is an assumption, not electrically measured** |
| Brown | `R3` | NC in CB column; **owner confirms this is one NASA Combi switched conductor** |
| White | `B4` | NC in CB column; **owner confirms this is the other NASA Combi switched conductor** |

**Owner-confirmed physical routing:**

1. **Origin:** the cage-clamp rail behind the chart-table DC panel (`CT-R`).
2. **Common trunk:** the single **Oceanflex 7 × 1.5 mm²** cable runs **forward to the forecabin starboard locker**, *not directly up the mast*.
3. **Second distribution point:** the seven incoming wires are split through **another set of similar cage-clamp connectors** in that locker.
4. **Distinct outgoing cable runs:** some feed the **bow light and forecabin lighting**, some return aft into the **saloon** space, and some run **via the swan neck up the mast**. These are **different wire runs**, with no individual secondary cable colours or connector allocations yet established.

## Second handwritten card — trunk-core functional allocations

**Evidence:** A second photographed handwritten card supplied by the owner on 31 October 2026. The owner explicitly confirms the **colour names on this card refer to the seven insulated conductors of the same Oceanflex 7 × 1.5 mm² panel-to-forecabin trunk**, **not** to the separate 2-core NASA or 3-core Osculati mast cables. `SAL` means the saloon's array of **12 LED downlights**, which will be documented separately. The card is transcribed below; it has not been electrically continuity-tested, and the **precise physical end/location described by the card is not yet established**.

| Seven-core trunk insulation | Second card's writing | Functional interpretation from card | First card's handwritten panel reference | Reconciliation |
| --- | --- | --- | --- | --- |
| **Blue** | `SAL + BLUE` | Saloon downlights positive | `B2` — `MAST HD` | **Different labels**; location/revision unresolved |
| **Yellow** | `SAL − YELLOW` | Saloon downlights negative | `Y2` — `STEAM.` | **Different labels**; do not assume common power or hard-wired joins |
| **White** | `COMBI WHITE` | One NASA Combi polarity-switched conductor | `B4` — `NC` | Consistent with **later owner-confirmed** NASA R3/B4 pair; old NC retained as historical CB label |
| **Brown** | `COMBI BROWN` | Other NASA Combi polarity-switched conductor | `R3` — `NC` | Consistent with **later owner-confirmed** NASA R3/B4 pair; polarity swaps by SW-001 |
| **Green** | `STEAM + GREEN` | Steaming-light positive | `B3` — `NAV LTS (BOW)` | **Different labels**; branch allocation requires tracing |
| **Red** | `DECK + RED` | Deck-light positive | `R2` — `DECK` | **Agreement on deck function** |
| **Black** | `STEAM DECK − BLACK` | Shared return for steaming/deck light functions, **as labelled on card** | `Y3` — `NC` | Adds evidence for intended common-negative use; physical connection to −12 V busbar remains unverified |

**Evidence hierarchy:** The owner-confirmed *identities* of all seven cores and their physical route to the forecabin locker are established. The **functional descriptions of blue, yellow and green conflict between the two handwritten cards**. We must not represent both simultaneously as a verified electrical circuit, infer that a core changes purpose along a continuous conductor, or conflate a cable's insulation colour with the **colour-coded DIN clamp lever**. These differences could reflect different connection locations, revisions or old annotations; **none of those explanations is confirmed**.

**Specific constraints:** White and brown are the two **reversible-polarity** NASA conductors under [SW-001](/about/configuration/equipment/sw-001/) and do not have permanent +/− assignments. The second card labels black as a common negative **for the steaming/deck functions only**, not the NASA Combi; this does not itself prove the physical negative-busbar connection. The colours written here are **seven-core trunk colours only**, not the insulated wire colours of the **separate Oceanflex 2 × 1.5 mm² NASA mast cable** or **3 × 1.5 mm² Osculati mast cable**.

The original first-card table and its `NC` column values above remain unchanged as a separate historical source. The next decisive task is to trace the starboard forecabin locker clamp connections and record which core goes to each outgoing cable.

### Reconciliation with previous “seven-core mast cable” notes

Older [DC Logical Circuits](/about/configuration/logical-circuits/) notes described `B2`, `Y2`, `Y3` as seven-core *mast* wires. That was a functional shorthand and **is not their direct physical route**. These are panel-end cores of the **forecabin-bound trunk**. The onward mast run begins beyond the forecabin secondary connector distribution.

**Superseding owner clarification, 31 October 2026:** The NASA Combi's **two switched conductors use `R3`/brown and `B4`/white** of the 7 × 1.5 mm² Oceanflex distribution trunk, connected through the DC panel's cage-clamp rail to the DPDT polarity switch **SW-001**. From the forecabin starboard-locker distribution these connect to the mast's **separate 2 × 1.5 mm² Oceanflex cable** (the cable includes a black-insulated core). **Which of the two mast-cable cores joins brown or white is not yet recorded.** The two NASA conductors are polarity-reversed by SW-001, so neither must be drawn as a permanently earthed/−12 V return.

The handwritten CB column records `NC` for `R3` and `B4`, while the earlier DPDT sketch mentioned `B2`/blue and `Y3`/black as the masthead pair. Retain both as **historical annotations superseded by the owner's latest as-fitted clarification**; do not rewrite the photographic transcription. The `B2` handwritten `MAST HD` label remains as a historical *function label*, but is **not proof that the NASA Combi uses B2**. The older `Y3` black masthead relationship is superseded.

**Black return: handwritten functional label, not a traced electrical connection.** The second card labels the seven-core **black** conductor as `STEAM DECK − BLACK`; the owner also previously proposed black cores associated with a common **−12 V busbar**. Neither is a continuity measurement. The black core of the **seven-core trunk** and the black core of the **separate 3 × 1.5 mm² Oceanflex steaming/deck mast cable** may be connected to that busbar; the actual junctions have not been measured or traced. That hypothesis **does not apply to the black core of the 2-core NASA Combi cable**, which is part of the polarity-reversing two-wire pair. The **3-core mast cable** serves the steaming and deck functions of [Osculati EQ-020](/about/configuration/equipment/eq-020/); do not infer its two positive wire colours from the manufacturer pigtail or the upstream seven-core colour codes.

See [DC-NAV-01](/about/configuration/circuits/dc-nav-01/), [DC-NAV-02](/about/configuration/circuits/dc-nav-02/), [DC-NAV-03](/about/configuration/circuits/dc-nav-03/) and [DC-NAV-04](/about/configuration/circuits/dc-nav-04/) for functional protection.

## Next physical survey

Trace the **forecabin starboard-locker secondary cage-clamp connectors**, record each Oceanflex incoming colour, associated outgoing cables, terminal references, joins/bridges, actual returns and destinations. Until then, **panel-end assignment is documented**, but **end-to-end circuit continuity remains unverified**.