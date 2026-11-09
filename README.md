# SolarPay: Pay-As-You-Go Solar Energy Management System

## Project Information

| Detail | Information |
|---|---|
| **Student Name** | Sugira Armel Davy |
| **Student ID** | 20251SEN076 |
| **Course** | INSY 8311: Oracle PL/SQL |
| **Academic Year** | 2026-2027 |
| **Semester** | Semester I |
| **Project Domain** | Energy and Utilities |
| **Database** | Oracle Database |
| **Repository** | `davy_20251SEN076_SolarPay` |

## 1. Project Overview

SolarPay is a database-driven Pay-As-You-Go (PAYG) solar energy management system designed to help off-grid solar energy providers manage customers, solar installations, prepaid energy accounts, payments, electricity consumption, and maintenance activities.

The system will allow customers to purchase prepaid energy credits and monitor their electricity usage. Solar providers will be able to manage installations, track payments, monitor battery performance, and identify installations that require maintenance.

The project will use Oracle Database and PL/SQL to implement its core business rules, automate transactions, and maintain accurate records.

## 2. Problem Statement

Off-grid solar energy providers face challenges managing prepaid customer accounts, monitoring electricity consumption, tracking payments, and identifying solar installations that require maintenance.

Without a centralized management system, providers may experience inaccurate credit balances, inefficient payment tracking, limited visibility into energy consumption, and delayed maintenance interventions.

**How can off-grid solar energy providers efficiently manage prepaid customer accounts, monitor electricity consumption, control energy credit transactions, and identify installations requiring maintenance?**

## 3. Project Objectives

### Main Objective

To develop a database-driven solar energy management system that automates prepaid energy transactions, monitors electricity consumption, and supports the management of solar installations and maintenance activities.

### Specific Objectives

1. Develop a centralized database for managing customers and solar installations.
2. Implement prepaid energy accounts and automate credit purchases and deductions.
3. Monitor electricity consumption and maintain transaction histories.
4. Track battery readings and identify installations requiring maintenance.
5. Generate operational reports to support decision-making by solar energy providers.

## 4. Proposed Solution

SolarPay will provide a centralized platform with four main functional areas:

- **Customer and Installation Management:** Register customers and manage their solar installations and components.
- **Prepaid Energy Management:** Process payments, recharge accounts, and track available energy credits.
- **Energy Consumption Monitoring:** Record electricity consumption and automatically deduct the corresponding credits.
- **Battery and Maintenance Management:** Monitor battery readings, track battery health, and manage maintenance requests.

When an account runs out of available credits, the system will update the installation's power status. Physical disconnection and reconnection will be represented through simulated power-controller events within the academic implementation.

## 5. Data Source

The project intends to use real-world off-grid solar energy consumption data from the Oxford University Research Archive.

**Proposed dataset:** [Off-grid solar energy consumption dataset](https://ora.ox.ac.uk/objects/uuid:3d8abe24-aebb-4b64-9771-01287089dcae)

The dataset will provide real-world electricity consumption records for analysis and testing. Customer profiles, payment transactions, prepaid accounts, and other operational records may be supplemented with clearly identified synthetic data where necessary.

*Dataset download, record count, and licence will be verified and documented before final submission.*

## 6. Planned Database Tables

The initial database design will include the following tables:

| Table | Purpose |
|---|---|
| CUSTOMERS | Stores customer information. |
| INSTALLATIONS | Stores registered solar installations. |
| SOLAR_COMPONENTS | Stores solar equipment and component information. |
| PREPAID_ACCOUNTS | Manages customer prepaid energy balances. |
| PAYMENTS | Records customer payments. |
| CREDIT_TRANSACTIONS | Tracks credit purchases, deductions, and adjustments. |
| CONSUMPTION_RECORDS | Stores electricity consumption readings. |
| POWER_EVENTS | Records simulated power disconnection and reconnection events. |
| BATTERY_READINGS | Stores battery monitoring data. |
| MAINTENANCE_REQUESTS | Tracks maintenance issues and their status. |
| TECHNICIANS | Stores technician information. |
| NOTIFICATIONS | Stores system-generated alerts and notifications. |

The final database structure will be refined during the data modeling and normalization phase.

## 7. Planned PL/SQL Features

The project will demonstrate the following Oracle PL/SQL features:

- **Stored Procedures:** Process payments, recharge prepaid accounts, and manage maintenance requests.
- **Functions:** Calculate available energy credits and evaluate battery health.
- **Cursors:** Generate customer consumption summaries and operational reports.
- **Packages:** Organize prepaid account and payment management operations.
- **Triggers:** Automatically deduct credits after consumption, enforce account restrictions, and maintain audit records.
- **Exception Handling:** Handle invalid payments, insufficient credits, and other transaction errors.
- **Audit Logging:** Record changes to important financial and account information.
- **DBMS_SCHEDULER:** Automate low-credit alerts and overdue maintenance checks.

## 8. Innovation

### Oracle APEX Operations Dashboard

SolarPay will include an interactive operations dashboard developed using **Oracle APEX**, connected to the actual Oracle Database.

The dashboard will provide:

- Total registered customers.
- Active and disconnected solar installations.
- Total prepaid payment revenue.
- Daily electricity consumption.
- Customers with low prepaid balances.
- Battery health indicators.
- Pending and overdue maintenance requests.
- Customer payment and transaction histories.

Authorized users will also be able to perform operations such as recharging prepaid accounts and reviewing customer records through the dashboard.

All core business rules and transaction processing will remain implemented in Oracle PL/SQL. The dashboard will provide an interactive interface for accessing the database functionality.

## 9. Expected Results

The expected outcome is a functional solar energy management database system capable of:

1. Managing customers and solar installations.
2. Processing prepaid payments and energy credit transactions.
3. Automatically updating prepaid balances based on electricity consumption.
4. Monitoring battery performance and maintenance activities.
5. Producing useful operational reports.
6. Providing an interactive Oracle APEX dashboard connected to the database.

## 10. References

Research references, dataset documentation, technical documentation, and existing system comparisons will be maintained in [`docs/research/research_log.md`](docs/research/research_log.md).

**Planned technical reference:**

- Oracle. Oracle Database Documentation. https://docs.oracle.com/en/database/

Additional academic papers, industry reports, and dataset references will be added after verification.