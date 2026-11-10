# Enterprise Hospital Information System (HIS) — QA & Testing Suite

## Project Overview
This repository contains sanitized quality assurance artifacts modeled after real-world, enterprise-scale Hospital Information System (HIS) regression testing cycles. It demonstrates end-to-end QA execution, team leadership workflows, role-based security validation, defect tracking lifecycles, and test metrics reporting.

> **Note on Data Privacy:** All business rules, workflows, and test cases in this repository are fully sanitized and anonymized implementations of generic healthcare software modules (Admission, Outpatient, Doctor, Nurse, Billing, Fixed Assets, and Inventory). No confidential or proprietary client data is included.

---

## 🛠️ Key Technical & Testing Competencies
- **Testing Types:** System Regression Testing, Role-Based Access Control (RBAC) Testing, Functional Testing, Integration Testing, Retesting & Verification.
- **Tools & Ecosystem:** Manual Test Execution Tracking (Spreadsheet Suites), jam.dev / Birdeatsbug (Proof-of-Testing capture), GitHub Issues / Defect Log Tracking.
- **QA Leadership:** Test case distribution, daily intern execution tracking, bug triage prioritization, and developer retest coordination across 300+ executable test cases.

---

## 📊 Core QA Execution Summary

| Metric | Value |
| :--- | :--- |
| **Total Test Cases Executed** | 318 |
| **Passed Test Cases** | 286 |
| **Failed Test Cases** | 32 |
| **Overall Pass Rate** | **89.9%** |
| **Roles Tested** | 7 (Super Admin, Doctor, Nurse, Admin, Custodian, Cashier/Billing, Inventory Personnel) |
| **Primary Defect Categories** | Permission/RBAC errors, UI state persistence failure, PDF print bugs, Pagination leaks |

---

## 📂 Repository Structure
- [`test-plan/`](./test-plan/): Master QA strategy and Role-Based Access Control (RBAC) matrix across 7 system roles.
- [`test-cases/`](./test-cases/): Detailed module-level test cases with preconditions, steps, expected results, and execution statuses.
- [`defect-reports/`](./defect-reports/): Sanitized defect log including reproduction steps, severity tagging, proof-of-testing (POT) references, and retest states.
- [`metrics-reporting/`](./metrics-reporting/): End-of-cycle summary reports and metrics breakdown.
