# DAMA-DMBOK2 Knowledge Area Mapping

This project is structured to demonstrate applied competency across all 11 DAMA-DMBOK2 knowledge areas, using the fund administration domain as the working context.

| Knowledge Area | How this project addresses it |
|---|---|
| **Data Governance** | `docs/01_governance_charter.md` — committee structure, policies, escalation path |
| **Data Architecture** | `data_catalogue/sample_metadata/` — logical structure of NAV, investor, trade, and FX domains and how they relate |
| **Data Modeling & Design** | Table/entity definitions in `data_catalogue/sample_metadata/*.yaml` (attributes, keys, relationships per domain) |
| **Data Storage & Operations** | Referenced in `docs/01_governance_charter.md` §2 scope — systems of record per domain |
| **Data Security** | Ownership/access tagging in catalogue metadata; investor PII (KYC/AML fields) flagged as restricted in `cde_register/CDE_Register.csv` |
| **Data Integration & Interoperability** | Lineage fields in `data_catalogue/openmetadata_ingestion_config.yaml` — tracks flow from trade capture → NAV calculation → investor statements |
| **Document & Content Management** | `docs/`, `training/` — policy and awareness documentation structure |
| **Reference & Master Data** | Fund, investor, and instrument reference data identified as Tier 1/2 CDEs in `cde_register/CDE_Register.csv` |
| **Data Warehousing & Business Intelligence** | `data_quality/DQ_Scorecard.csv` — committee-ready reporting output |
| **Metadata Management** | Core focus of `data_catalogue/` — business glossary, technical metadata, lineage |
| **Data Quality** | `data_quality/dq_rules.yaml` — completeness, validity, accuracy, timeliness rules per CDE, with thresholds |

## Note

This mapping is intended to show working familiarity with the DAMA-DMBOK2 body of knowledge as applied to a real operating context — it is a project artefact, not a claim of certification. The CDMP exam itself tests recall and case-study application of the full body of knowledge and is being pursued separately.
