# Data licence & attribution

The **code** in this repository (the dbt models, the Python in `pipeline/` and `scripts/`) is MIT licensed — see [LICENSE](LICENSE).

The **data** is a different matter, and it is not mine to relicense.

## Upstream source

All ball-by-ball and match data originates from **[Cricsheet](https://cricsheet.org)**, which publishes it under the **[Open Data Commons Open Database License (ODbL) v1.0](https://opendatacommons.org/licenses/odbl/1-0/)**.

Everything in `data/base/` is a parse of Cricsheet's `ipl_male_json.zip`. Everything in `data/marts/` is derived from that by the dbt models in `dbt/`. Both are therefore **derivative databases** under the ODbL, and the ODbL travels with them.

## What that means for you

The ODbL is a share-alike licence. In plain terms, if you use this data you must:

1. **Attribute** — credit Cricsheet as the source. A link to <https://cricsheet.org> is enough.
2. **Share alike** — if you publicly distribute a modified or extended version of the *database*, license it under the ODbL too.
3. **Keep it open** — if you distribute the database in a form that restricts access (for example, behind DRM), you must also make an unrestricted version available.

Note that ODbL covers the *database*. Analyses, charts, models and articles you produce *from* the data are "Produced Works" — you may license those however you like, provided you still credit the source.

This is a summary written for convenience, not legal advice. The [full ODbL text](https://opendatacommons.org/licenses/odbl/1-0/) governs.

## Suggested attribution

> IPL data from [Cricsheet](https://cricsheet.org), licensed under the [ODbL](https://opendatacommons.org/licenses/odbl/1-0/).

## Squad and auction data

`squads` / `dim_squads` and `stg_auctioned_players` contain player profile and IPL 2026 auction information compiled from public ESPNCricinfo listings. This is factual reference data (name, role, team, price) rather than creative content. It is provided for research and analysis; ESPNCricinfo is not affiliated with this project and does not endorse it.

## No warranty

The data is provided as-is. It is a static snapshot (see `data/MANIFEST.md` for the export date), it may contain upstream errors, and it is not an official IPL or BCCI product. Do not rely on it for anything that matters without checking it yourself.
