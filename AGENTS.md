# Ragtime (GBR5338L) repository guidance

This repository builds Ragtime's Hugo technical website.

## Publishing workflow

- The owner prefers **reviewing changes on the live site** rather than reviewing Markdown or pull requests.
- For agreed changes, commit small, reversible updates directly to `main` and use the existing GitHub Actions publication process.
- Before each change, capture the current `main` commit SHA. Verify that the head has not changed before updating it.
- After a push, report the commit URL, GitHub Actions result (if accessible), and the live page URL. Do not claim the deployment succeeded until verified.
- If the owner requests rollback, use a **new reverting commit** (avoid force-pushing or resetting `main`), preserving unrelated changes.
- Do not include unrelated edits in the same publication commit.
- Update `main` only if its head still matches the baseline; use a conditional reference update where possible. Never reset or force-push.
- Verify the **exact new commit** through separate Hugo-build and GitHub Pages deployment statuses. Inspect the **rendered public page**, including its diagram styling and mobile layout, where possible; a successful build or deployment is not evidence that a particular feature rendered correctly. Distinguish verified rendering from uninspected public output.

## Hugo

- English pages are under `content/en/`.
- Keep internal links and front matter compatible with the existing `roadster` theme and GitHub Actions Hugo build.
- Preserve existing documentation when adding new registers and references.
- Reuse the existing **responsive, accessible, clickable Hugo diagrams** for functional DC and RF paths rather than presenting ASCII code blocks as the primary diagrams. Current conventions: `layouts/shortcodes/dc-distribution.html` and `rf-distribution.html`, diagram definitions in `data/electrical_diagrams/`, and styles in `static/css/ragtime-circuit-diagrams.css`. Link device and circuit boxes to their individual records. Keep diagrams readable on narrow/mobile screens, without mandatory external JavaScript.
- The deployed **Roadster** theme reads `customCSS` (not `custom_css`) in `config/_default/params.yaml`. Verify the exact pinned theme's expectations when changing CSS configuration.
- Diagram YAML is currently a **presentation projection**, not a separately authoritative engineering inventory. When editing any device, circuit, rating, route or connection, reconcile its diagram data, equipment page, circuit record and register entries in the same change. Do not let diagram labels silently contradict the source records. Prefer deriving repeated facts from structured authoritative records as the documentation evolves.
- Keep technical reference PDFs, manufacturer data and relevant wiring/photographic evidence linked from the corresponding equipment page. Do not attribute an installation manual or product specification to an unconfirmed model; manufacturer specs are reference values, **not measurements made aboard**.

## Equipment status — single source of truth

- The **individual equipment Markdown page** under `content/en/about/configuration/equipment/` is the authoritative source for that item's status. Keep the fields in its Hugo front matter, rather than duplicating status in the Equipment Register, Equipment Catalogue or other indexes.
- `survey_state` records evidence about the **physical installation**: `U` means owner-identified/confirmed but not independently electrically surveyed, `T` means tentative or proposed, and `G` means grouped equipment with an unresolved individual count. Do not infer independent verification from owner-confirmed information.
- `documentation_stage: "mapped"` records that identity, location and relevant functional connections are documented from owner evidence, **not** that the installation has been independently inspected, tested or certified. For mapped but unsurveyed records the index renders **Mapped (U)**. Omit the optional field for records not yet mapped.
- Both `content/en/about/configuration/equipment-register.md` and `content/en/about/configuration/equipment/_index.md` must **derive displayed status** through the `{{< equipment-status id="EQ-003" >}}` Hugo shortcode in `layouts/shortcodes/equipment-status.html`. Never reintroduce hard-coded status labels or independently maintained status columns. Update the equipment page's front matter to change the status everywhere.
- Keep documentation progress separate from **as-fitted electrical verification**, and retain survey gaps, measured values and evidence provenance on the equipment detail page. Do not elevate the survey state merely because a documentation diagram or circuit relationship has been completed.
- When allocating a new equipment ID, create its equipment page (including `survey_state`) and use the same status shortcode in **both** indexes; check that every index ID resolves to an existing equipment page.
- When **multiple historical connection cards disagree** about the same multi-core trunk, preserve each original assignment with its source and date, compare them in a reconciliation table, and record the conflict explicitly. Never silently overwrite older handwritten evidence or publish a fused as-built connection as verified. Later owner confirmation of a cable **colour naming scheme** does not necessarily confirm its end-to-end connectivity or resolve disagreement between two different schedules.

- Keep provenance explicit: `owner-confirmed`, `photographically observed`, `taken from legacy notes`, `manufacturer-published`, `estimated`, `measured/tested` and `proposed` are different kinds of evidence. Record test dates and conditions if available. A useful qualitative observation (for example improved radio reception) is not a calibrated signal-loss, range or VSWR measurement.

### Colour-coded DIN cage-clamp groups

- Behind Ragtime's DC panel, the owner arranged **three separate generic cage-clamp connectors** into repeated physical groups, with lever colours always **Yellow, Red, Blue** (`Y`, `R`, `B`) in that order. Groups are numbered sequentially **from the top down**, following the original field notes.
- A legacy reference `B1` means the **blue individual connector in group 1**, `Y2` the **yellow connector in group 2**, and `R4` the **red connector in group 4**. The number is a **group ordinal**, not a terminal number or colour of wire insulation. These references are physical location aliases, **not circuit IDs or equipment IDs**.
- **Never confuse the lever colour with the attached conductor colour.** For example `Y3` can connect a **black insulated wire**; the original documentation explicitly reports this for a NASA masthead conductor. Manufacturer pigtail colours (for example Osculati yellow/brown/white) are a **third, distinct** naming system; do not infer colour-to-colour splices.
- Keep a group-level `TB-NNN` record separate from individual `Y2`/`R2`/`B2` connection positions. Do **not** imply that the three cage clamps in a group are electrically common or form one multi-way connector. Their electrical links, bridged parts (if any), wire occupancy and actual conductor routes require evidence.
- **Partial photographs establish only what they show.** The owner has advised that the connector photo is incomplete: do not infer the full number of groups, wire occupancy, unused clamp positions, colour ordering of hidden parts or complete conductor topology from it.

