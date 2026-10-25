# 287(g) Program Tracker: Report Methodology
 
**Version 1.4** · Supersedes v1.3 (October 13, 2026)

## 1. Scope

The report tracks agreements executed under Section 287(g) of the Immigration and Nationality Act, which authorizes ICE to delegate specified immigration enforcement functions to state and local law enforcement agencies. 

It covers three program models: 

- Jail Enforcement Model (JEM);
- Warrant Service Officer (WSO);
- Task Force Model (TFM).

It also covers three levels of policing across local and state government:
- Local (municipal) police departments;
- County sheriffs' offices, district attorneys' offices, and other county-level agencies;
- State law enforcement agencies, like highway patrols and departments of corrections.

The primary unit of analysis is the agreement, not the agency. Agency-level counts are deduplicated.

<hr>

## 2. Data sources

### 2.1 Primary — ICE published agreement list

ICE publishes an Excel file of currently active agreements on its [287(g) program page](https://www.ice.gov/identify-and-arrest/287g). Publication is irregular and unannounced. Each file is a complete replacement of its predecessor and reflects only the agreements active at time of publication. ICE provides no changelog, no version history, and no persistent unique identifiers.

### 2.2 Derived — Canceled agreements

Reconstructed by differencing consecutive locally archived snapshots; backfilled data from January to December 2025 courtesy of Elijah Appelson's public [287(g) scraper and archive repository](https://github.com/appelson/Tracking_287g/tree/main). See [§3.2](#32-change-detection). Coverage begins January 01, 2025.

### 2.3 Arrest data — Deportation Data Project

ICE administrative 'Arrest with detention' records obtained under FOIA and processed by the Deportation Data Project. Includes arrest records leading to ICE detention recorded between October 01, 2022 and August 06, 2026. For the purposes of this report, we have then filtered the dataset to focus on arrests recorded from January 01, 2025 to August 06, 2026. Used solely for the 287(g)-related arrest analysis section of the report; this data is not joined to the agreement dataset at the record level. For more on Deportation Data Project's data processing, please refer to the organization's 'ICE core data codebook'.

### 2.4 Payment data — Federal reimbursements and state grants

Compiled from published journalism, state award listings, agency budget and auditor records, and leaked documents. Maintained in two places in the source dataset: a 'Confirmed TFM Reimbursements + Invoices' field on the agreement record (when independently verified), and a separate State Grants table. Not a systematic collection. See [§6.4](#64-payment-data).

### 2.5 Reference data

- `Location`: publicly sourced address data, taken from the agency's official website wherever available, normalized to "[City], [State Abbreviation] [ZIP]" or "[Physical Address], [City], [State Abbreviation] [Zip]" for compatibility with Google Data Studio geographic mapping.

- `Population`: estimates, matched to each agency's corresponding jurisdiction (municipality, county, or statewide). U.S. Census Bureau [American Community Survey (ACS) 2024‍](https://www.census.gov/programs-surveys/acs/data.html)

- Law Enforcement Agency (LEA) Totals: State-level agency counts come from the [2018 Census of State and Local Law Enforcement Agencies](https://bjs.ojp.gov/library/publications/census-state-and-local-law-enforcement-agencies-2018-statistical-tables) from the U.S. Department of Justice's Bureau of Justice Statistics.

<hr>

## 3. Collection

### 3.1 Snapshot capture

Each published ICE file is first downloaded and manually filtered by 'Signed' date to identify agreements newly added to ICE's snapshot raw data. Discrepancies, including agreements added with retroactive 'Signed' dates, are then detected via the composite key script described below (See [§3.2](#32-change-detection)). After processing and manual enrichment (`Location` field) and automated enrichment (`Population` field, which pulls Census ACS data automatically), new records added to the primary list of active agreements (available for [download here](https://docs.google.com/spreadsheets/d/e/2PACX-1vRZGuLQ58qO5hS1IO-FrF2yGuDHT4QHIDplON_Akdr7mCZyoG8WorUTxsZq60rNTpkfnm1EmLV3gUhX/pub?gid=1164266648&single=true&output=csv)) are then fetched and auto-populate to the visual report in Data Studio within 15 minutes.

### 3.2 Change detection

Each new snapshot is compared against the immediately preceding snapshot using a composite key of state + agency name + agreement type + signature date. Rows present in the prior snapshot and absent from the new one are flagged as potential cancelations; rows present in the new snapshot only are flagged as potential additions.

Because the composite key contains no stable identifier, it is sensitive to upstream edits. Every flagged row is reviewed and cross-checked manually before classification, specifically to distinguish genuine removals from re-naming and model switches.

### 3.3 Classifying removals

Each agreement removed from ICE’s list is assigned a '**Cancel Reason**':

- **Unknown/Other**: No public reason for the cancelation is available; the participating agency holds no remaining active agreements.
- **Consolidation/Re-signed**: An agreement is removed, but the participating agency maintains at least one other active agreement.
- **State Legislation**: Agreement canceled in response to state-level legislation that restricts or bars agencies from participating in the 287(g) program.
- **State Executive Order/Directive**: Agreement canceled in response to an executive directive from the state governor which restricts or bars agencies from participating in the 287(g) program.
- **Local/County Govt. Vote**: Agreement canceled in response to a vote by the controlling/governing body (e.g. town council or county board of commissioners).
- **Voluntary Cancelation by LEA**: Agreement canceled voluntarily by the participating law enforcement agency.
- **Unauthorized Agreement**: Agreement canceled because of lack of proper authorization.

<hr>

## 4. Processing

The published report reflects a processed version of ICE's data. Processing is limited to independently verifiable data, and consists of:

- correcting typographic errors and level-of-government discrepancies;
- reconciling verifiable discrepancies in agency and jurisdiction names;
- trimming errant whitespace;
- enriching with reference data ([§2.5](#25-reference-data));
- correction of other verifiable data entry errors.

Corrections are recorded in the 'Notes' field on the affected record. Two representative examples:

Signature date: ICE's published list shows a signature date of February 23, 2025 for the Ottawa County Sheriff's Office (OK). The corresponding Memorandum of Agreement published by ICE shows February 23, 2026. The report reflects the date in the MOA.

Agency name:  The Iuka Police Department (MS) was initially published by ICE as "Luka Police Department." Corrected to "Iuka" against the agency's own records.

> [!IMPORTANT]
> Standing rule: Where ICE's published list conflicts with an underlying primary document published by ICE itself, or similar primary evidence, the primary document controls, and the discrepancy is noted on the record.

<hr>

## 5. Operational definitions

- **Agreement**: A single 287(g) Memorandum of Agreement (MOA), an intergovernmental contract instrument entered by ICE and one agency under one program model. The report's base unit.

- **Agency**: A unique law enforcement body, deduplicated across models. May hold up to three agreements.

- **Active**: Present on the most recently processed ICE snapshot list.

- **Canceled**: Agreements that were previously present on the list and subsequently removed by ICE, and therefore missing from subsequent snapshot releases. Each is manually confirmed as a removal (rather than a renaming, program model switch, or other updates). Coverage begins January 01, 2025.

- **Administrative arrest**: Per Deportation Data Project, a unique record for "every time ICE arrests someone, whether or not that arrest results in a decision to detain the person."

- **287(g)-related arrest**: An 'administrative arrest with detention' as defined by Deportation Data Project ([DDP codebook](https://deportationdata.org/docs/ice/codebook.html)) carrying one or more qualifying ICE tags. Union logic; unweighted; deduplicated.

- **Confirmed payment**: A federal reimbursement or state grant to a participating agency evidenced by a primary or credibly reported secondary source. Not a comprehensive record.

- **Estimated population**: ACS 2024 estimate for the jurisdiction corresponding to the agency. 'Not Found' where the agency's authority covers only part of a larger jurisdiction and the sub-jurisdiction is not independently verifiable (applied as default for township- and borough-level police departments).

<hr>

## 6. Limitations and sources of error

### 6.1 Snapshot publishing

No historical series is published by ICE. Every time-series figure in this report is reconstructed and bounded by the start of our own archive.

### 6.2 Identifier fragility

The composite key is a known weak link in the pipeline, and so a unique slug is the next step in creating a unique identifier for each agreement. With the composite ID, silent upstream edits to an agency name or signature date break the match and can generate a spurious cancelation-plus-addition pair flag, which is why every change is manually reviewed to help mitigate this issue. However, it does not eliminate the fragility entirely, and so users should treat single-record cancelation claims with slightly more caution than aggregate trends, particularly because we have seen some records removed from ICE's published list and subsequently re-added several days later (occasionally with other, substantive, edits made).

### 6.3 Arrest analysis

The classification depends entirely on ICE's own coding processes, which are demonstrably inconsistent across the two fields we use in this analysis— almost certainly representing an undercount of total 287(g)-related arrests across this period of time. The reported correlation (r = 0.86) between 287(g)-related monthly arrest totals and total monthly ICE administrative arrests is descriptive, and doesn't necessarily confirm causal inference. 

The arrest dataset, provided by ICE to Deportation Data Project in late August 2026, terminates August 06, 2026. While most 287(g)-coded arrest records include an 'Apprehension city' value, individual records almost never include data to properly attribute an arrest back to the local/county/state agency that made the arrest on ICE's behalf. This is particularly important to consider where agency jurisdictions overlap and regional task forces operate, and in other scenarios where an arrest logged to a specific city may reasonably be attributed to multiple participating agencies.

### 6.4 Payment data

The single largest limitation in the report. There is no federal disclosure system for 287(g) reimbursement requests or confirmation of distributed payments. Each of the recorded figures in this report comes from verified media reports (including interviews with participating agency officials), public records releases, and/or other official evidence or trusted media documentation. The absence of a payment record carries no evidentiary weight. Coverage is geographically biased toward jurisdictions with active newsrooms and independent reporting, as well as states with government disclosure requirements. Do not aggregate to a national total, and do not use for cross-state comparison without noting the inherent limitations in record availability.

### 6.5 Population matching

"Not Found" values in the `Population` field are heavily concentrated among constable offices and similar sub-county jurisdictions, typically listed by ICE at the municipal government level (`Type` field). Population-weighted analyses should exclude, rather than impute, these records.

### 6.6 Upstream data quality

ICE has historically over-counted agreements by including the header row in its own sums. Typographic and data entry errors are routine. Any figure attributed to ICE directly, including ICE's own published totals, should be independently verified. Labeling issues are also common, including several county sheriffs' offices listed as 'Municipality'.

<hr> 

## 7. Versioning, corrections, and reuse

Every figure is an as-of figure tied to a snapshot date, which is displayed on the primary report page. Corrections to individual records are logged in the `Notes` field of the primary agreement dataset.

Methodology version: **v1.4** — Last revised **October 24, 2026**. 

The dataset is published under the [MIT License](LICENSE). Attribution is requested. Researchers needing the processed dataset, an archived snapshot, or clarification on a specific record may contact us.
