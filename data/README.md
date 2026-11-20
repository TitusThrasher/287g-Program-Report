# The 287(g) Program Report's Data

> [!IMPORTANT]
> Each active + canceled agreement file uploaded to this repository represents a snapshot of the processed dataset reflected in the visual report. File names start with the date (e.g. 'Nov-12-2026-Active') on which the snapshot was taken. For "live" current data, please see links below.

> [!NOTE]
> Formal methodology with further detail on data sources, processing, and known limitations is [available here](/docs/METHODOLOGY/methodology.md).

## Agreements


### Active Agreements

[Weekly snapshot](/data/active-agreements) (**CSV**)

[Live 'as-of' data](https://docs.google.com/spreadsheets/d/e/2PACX-1vRZGuLQ58qO5hS1IO-FrF2yGuDHT4QHIDplON_Akdr7mCZyoG8WorUTxsZq60rNTpkfnm1EmLV3gUhX/pub?gid=1164266648&single=true&output=csv) (**Google Sheets CSV download**)

<hr>

### Canceled Agreements

[Weekly snapshot](/data/canceled-agreements) (**CSV**)

[Live 'as-of' data](https://docs.google.com/spreadsheets/d/e/2PACX-1vRZGuLQ58qO5hS1IO-FrF2yGuDHT4QHIDplON_Akdr7mCZyoG8WorUTxsZq60rNTpkfnm1EmLV3gUhX/pub?gid=1393407557&single=true&output=csv) (**Google Sheets CSV download**)

<hr>

## Financials

[Award Records](/data/financials/Nov-10-2026-Award-Records.csv)

[Award Program Details](/data/financials/Award-Program-Details.csv)

<hr>

## Known Limitations

### ICE Agreement Data

List of common issues with ICE's 287(g) program data quality.

| Issue	| Why It's a Problem |
| :------ | :------ |
| 📆 **Publication Schedule** |	Unannounced and inconsistent updates, ranging from multiple new versions in one day (rare) to once per week, or longer. |
| 📷 **Snapshot Publication** | Each version of ICE's spreadsheet replaces the last, with no changelog or basic metadata to keep track of agreement record edits. |
| 🪪 **No Unique Identifiers** | ICE's spreadsheet doesn't include a unique permanent record for each agreement, making it difficult to track changes at scale |
| 📛 **Agency Names** |	Typos (Iuka PD listed as “Luka”), near-spellings, renamed agencies (e.g. for several weeks, an agreement with the Union County Sheriff's Office in North Carolina was abruptly changed to reflect the 'Fayetteville Police Department' instead), extra or missing words, or incorrect word order (e.g. "[City Name] Police Department" vs. "City of [City Name] Police Department]. |
| ✍️ **Signature Dates**	| The `SIGNED` date represents ICE's counter-signature, not the participating agency official's. Some entries list the incorrect date (e.g. the Ottawa County Sheriff's Office in OK: 2025 on the list, 2026 on the MOA).
| 🏷️ **Data Schema** | The columns in ICE's spreadsheet have changed at least once since early 2025; TYPE and COUNTY columns therefore don't exist across the full history. |
| 3️⃣ **Program Totals** |	ICE's own agreement totals, listed on the program landing page, have previously counted the table's header row and over-counted the number of states with active agencies due to typographic errors (e.g. "New Hamsphire" was counted as an additional state for several weeks) |