## Electrical data rules

- Maintain independent **location**, **equipment**, **circuit** and **relationship** identifiers. A location (for example `SL-COM`) is not a device; a circuit name does not encode its fuse or breaker. Keep stable IDs even if equipment moves, a device is replaced or protection is redesigned; preserve the installation/change history.
- Use an individual `CB-NNN` record for a breaker, `FU-NNN` for each identified fitted fuse and `EQ-NNN` for a device or complete subassembly (for example a four-way fuse board). A physical panel coordinate (for example column 3, row 4) or fuse-way number is **an attribute/alias**, not the equipment ID.
- Assign independent circuit records using the established `<SUPPLY>-<SYSTEM>-<NUMBER>` pattern (for example `DC-COM-01`), and make their protection/device relationships explicit in the Circuit Register.
- Model supply, protection and load relationships explicitly; distinguish **feeder protection**, **branch protection**, source, destination and load. Document a 10 A feeder breaker separately from the downstream fuse ratings, even when those ratings happen to match. Equal nominal fuse/breaker ratings do **not** establish selective tripping or protection coordination; actual devices and conductor sizes must be checked.
- Record each fuse-board way as known, unknown, occupied or spare only on evidence. Do not infer that an unidentified fourth way is spare, or allocate a fuse ID/rating to an unconfirmed device.
- A **polarity-reversing two-wire load** must not be given a fixed negative connection simply because one conductor has black insulation. Document both switched legs and their mode/polarity states independently of common-return DC circuits. Distinguish **owner assumptions** about −12 V busbar ties from verified continuity and preserve superseded legacy terminal mappings.
- Distinguish DC supply/protection from **RF and data signal paths**. Passive antenna coax is a signal connection, not a new fused DC circuit; a shared VHF/AIS antenna carries bidirectional transmit/receive signals. Record cable type, route, joints and terminations as supplied; do not invent length, insertion loss, connector details or SWR readings.
- During the house-bank source audit, model the **entire house bank as one aggregate electrical source interface** (`EQ-059`). Do not duplicate batteries, claim installed chemistry/capacity or incorporate LiFePO4 refit proposals until the separate battery-component survey. The **five functional service circuits** from house-bank distribution are Watchkeeper, Pump 1 and Pump 2 (**unswitched by the one common remote switch**), plus House and Autopilot (**both switched together** by **one owner-confirmed physical remote switch, `SW-002`**). Do not infer two independent switches or independently controllable House/Pilot service states: the switched feed splits to two **separate circuits** downstream of **one common remote contact**. The switch manufacturer/model remains unverified as currently installed, though an August 2025 photograph shows a WhisperPower-branded unit. Fuseholders, fuse ratings and exact wiring need tracing.
- The house-bank **negative copper link** (`BB-004`) connects the existing battery negative terminals to the **battery side** of the Victron BMV-712 shunt (`EQ-060`). All load and charging returns must connect on the shunt **system/load side** for accurate net-bank monitoring; the downstream negative busbar's actual physical connection remains subject to inspection. Preserve custom copper-bar design dimensions as **historical design**, not installed measurements.
- Retain existing physical breaker, terminal and busbar references as aliases during migration.
- Distinguish **multi-core panel-to-distribution trunks** from the separate outgoing legs after intermediate connectors. A conductor labelled for a masthead load is not proof the original multi-core cable physically reaches the mast. Record each junction, branch, conductor cross-section and provenance. Keep handwritten `NC` labels verbatim; never silently treat them as `unused`, `spare` or `disconnected`.
- Clearly distinguish proposed information from **installed/owner-confirmed**, **physically inspected**, **tested/measured** and **verified-as-built** electrical configurations. Preserve unverified conductor size, fuse format, return path, fuse rating, serial number and device variants as explicit unknowns until evidence is supplied.
- Never invent component ratings, cable sizes, terminals or wiring connections.
- See `content/en/about/configuration/electrical-reference-system.md` for the reference convention; `content/en/about/configuration/circuit-register.md` is the circuit-to-protection inventory and the individual equipment pages supply asset-level details.
- On each technical change, check internal links and consistency across the **Equipment Register, Catalogue, Circuit Register, equipment/circuit detail pages and diagrams**, as applicable. In particular, status must never be independently copied into either equipment index.
- Keep the public site free of passwords, secrets, network credentials and unnecessary identifying operational details.


## Technical documentation versus maintenance backlog

- The Hugo website is the **technical system-of-record** for equipment identities, as-fitted/owner-confirmed configuration, circuits, interconnections, references and survey evidence. **Trello is the existing operational maintenance and refit backlog**, with its own established workflow; do not import, reorganise or duplicate the whole backlog on the website.
- If explicitly requested, cross-link a maintenance card to the affected stable equipment or circuit ID, but do not treat an open Trello task as evidence that a physical configuration or test result has been verified. Keep task state separate from the technical record's `survey_state` and `documentation_stage`.
