# Source Data

## Arrest data

Source: **[Deportation Data Project](https://deportationdata.org/data/processed/ice.html)**
 
ICE administrative "arrest with detention" records obtained under FOIA and processed by the [Deportation Data Project](https://deportationdata.org/data/processed/ice.html). The release used covers arrests leading to ICE detention from **October 1, 2022 to August 6, 2026**. This report uses arrests from **January 1, 2025 to August 6, 2026**. The data is used only in the arrest analysis section and is **not** joined to the agreement data record by record. For DDP's processing, see its [ICE core data codebook](https://deportationdata.org/docs/ice/codebook.html).

> [!NOTE]
> For more information on how the **Deportation Data Project** data is processed and analyzed for this report, please see [our methodology](docs/METHODOLOGY/methodology.md).

<hr>

## Payment data 

Source: Compiled from published journalism, state award listings, agency budget and auditor records, and leaked documents. *Not* a systematic collection. 

Currently recorded in two places:
 
- the `Confirmed TFM Reimbursements + Invoices` column of the active agreements file, with its source listed in `Notes`;
- a separate state grants table.


> [!NOTE]
> For more information on how state grant and federal reimbursement/invoice data is wrangled, processed, and analyzed for this report, please see [our methodology](docs/METHODOLOGY/methodology.md).
  

> [!NOTE]
> Migration to a single payments table, separate from the active agreement data and with improved tracking and record source details, is in progress.


<hr>


## Reference data
 
- **Location:** agency address from the agency's official website where available (or ICE MOA or Google Maps), written as "Address, City, ST ZIP" where a full address was found. Some records carry only a county or state.
- **Population:** U.S. Census Bureau [American Community Survey (ACS) 2024](https://www.census.gov/programs-surveys/acs) estimates, matched to the agency's jurisdiction: municipality, county, or state. State agencies are assigned the statewide population.
- **Agency totals by state:** the [2018 Census of State and Local Law Enforcement Agencies](https://bjs.ojp.gov/data-collection/census-state-and-local-law-enforcement-agencies-csllea), Bureau of Justice Statistics. Used for each state's participation rate. Agencies created after 2018 are not in that count.
