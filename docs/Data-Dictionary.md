# Data Dictionary

## Active Agreements List
| Field / Column | Description | Format / Values | Source |
|---|---|---|---|
| `STATE` | State or territory | Uppercase full name | ICE |
| `LAW ENFORCEMENT AGENCY` | Agency name, corrected where verifiably wrong | Text | ICE (corrected) |
| `Location` | Agency address | "City, ST ZIP" where found | Agency website, Google Maps, or published MOA |
| `TYPE` | Level of government | County, Municipality, State | ICE (corrected) |
| `COUNTY` | County containing the agency's jurisdiction, with state suffix added for county agencies (required for Data Studio visual mapping) | Text; empty if unmatched | ICE with manual corrections + modifications|
| `County Name` | `COUNTY` without the state suffix, for county map joins | Text; empty if unmatched | Derived |
| `SUPPORT TYPE` | Program model | Task Force Model, Warrant Service Officer, Jail Enforcement Model | ICE |
| `SIGNED` | Date of ICE counter-signature | Date | ICE, corrected to MOA where flagged |
| `Jurisdiction Population (2024 Census Est.)` | Jurisdiction population | Integer; 'Not Found' if not matched | [Census ACS 2024](https://www.census.gov/programs-surveys/acs/data.html) |
| `MuniName` | Municipality name used to match Census places | Text; municipalities only | Derived |
| `MOA URL` | Link to the signed MOA on ice.gov | URL; where reviewed | ICE |
| `LEA Signed Date` | Date the agency official signed the MOA | Date; where reviewed | MOA |
| `LEA Signer Name` | Agency official who signed | Text; where reviewed | MOA |
| `LEA Signer Position` | That official's title | Text | MOA |
| `LEA Point of Contact (POC)` | Contact named in the MOA | Text | MOA |
| `LEA POC Position` | That contact's title | Text | MOA |
| `Confirmed TFM Reimbursements + Invoices` | Documented Task Force payments | USD; lower bound | Records, reporting |
| `Notes` | Corrections and payment sourcing | Text | Manual |
| `# of Active Agreements for Agency` | Active agreements held by the agency | 1–3, computed | Derived |
| `Slug Helper` | Working identifier | Text | Derived |

<hr>
 
## Canceled Agreements List
Shares `STATE`, `LAW ENFORCEMENT AGENCY`, `Location`, `TYPE`, `COUNTY`, `SUPPORT TYPE` and `SIGNED` with **Active Agreements List**, plus:
 
| Field Column | Description | Format / Values |
|---|---|---|
| `REMOVED DATE` | First ICE edition without the agreement | Date |
| `CANCEL REASON` | Reason for agreement removal | enum (7 values) |
| `NOTES` | Context: related agreements, which edition | Text |
