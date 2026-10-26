# 287(g) Program Report

Open data and tooling behind [Titus Consulting](https://tituslegaldesign.com/287g-program/report)'s interactive visual report on ICE's 287(g) program — the law enforcement partnership agreements that deputize state and local officers to act on behalf of ICE. 

<https://datastudio.google.com/embed/reporting/ebe8be08-53be-4afc-9240-83ec3075e873/page/p_5yty8mz8xd>

Learn more about the 287(g) program: [Resource Guide](https://www.tituslegaldesign.com/immigration-101/287-g/explore#:~:text=287(g)%20agencies.-,Learn%20More,-Recommended%20resources%20for)

ICE publishes a spreadsheet of participating agencies, which overwrites the previous 'snapshot' version. There is no changelog, no cancelation date, and no archive. This repository reconstructs the change history from snapshots, reconciles consecutive editions into a record of additions and cancelations, and provides a formal methodology on the program-related and community-level population datasets used in the published visual report.

**Report Home Page:** <https://tituslegaldesign.com/287g-program/report>

**Formal Methodology:** <https://www.tituslegaldesign.com/287g-program/report-methodology>

<hr>

## What's here

| Name | Path | Contents |
|---|---|---|
| Active Agreements (**Data:CSV**) | [`data/Active`](data/Active) | ICE's active 287(g) agreement list, processed and enriched for report purposes. Weekly CSV snapshots published here with as-of dates for reference. |
| Canceled Agreements (**Data:CSV***) | [`data/Canceled`](data/Canceled)| Archival list of agreements removed from ICE's published list since January 2025. Weekly CSV snapshots published here with as-of dates for reference. |
| Report Methodology (**Docs**)| [`docs/Report-Methodology.md`](docs/Report-Methodology.md) | Formal report methodology, including data processing and standards. |
| Data Dictionary (**Docs**) | [`docs/Data-Dictionary.md`](docs/Data-Dictionary.md) | Field-by-field schema and definitions for the published files. |
| Source Data (**Docs**) | [`docs/Source-Data.md`](docs/Source-Data.md) | Details on primary and secondary data sources used in the report. |
| Media References | [`media/`](media/media.md) | Table of media references + citations for the report. |
| Resources Guide | [`resources/`](resources/resources.md) | Public and professional resources for understanding the 287(g) program and its impact on local communities. |
| `src/` | **COMING SOON** | Deterministic pull scripts and reconciliation pipeline. |

<hr>

## License

MIT — see [`LICENSE`](LICENSE). ICE source documents reproduced here are U.S. federal government works and are not subject to copyright.

## Author/Creator

A [Titus Consulting](tituslegaldesign.com) product, proudly based in Chicago.

## Corrections

Data corrections are welcome and appreciated! `CONTRIBUTING.md` + corrections form coming soon. In the meantime, please email **info@tituslegaldesign.com** with the correction details.
