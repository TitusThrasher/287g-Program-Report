# 287(g) Program Report

Open data and tooling behind [Titus Consulting](https://tituslegaldesign.com/immigration-101/287g-program)'s
interactive visual report on ICE's 287(g) program — the law enforcement partnership agreements that deputize state and local officers to act on behalf of ICE. 

Learn more about the 287(g) program: [Resource Guide](https://www.tituslegaldesign.com/immigration-101/287-g/explore#:~:text=287(g)%20agencies.-,Learn%20More,-Recommended%20resources%20for)

ICE publishes a spreadsheet of participating agencies, which overwrites the previous 'snapshot' version. There is no changelog, no cancellation date, and no archive. This repository
reconstructs the change history from snapshots, reconciles consecutive editions
into a record of additions and cancelations, and provides a formal methodology on the program-related and community-level population datasets used in the published visual report.

**Report Home Page:** <https://tituslegaldesign.com/immigration-101/287g-program>

**Formal Methodology:** <https://www.tituslegaldesign.com/immigration-101/287-g/report-methodology>

<hr>

## What's here

| Path | Contents |
|---|---|
| `data/active-agreements/` | ICE's active 287(g) agreement list, processed and enriched for report purposes. Weekly CSV snapshots published here with as-of dates for reference. |
| `data/canceled-agreements/` | Archival list of agreements removed from ICE's published list since January 2025. Weekly CSV snapshots published here with as-of dates for reference. |
| `docs/METHODOLOGY.md` | How a cancelation is defined, confirmed, and verified |
| `docs/DATA_DICTIONARY.md` | **COMING SOON** Field-by-field schema for the published files |
| `src/` | **COMING SOON** Deterministic pull scripts and reconciliation pipeline |

<hr>

## License

MIT — see [`LICENSE`](LICENSE). ICE source documents reproduced here are U.S. federal government works and are not subject to copyright.

## Corrections

Data corrections are welcome and appreciated! Please open an issue using the **Data correction** template — it asks for the row, the edition, and the source that contradicts it. See `CONTRIBUTING.md` (coming soon). Alternatively, please feel free to email **info@tituslegaldesign.com** with the correction details.
