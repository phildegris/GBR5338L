---
title: "DC-N2K-02 — Segment A power injection behind DCP"
description: "Owner-confirmed NMEA 2000 power supply relationship"
circuit_id: "DC-N2K-02"
date: 2026-11-06
---

[← Circuit Register](/about/configuration/circuit-register/) · [NMEA 2000 network](/about/configuration/nmea2000-configuration/)

**Owner-confirmed functional supply, 6 November 2026; not independently electrically surveyed.**

| Field | Record |
| --- | --- |
| Circuit ID | `DC-N2K-02` |
| Destination / function | Segment A power injection behind DCP |
| Known protection | Common **10 A NAV INSTR [CB-007](/about/configuration/equipment/cb-007/)** |
| Source | Main DC panel; detailed upstream connection not traced |
| Switching | A and B share CB-007; any additional downstream switching unconfirmed |
| Historical connection reference | Historical R1 / NMEA 2K A — continuity untraced |
| Local protection | Additional downstream fuses not yet established |
| Wiring / return | Split point, injection hardware, conductor sizes, lengths and negative-return route untraced |

See [DC-N2K-01](/about/configuration/circuits/dc-n2k-01/) for the common supply, [DC-N2K-02](/about/configuration/circuits/dc-n2k-02/) for A and [DC-N2K-03](/about/configuration/circuits/dc-n2k-03/) for B. These circuit IDs do not imply additional breakers or verified protection coordination. Positive-supply separation at [EQ-063](/about/configuration/equipment/eq-063/) is distinct from shared upstream supply/protection.
