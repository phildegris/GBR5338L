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

## Electrical data rules

- Maintain independent location, equipment and circuit identifiers.
- Model supply, protection and load relationships explicitly; distinguish branch and upstream protection.
- Retain existing physical breaker, terminal and busbar references as aliases during migration.
- Clearly distinguish proposed information from installed, surveyed and verified-as-built electrical configurations.
- Never invent component ratings, cable sizes, terminals or wiring connections.
- See `content/en/about/configuration/electrical-reference-system.md` for the initial convention.
