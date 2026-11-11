# SolarPay Research Log

**Project:** SolarPay: Pay-As-You-Go Solar Energy Management System  
**Student:** Sugira Armel Davy  
**Student ID:** 20251SEN076  
**Course:** INSY 8311: Oracle PL/SQL  
**Phase:** 0  
**Last updated:** 9 November 2026

## 1. Research purpose

This research investigates the operational context of pay-as-you-go (PAYGo) solar home systems, the use of consumption and payment data, existing PAYGo management platforms, Rwanda's electricity-access context, and the Oracle technologies planned for SolarPay.

The sources below are grouped according to the Phase 0 requirements. Key findings summarize the cited material. The project gaps are observations about how each source informs the proposed SolarPay scope.

## 2. Research sources

### Source 1: Research paper

**APA reference**

Mergulhão, V. P., Capra, L., Voglitsis, K., & Parikh, P. (2023). How do they pay as they go?: Learning payment patterns from solar home system users data in Rwanda and Kenya. *Energy for Sustainable Development, 76*, Article 101295. https://doi.org/10.1016/j.esd.2023.101295

**Type:** Peer-reviewed research article  
**Link:** https://discovery.ucl.ac.uk/id/eprint/10175341/

**Key finding:** The study analyses payment records from more than 32,000 Rwandan and 25,000 Kenyan solar home system users. It identifies six payment-behaviour groups in Rwanda and four in Kenya. The authors report that payment behaviour varies across customers and that a one-size-fits-all approach can create inefficiencies.

**Relevance to SolarPay:** This supports maintaining detailed payment histories and designing reports that help providers understand different customer payment patterns. It also supports keeping payments and prepaid-credit transactions as distinct, traceable records.

**Gap / opportunity:** The paper focuses on analysing payment behaviour and customer segmentation. SolarPay's planned academic prototype will focus on operational database processes such as account recharges, credit deductions, transaction validation, consumption records, and maintenance tracking. The paper does not provide a complete database implementation for those operations.

---

### Source 2: Research paper

**APA reference**

Perriment, R., Mergulhão, V., Kumtepeli, V., Parikh, P., McCulloch, M. D., & Howey, D. A. (2026). Understanding long-term energy use in off-grid solar home systems in sub-Saharan Africa. *Energy for Sustainable Development, 90*, Article 101896. https://doi.org/10.1016/j.esd.2025.101896

**Type:** Peer-reviewed research article  
**Link:** https://discovery.ucl.ac.uk/id/eprint/10218733/

**Key finding:** The study analyses hourly load-demand data from 1,000 solar home systems across sub-Saharan Africa. It identifies five typical daily load profiles. The study reports that 77% of households reduced average daily electricity consumption beyond the first year, with average demand falling by approximately one-third by the end of the second year compared with peak demand.

**Relevance to SolarPay:** This demonstrates why energy-consumption history is useful. SolarPay can store consumption readings and provide summaries over time rather than treating energy use as a single static value.

**Gap / opportunity:** The paper studies consumption patterns and their evolution. It does not provide the complete customer-account, payment-processing, installation-maintenance, and operational dashboard workflow planned for SolarPay.

---

### Source 3: Report and Rwanda statistics

**APA reference**

National Institute of Statistics of Rwanda. (2025). *EICV7: Poverty profile report 2023/24*. https://statistics.gov.rw/data-sources/surveys/EICV/integrated-household-living-conditions-survey-7-eicv-7/eicv7-poverty-profile-report-202324

**Type:** National statistical report  
**Link:** https://statistics.gov.rw/data-sources/surveys/EICV/integrated-household-living-conditions-survey-7-eicv-7/eicv7-poverty-profile-report-202324

**Key finding:** The report states that in 2024, 72% of Rwandan households had access to electricity: 50% through the national grid and 22% through solar panels, mainly standalone solar systems. It also reports that electricity is mainly used for lighting and charging mobile phones.

**Relevance to SolarPay:** The figures establish the relevance of solar electricity in Rwanda and provide national context for a system focused on managing standalone solar installations.

**Gap / opportunity:** The report provides household-level national statistics. It is not an operational dataset of individual solar installations, prepaid accounts, payments, consumption transactions, or maintenance records. It supports the problem context but cannot directly populate all SolarPay tables.

---

### Source 4: Existing PAYGo management system

**APA reference**

d.light. (n.d.). *Atlas: A comprehensive software platform for your PayGo business*. https://www.dlight.com/atlas

**Type:** Existing commercial system  
**Link:** https://www.dlight.com/atlas

**Key finding:** d.light describes Atlas as a software platform supporting PAYGo operations. Its published functionality includes customer registration, inventory management, payment processing, service and repair, marketing materials, and field-team management. d.light also states that Atlas handles more than four million transactions monthly in Kenya.

**Relevance to SolarPay:** Atlas demonstrates that PAYGo providers need integrated customer, payment, inventory, and after-sales service workflows. It is a useful reference for identifying practical features and the scope of an existing commercial solution.

