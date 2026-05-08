# Statement of Work
## Acme Corp: Enterprise Data Warehouse Modernization

**Version:** 1.2 (Executed)
**Date:** June 10, 2025
**Client:** Acme Corp
**Firm:** [YOUR FIRM NAME]
**Engagement Lead:** [Engagement Lead Name]

---

## 1. Project Overview

Acme Corp ("Client") has engaged [YOUR FIRM NAME] ("Firm") to modernize its enterprise data warehouse environment. The current environment consists of a legacy on-premise SQL Server 2016 data warehouse serving 14 internal reporting consumers across Finance, Operations, and Merchandising. The Firm will design, build, and deploy a replacement environment on Snowflake (AWS us-east-1), including data migration from the legacy system, a rebuilt reporting layer, and end-user enablement.

---

## 2. Scope of Work

### 2.1 In Scope

The Firm will deliver a fully functional data warehouse on Snowflake that replicates and improves upon the current environment, including:

- **Data Migration:** Migration of all historical data from SQL Server to Snowflake, covering the Orders, Inventory, Finance, and Customer domains (approximately 3.2TB of structured data)
- **Data Modeling:** Design and implementation of a dimensional data model (star schema) optimized for analytical workloads
- **ETL/ELT Pipelines:** Build and deploy 18 data pipelines using dbt on Fivetran to load source data from the Client's ERP (SAP Business One) and POS systems
- **Reporting Layer:** Rebuild 12 existing Tableau dashboards on the new Snowflake data layer
- **Data Quality:** Implement data quality checks and alerting for all 18 pipelines
- **Documentation:** Provide data dictionary, pipeline documentation, and runbook for ongoing operations
- **Training:** Deliver four 2-hour training sessions: two for power users (Tableau authors) and two for the IT operations team

### 2.2 Out of Scope

The following are explicitly excluded from this Statement of Work:

- Migration of any data domains not listed in Section 2.1
- Development of net-new dashboards or reports not currently in production
- Integration with systems other than SAP Business One and POS
- Ongoing managed services or support post-go-live (see Section 9 for hypercare terms)
- Snowflake licensing or Fivetran licensing (Client to procure directly)

---

## 3. Deliverables

| # | Deliverable | Description | Target Date |
|---|---|---|---|
| D1 | Architecture Design Document | Snowflake environment design, data model, and pipeline architecture | Aug 1, 2025 |
| D2 | Data Migration Plan | Migration sequence, validation approach, and rollback plan | Aug 15, 2025 |
| D3 | ETL/ELT Pipelines (18) | All data pipelines deployed and validated in staging | Oct 15, 2025 |
| D4 | Dimensional Data Model | Deployed to Snowflake production environment | Oct 31, 2025 |
| D5 | Rebuilt Tableau Dashboards (12) | All 12 dashboards rebuilt and validated against legacy output | Nov 28, 2025 |
| D6 | Training Sessions (4) | Completed with attendance records and materials | Dec 5, 2025 |
| D7 | Documentation Package | Data dictionary, runbook, and pipeline docs | Dec 10, 2025 |
| D8 | Go-Live Sign-Off | Client sign-off on production environment | Dec 12, 2025 |

---

## 4. Assumptions

The following assumptions are the basis of this SOW. Changes to these assumptions may result in a change request.

1. Client will provide access to all source systems (SAP Business One API, POS export) by **July 15, 2025**.
2. Client will provide at least two Subject Matter Experts (SMEs) from Finance and Operations, available a minimum of 4 hours per week throughout the project.
3. Snowflake and Fivetran licenses will be provisioned by the Client no later than **July 1, 2025**.
4. The 12 Tableau dashboards to be rebuilt are the versions currently in production as of June 1, 2025. Any changes to dashboard requirements post-SOW execution are out of scope.
5. Source data is of sufficient quality to migrate without major cleansing (a data profiling report will be delivered in Week 2; material quality issues will trigger a change request).
6. Client IT will provide VPN access and necessary firewall rules within 5 business days of project kickoff.

---

## 5. Client Responsibilities

- Assign a dedicated Client Project Manager as the primary point of contact
- Provide timely access to source systems, data, and SME time per Section 4
- Review and provide written approval of deliverables within 5 business days of submission
- Ensure availability of Client IT resources for environment setup and security reviews

---

## 6. Project Timeline

| Phase | Dates | Key Milestone |
|---|---|---|
| Initiate & Discover | Jul 7 – Jul 31, 2025 | Architecture doc approved |
| Design & Plan | Aug 1 – Aug 29, 2025 | Data migration plan approved |
| Build (Sprints 1-4) | Sep 1 - Oct 31, 2025 | All pipelines deployed to staging |
| Build (Sprints 5-8) | Nov 1 - Nov 28, 2025 | Dashboards rebuilt and validated |
| UAT & Enablement | Dec 1 – Dec 10, 2025 | Training complete; go-live approved |
| Go-Live | Dec 12, 2025 | Production cutover |

---

## 7. Pricing

This engagement is priced on a **fixed-fee basis**. The total fee is:

**$485,000**

Payment schedule:
| Milestone | Amount | Due |
|---|---|---|
| Contract execution | $97,000 (20%) | Jul 7, 2025 |
| Architecture doc approved (D1) | $72,750 (15%) | Aug 1, 2025 |
| All pipelines deployed (D3) | $121,250 (25%) | Oct 15, 2025 |
| Dashboards validated (D5) | $121,250 (25%) | Nov 28, 2025 |
| Go-live sign-off (D8) | $72,750 (15%) | Dec 12, 2025 |

Expenses (travel, lodging) are billed at cost, not to exceed $12,000 without prior written approval.

---

## 8. Change Control

Scope changes requested by either party will be managed through a formal change request process. Each change request will document the scope change, estimated effort, timeline impact, and cost impact. Change requests require written approval from the Client Project Sponsor and the Firm Engagement Lead before work begins.

---

## 9. Hypercare

Following go-live, the Firm will provide 30 days of hypercare support (up to 20 hours total), included in the contract price. Hypercare covers bug fixes and questions related to delivered work. New feature requests or enhancements are out of scope and subject to a separate agreement.

---

## 10. Signatures

By signing below, both parties agree to the terms of this Statement of Work.

| Party | Name | Title | Signature | Date |
|---|---|---|---|---|
| Acme Corp | _________________ | _________________ | _________________ | _________________ |
| [YOUR FIRM NAME] | _________________ | _________________ | _________________ | _________________ |
