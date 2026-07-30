# Data Governance Framework Charter
## Fund Administration & Asset Servicing — Data Governance Operating Model

## 1. Purpose

This charter establishes the framework by which data is managed as a strategic asset across fund accounting, investor services, trade/settlement, and treasury functions, in support of regulatory obligations (CBI, SEC, AIFMD reporting), operational accuracy (NAV integrity), and risk management.

## 2. Scope

- **In scope:** Critical Data Elements feeding NAV calculation, investor records, trade/settlement data, custody positions, FX rates used in valuation, and any data reported to regulators or fund boards.
- **Out of scope:** Internal HR/finance systems not touching client fund data (governed under a separate internal data policy).

## 3. Governance structure

| Body | Composition | Responsibility |
|---|---|---|
| Data Governance Committee | Head of Fund Services, Head of Risk & Compliance, Head of Technology, Data Governance Lead | Approves policy, reviews scorecards, escalated issue sign-off |
| Data Governance Function | Data Governance Senior Associate (this role), Data Stewards | Day-to-day framework operation, catalogue maintenance, CDE monitoring, issue triage |
| Data Owners | Business unit heads (Fund Accounting, Investor Services, Trading Ops, Treasury) | Accountable for accuracy and fitness-for-purpose of data in their domain |
| Data Stewards | Nominated SMEs within each business unit | Day-to-day data quality monitoring, first-line issue resolution |

## 4. Guiding principles

1. Every Critical Data Element has one accountable Data Owner (see RACI Matrix).
2. Data quality is measured, not assumed — every CDE has a defined quality rule and monitoring frequency.
3. Lineage and metadata are maintained in the central catalogue, not in spreadsheets or tribal knowledge.
4. Issues are logged, triaged by severity, and tracked to remediation with an SLA.
5. The framework is reported on monthly via the Data Quality Scorecard to the Governance Committee.

## 5. Core policies maintained under this framework

- **Data Ownership Policy** — defines Owner/Steward roles and RACI (see `raci/RACI_Matrix.csv`)
- **Critical Data Element Policy** — defines CDE identification criteria, tiering (Tier 1 = NAV-impacting, Tier 2 = investor-impacting, Tier 3 = operational) and review cadence
- **Data Quality Policy** — defines the four quality dimensions in scope (completeness, validity, accuracy, timeliness), thresholds, and escalation triggers
- **Metadata & Cataloguing Policy** — mandates all CDE-bearing systems are registered in the data catalogue with business glossary terms, technical lineage, and ownership tags
- **Issue Management Policy** — defines severity tiers (Critical/High/Medium/Low), SLAs, and escalation path to the Governance Committee

## 6. Reporting cadence

| Report | Frequency | Audience |
|---|---|---|
| Data Quality Scorecard | Monthly | Data Governance Committee |
| CDE exception report | Weekly | Data Owners / Stewards |
| Data Maturity Assessment | Quarterly | Governance Committee, Board risk sub-committee (annual) |
| Issue remediation status | Bi-weekly | Data Governance Committee |
