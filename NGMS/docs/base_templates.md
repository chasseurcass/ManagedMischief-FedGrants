---
# Base Templates

### 1. MainCode = grant + document type

Examples:

* `RSAT_APP`  → RSAT application
* `RSAT_MFR`  → RSAT monthly financial report
* `RSAT_QFR`  → RSAT quarterly financial report (or progress, depending on naming)
* `RSAT_PR`   → RSAT progress report
* `RSAT_CLOSE` → RSAT closeout

This part is exactly how you described it.

### 2. SubCode = **award year** (tied to federal award number)

For example:

* Federal award 2022-RS-BX-0001 → award year 2022
* Federal award 2023-RS-BX-0004 → award year 2023
* Federal award 2024-RS-BX-0011 → award year 2024

You’d set SubCode based on that year, so you can filter.

Concrete examples:

| Purpose          | MainCode | SubCode | Meaning                                     |
| ---------------- | -------- | ------- | ------------------------------------------- |
| RSAT application | RSAT_APP | 2022    | RSAT application tied to 2022 federal award |
| RSAT MFR         | RSAT_MFR | 2022    | RSAT MFRs for 2022 federal award funds      |
| RSAT QFR         | RSAT_QFR | 2022    | RSAT QFRs for 2022 federal award funds      |
| RSAT application | RSAT_APP | 2023    | RSAT application tied to 2023 federal award |
| RSAT MFR         | RSAT_MFR | 2023    | RSAT MFRs for 2023 federal award funds      |
| RSAT QFR         | RSAT_QFR | 2023    | RSAT QFRs for 2023 federal award funds      |

In that setup:

* If you want “all RSAT documents for the 2023 award,” you filter on:

  * MainCode LIKE `RSAT_%`
  * SubCode = `2023`

* If you want “all RSAT MFRs for the 2024 award,” you filter on:

  * MainCode = `RSAT_MFR`
  * SubCode = `2024`
---
