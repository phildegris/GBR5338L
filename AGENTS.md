# Ragtime (GBR5338L) repository guidance

This repository builds Ragtime's Hugo technical website.

## Publishing workflow

- The owner prefers **reviewing changes on the live site** rather than reviewing Markdown or pull requests.
- For agreed changes, commit small, reversible updates directly to `main` and use the existing GitHub Actions publication process.
- Before each change, capture the current `main` commit SHA. Verify that the head has not changed before updating it.
- After a push, report the commit URL, GitHub Actions result (if accessible), and the live page URL. Do not claim the deployment succeeded until verified.
- If the owner requests rollback, use a **new reverting commit** (avoid force-pushing or resetting `main`), preserving unrelated changes.
- Do not include unrelated edits in the same publication commit.

## Hugo

- English pages are under `content/en/`.
- Keep internal links and front matter compatible with the existing `roadster` theme and GitHub Actions Hugo build.
- Preserve existing documentation when adding new registers and references.

## Equipment status — single source of truth

- The **individual equipment Markdown page** under `content/en/about/configuration/equipment/` is the authoritative source for that item's status. Keep the fields in its Hugo front matter, rather than duplicating status in the Equipment Register, Equipment Catalogue or other indexes.
- `survey_state` records evidence about the **physical installation**: `U` means owner-identified/confirmed but not independently electrically surveyed, `T` means tentative or proposed, and `G` means grouped equipment with an unresolved individual count. Do not infer independent verification from owner-confirmed information.
- `documentation_stage: "mapped"` records that identity, location and relevant functional connections are documented from owner evidence, **not** that the installation has been independently inspected, tested or certified. For mapped but unsurveyed records the index renders **Mapped (U)**. Omit the optional field for records not yet mapped.
- Both `content/en/about/configuration/equipment-register.md` and `content/en/about/configuration/equipment/_index.md` must **derive displayed status** through the `{{< equipment-status id="EQ-003" >}}` Hugo shortcode in `layouts/shortcodes/equipment-status.html`. Never reintroduce hard-coded status labels or independently maintained status columns. Update the equipment page's front matter to change the status everywhere.
- Keep documentation progress separate from **as-fitted electrical verification**, and retain survey gaps, measured values and evidence provenance on the equipment detail page. Do not elevate the survey state merely because a documentation diagram or circuit relationship has been completed.
- When allocating a new equipment ID, create its equipment page (including `survey_state`) and use the same status shortcode in **both** indexes; check that every index ID resolves to an existing equipment page.

## Electrical data rules

- Maintain independent location, equipment and circuit identifiers.
- Model supply, protection and load relationships explicitly; distinguish branch and upstream protection.
- Retain existing physical breaker, terminal and busbar references as aliases during migration.
- Clearly distinguish proposed information from installed, surveyed and verified-as-built electrical configurations.
- Never invent component ratings, cable sizes, terminals or wiring connections.
- See `content/en/about/configuration/electrical-reference-system.md` for the initial convention.
