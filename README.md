# Fund Administration Data Governance Framework
### A portfolio project simulating the Data Governance operating model of a global fund administrator / asset servicer

## Why this project exists

This project was built to demonstrate hands-on capability against the requirements of a **Senior Associate, Data Governance** role at a fund administration / asset servicing business (custody, fund accounting, NAV, transfer agency, securities lending, FX). It simulates the data governance operating model such a business would run, end to end:

| JD Requirement | Where it's addressed |
|---|---|
| Rollout & maintenance of a DG framework | [`docs/01_governance_charter.md`](docs/01_governance_charter.md) |
| Data management policies & procedures | [`docs/01_governance_charter.md`](docs/01_governance_charter.md) §5 |
| Data Catalogue & Data Taxonomy | [`data_catalogue/`](data_catalogue/) — OpenMetadata ingestion config + cataloged fund admin datasets |
| Identification & monitoring of Critical Data Elements (CDEs) | [`cde_register/CDE_Register.csv`](cde_register/CDE_Register.csv) |
| Metadata management & data quality assessments | [`data_quality/`](data_quality/) |
| Track & remediate data issues | [`issue_log/Data_Issue_Remediation_Log.csv`](issue_log/Data_Issue_Remediation_Log.csv) |
| Data maturity assessments & reporting | [`maturity_assessment/Data_Maturity_Assessment.md`](maturity_assessment/Data_Maturity_Assessment.md) |
| Data ownership records / RACI | [`raci/RACI_Matrix.csv`](raci/RACI_Matrix.csv) |
| DG training & awareness materials | [`training/DG_Awareness_OnePager.md`](training/DG_Awareness_OnePager.md) |
| Data scorecards for management/committees | [`data_quality/DQ_Scorecard.csv`](data_quality/DQ_Scorecard.csv) |
| DAMA-DMBOK alignment | [`docs/02_dama_dmbok_mapping.md`](docs/02_dama_dmbok_mapping.md) |

## Why fund administration as the domain

Fund administrators sit between asset managers and investors and are accountable for the accuracy of the **Net Asset Value (NAV)** — the single most consequential Critical Data Element in the business. A DG program here has to cover:

- **Fund accounting data** — NAV components, pricing, corporate actions
- **Investor data** — subscriptions, redemptions, AUM, KYC/AML status
- **Trade & settlement data** — trade capture, matching, custody positions
- **FX & treasury data** — rates used in NAV calculation and reporting

This project builds a governance program around exactly these four domains, rather than a generic/abstract dataset, so the artefacts map directly onto what a fund administrator's data governance function actually owns.

## Tooling choice: OpenMetadata over a Purview-only stack

The existing profile's DG tooling experience is Microsoft Purview. To close the "dedicated DG platform (Collibra/Alation-class)" gap, this project uses **OpenMetadata** — an open-source data catalogue/governance platform in the same category as Collibra and Alation (metadata management, data quality, glossary/taxonomy, lineage, ownership tagging). The ingestion config and catalogued asset definitions in `data_catalogue/` are written against OpenMetadata's actual YAML ingestion framework, not a mock — so the config is transferable to a real Collibra/Alation onboarding (same underlying DG platform concepts: glossary, business terms, data quality tests, ownership).

## Repo structure

```
mufg-data-governance-framework/
├── README.md
├── docs/
│   ├── 01_governance_charter.md          # DG framework, policies, roles
│   └── 02_dama_dmbok_mapping.md          # Maps this project to all 11 DAMA-DMBOK knowledge areas
├── data_catalogue/
│   ├── openmetadata_ingestion_config.yaml
│   └── sample_metadata/                  # Table/glossary definitions for 4 fund admin domains
├── cde_register/
│   └── CDE_Register.csv                  # 20 CDEs with owner, tier, quality rule, monitoring frequency
├── raci/
│   └── RACI_Matrix.csv                   # Data ownership across 9 DG activities x 7 stakeholder groups
├── data_quality/
│   ├── dq_rules.yaml                     # Executable-style DQ rules (completeness/validity/timeliness/accuracy)
│   └── DQ_Scorecard.csv                  # Monthly scorecard output, committee-ready
├── maturity_assessment/
│   └── Data_Maturity_Assessment.md       # DCAM-aligned maturity scoring, current vs target state
├── training/
│   └── DG_Awareness_OnePager.md          # New-joiner / business-user DG awareness material
└── issue_log/
    └── Data_Issue_Remediation_Log.csv    # Issue tracking with SLA, severity, root cause, remediation
```

## Note on CDMP

This project demonstrates practical, applied competency across the DAMA-DMBOK knowledge areas (see `docs/02_dama_dmbok_mapping.md`) but is **not a substitute for the CDMP certification itself**. The certification exam is being scheduled separately.
