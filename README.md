# 287(g) Program Report

Open data and tooling behind [Titus Consulting](https://tituslegaldesign.com/287g-program/report)'s interactive visual report on ICE's 287(g) program — the law enforcement partnership agreements that deputize state and local officers to act on behalf of ICE. 

<https://datastudio.google.com/embed/reporting/ebe8be08-53be-4afc-9240-83ec3075e873/page/p_5yty8mz8xd>

Learn more about the 287(g) program: [Resource Guide](https://www.tituslegaldesign.com/immigration-101/287-g/explore#:~:text=287(g)%20agencies.-,Learn%20More,-Recommended%20resources%20for)

ICE publishes a spreadsheet of participating agencies, which overwrites the previous 'snapshot' version. There is no changelog, no cancelation date, and no archive. This repository reconstructs the change history from snapshots, reconciles consecutive editions into a record of additions and cancelations, and provides a formal methodology on the program-related and community-level population datasets used in the published visual report.

**Report Home Page:** <https://tituslegaldesign.com/287g-program/report>

**Formal Methodology:** <https://www.tituslegaldesign.com/287g-program/report-methodology>

<hr>

[![](https://mermaid.ink/img/pako:eNp1U01v2zAM_SuCekmxyIntfE23IulhhwBFC7TYkItqMbZWWzIkak0W9L9PsptuQ1zBNqxH8vGRok60MBIop4yxnS6M3quS7zQhaAEeFbx2G0JcZV6_BbPjweKhByXsha8x4neieOGkEQhWiZqpADGsoHn3hAOCdsronqMHCUkw8h1bcIVVLf4DHzixIApk6P6iB-REGx04O7VniewZUJy9-pWtliW7s6a0omH30BqLk_894rq_vdlsbwnnvFJlVYcXSVQ-2qsarsnVFfluPBEWSAUWLuOTUmHlnweYpUAxiQRPAC_1kTgt2tBCdGS0fni8vgyI66ZA9QsmZNi6FrqAGuRQNlO4Lluo-CcUGAHfgEaBoeXDdJugkG1UET2EPQ479Z1jW8DKSFOb8hO_B-NtASxyXtguIxqQqu_OWvUSHfnSo-HQ96HVoVI3nKnzSho5QGvBdTL6Vqy9DcMoSemVBIKGeC3BOhRaKl3GARmVn5zDB1HIQ8e0tEpSHqd-TBuwjYhbeoqxO9rPOOXh9_027OhOv4WwVugfxjTnSGt8WVG-F7ULO9-GCYGNEnFAP9BQeNC4Nl4j5av5mIZi0dhtf0O7i9rxUn6iB8pneZpk4ZNNF1_n03SVj-mR8izNk3m-XGVZtsqWs3mWvY3p707JNJnl-SxNp4t0ucjDM3v7A6OiHR4?type=png)](https://mermaid.live/edit#pako:eNp1U01v2zAM_SuCekmxyEnsfE23IulhhwBFA7TYkItqMbZWWzIkak0W5L9PsptuQ1zBNqxH8vGRok40NxIop4yxnc6N3quC7zQhaAGeFLy1G0Jcad6-BbPjweKhAyXsha8w4g8if-WkFghWiYqpADEsoX73hAOCdsrojqMDCUkw8h0bcLlVDf4DHzixIHJk6P6iB-REGx04W7UXiewFUFy8upUuFwV7sKawomaP0BiLo_894nq8v1tv7gnnvFRFWYUXSVQ-2KsKbsnNDdmisPjdeCIskBIsXJMkhcLSv_TQS4FiFFmeAV6rI3FaNKGP6MhgtX26vQ6I6y5H9QtGpN-6EjqHCmRfNpO7Nlso-yfkGAFfg0aBoe_9dOugkK1VHj2EPfY7de1jG8DSSFOZ4hO_rfE2BxY5r2zXETVI1XVnpTqJjnzp0HDy-9DqUKnrz9R6JbXsobXgWhldK1behomUpPBKAkFDvJZgHQotlS7ilAyKT87hgyjkoUNaWCUpj6M_pDXYWsQtPcXYHe0GnfLw-34ldnSnzyGsEfqHMfUl0hpflJTvReXCzjdhQmCtRJzSDzQUHjSujNdI-Xw2pKFYNHbTXdP2tra8lJ_ogfJpNknS8EnH86-z8WSZDemR8nSSJbNssUzTdJkuprM0PQ_p71bJOJlm2XQyGc8ni3kWnun5D1JXHyo)

## What's here

| Name | Path | Contents |
|---|---|---|
| Active Agreements (**Data: CSV**) | [`data/Active`](data/Active) | ICE's active 287(g) agreement list, processed and enriched for report purposes. Weekly CSV snapshots published here with as-of dates for reference. |
| Canceled Agreements (**Data: CSV**) | [`data/Canceled`](data/Canceled)| Archival list of agreements removed from ICE's published list since January 2025. Weekly CSV snapshots published here with as-of dates for reference. |
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
<picture>

## Corrections

Data corrections are welcome and appreciated! `CONTRIBUTING.md` + corrections form coming soon. In the meantime, please email **info@tituslegaldesign.com** with the correction details.
