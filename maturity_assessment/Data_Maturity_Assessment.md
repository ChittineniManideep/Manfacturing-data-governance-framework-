# Data Maturity Assessment — Q2 2026 (simulated baseline)
### Aligned to DCAM (Data Management Capability Assessment Model) component structure

Scoring: 1 = Ad hoc, 2 = Repeatable, 3 = Defined, 4 = Managed, 5 = Optimized

| Capability Area | Current State | Score | Target State (18mo) | Score | Key Gap |
|---|---|---|---|---|---|
| Data Governance & Leadership | Committee formed, charter approved | 3 | Committee driving proactive risk decisions | 4 | Escalation SLAs not yet enforced |
| Data Architecture | Domains mapped, lineage partially automated | 2 | Full automated lineage across all CDEs | 4 | Manual lineage for legacy trade systems |
| Data Quality Management | CDE-level rules defined and running for 4 domains | 3 | Real-time DQ monitoring with automated alerting | 4 | Currently daily-batch, not real-time |
| Metadata Management | Central catalogue live for 4 domains | 3 | 100% of regulator-reportable systems catalogued | 4 | 2 legacy custody feeds not yet onboarded |
| Data Ownership & Stewardship | RACI defined, owners assigned | 3 | Stewards actively closing issues within SLA | 4 | Steward capacity constrained in Trade Ops |
| Issue Management | Issue log operating, severity-tiered | 3 | Root-cause trending reduces repeat issues | 4 | No formal root-cause taxonomy yet |
| Training & Culture | Awareness material published | 2 | DG training embedded in onboarding | 3 | Not yet mandatory for new joiners |

**Overall maturity score: 2.7 / 5 (Repeatable → Defined transition)**

## Narrative summary

The framework has moved from ad hoc to repeatable across most capability areas within two quarters: CDEs are identified, owned, and monitored; a central catalogue is live; and a committee governs escalations. The primary gaps holding maturity back are (1) DQ monitoring is still batch/daily rather than real-time, (2) two legacy custody feeds remain outside the catalogue, and (3) DG training is not yet a mandatory onboarding step. These three items form the basis of the next-quarter roadmap.

## Next-quarter roadmap

1. Onboard remaining 2 legacy custody feeds to the catalogue (closes metadata coverage gap)
2. Move NAV and FX rate DQ checks from daily batch to intraday monitoring
3. Formalize root-cause taxonomy for the issue log to enable trend reporting
4. Make DG awareness training mandatory within first-30-days onboarding