**Gap / opportunity:** Atlas is an established commercial platform. Public product information does not expose its internal database schema or PL/SQL implementation. SolarPay is an academic Oracle database project that will demonstrate its own relational design, PL/SQL business rules, audit records, and an Oracle APEX dashboard. SolarPay should not claim to be the first platform to combine PAYGo customer and payment management.

---

### Source 5: Real dataset

**APA reference**

Perriment, R., Mergulhão, V., Kumtepeli, V., Parikh, P., McCulloch, M., & Howey, D. (2025). *Data repository for “Understanding long-term energy use in off-grid solar home systems in sub-Saharan Africa”* (Version 1.0). University of Oxford. https://doi.org/10.5287/ora-6r4vapx6b

**Type:** Research dataset  
**Link:** https://ora.ox.ac.uk/objects/uuid:3d8abe24-aebb-4b64-9771-01287089dcae

**Key finding / contents:** The repository documents hourly load-demand time series from 1,000 off-grid solar home systems in sub-Saharan Africa. Each column represents a household, with hourly electricity-consumption values in watt-hours recorded over 391 to 1,232 days. The repository lists a CSV file named `final_anon_hourly.csv` with a displayed size of approximately 283.5 MB.

**Licence:** The repository identifies the dataset licence as Creative Commons Attribution-NonCommercial (CC BY-NC). The project must retain attribution and must not use the dataset commercially. The licence file supplied with the download should be retained and checked before redistribution.

**Relevance to SolarPay:** The dataset provides real consumption observations that can be profiled, sampled, transformed, and used to test consumption-related database workflows.

**Limitations / gap:** The documented dataset contains hourly load-demand time series. It does not, based on the repository description, provide all the operational entities required by SolarPay, such as named customer profiles, prepaid account balances, individual payment transactions, solar component inventories, technician assignments, or maintenance requests. Any additional records created for those entities must be clearly labelled as synthetic sample data and must not be presented as real customer records.

**Verification still required before final submission:** Download the CSV and inspect it to record the exact row/column count, missing values, date coverage, and sample records. The repository's 1,000-system description is not a substitute for documenting the actual imported file structure.

---

### Source 6: Technical documentation

**APA reference**

Oracle. (2019). *Coding PL/SQL subprograms and packages*. Oracle Database 19c Documentation. https://docs.oracle.com/en/database/oracle/oracle-database/19/adfns/coding-subprograms-and-packages.html

**Type:** Official technical documentation  
**Link:** https://docs.oracle.com/en/database/oracle/oracle-database/19/adfns/coding-subprograms-and-packages.html

**Key finding:** Oracle documents PL/SQL procedures and functions as reusable named program units. It describes packages as schema objects that group related program elements, including procedures, functions, cursors, and exceptions. Oracle also explains that enabled triggers execute automatically when their triggering database events occur.

**Relevance to SolarPay:** This documentation supports the planned use of procedures for payment and recharge operations, functions for calculations, packages for related account operations, and triggers for automatic validation and audit-related actions.

**Gap / opportunity:** The documentation explains Oracle implementation features, not the business requirements of a PAYGo solar provider. SolarPay must define and test its own business rules, constraints, and transaction workflows.

## 3. Additional technical source

Oracle. (2019). *Administering Oracle Scheduler*. Oracle Database 19c Documentation. https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/administering-oracle-scheduler.html

**Type:** Official technical documentation  
**Key finding:** Oracle Scheduler can be used to configure, run, monitor, and manage scheduled database jobs. This is relevant to the planned automated checks for low prepaid balances and overdue maintenance requests.

## 4. Research synthesis and identified opportunity

The research indicates that PAYGo solar operations involve more than recording customer payments. Customer payment patterns differ, energy consumption changes over time, and existing commercial systems combine customer registration, payments, inventory, and after-sales service.

The Oxford dataset provides a substantial real source of hourly electricity-consumption observations. However, it does not appear to contain all the operational records required to implement a complete PAYGo management database. SolarPay will therefore use the real dataset for consumption-related analysis and testing, while any additional customer, account, payment, component, technician, and maintenance records created for demonstration will be identified as synthetic.

The proposed project opportunity is to build an academic Oracle-based implementation that brings together customer and installation records, prepaid-account transactions, consumption tracking, battery readings, maintenance workflows, and operational reporting. PL/SQL will implement the core business rules, while Oracle APEX will provide an interactive dashboard connected to the database.

The project is not claiming that these capabilities are unprecedented in the commercial market. The intended contribution is the implementation and demonstration of these integrated workflows using Oracle Database, PL/SQL, and Oracle APEX within the scope of the capstone assignment.

## 5. Source verification checklist

- [x] Two research papers identified.
- [x] National report/statistics source identified.
- [x] Existing PAYGo system identified.
- [x] Real dataset identified and repository licence checked.
- [x] Official Oracle technical documentation identified.
- [ ] Download the dataset and inspect its actual structure and record count.
- [ ] Retain the dataset's original licence and readme files with the downloaded data.
- [ ] Add a screenshot of the dataset sample to the Phase 0 evidence.
- [ ] Confirm the lecturer has accepted/registered the SolarPay topic.
