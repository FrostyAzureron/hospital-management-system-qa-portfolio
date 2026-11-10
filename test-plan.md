# Master Test Plan: Hospital Information System (HIS)

## 1. Scope of Testing
The primary objective of this regression cycle is to verify the core operational modules of the Hospital Information System across all primary user roles prior to production staging.

### In-Scope Modules
1. **Outpatient Department (OPD):** Patient queue, consultation records, doctor assignment.
2. **Nursing Module:** Vitals entry, medication administration records, ward transfer requests.
3. **Inventory & Materials:** Item requests, stock approval, item denial/return flows, minimum stock alerts.
4. **Billing & Cashier:** Disbursement options, invoice rendering, PDF receipt generation.
5. **Access Control (ACL):** Role-based access permission enforcement across 7 user types.

---

## 2. Role-Based Access Control (RBAC) Test Matrix

| System Module | Super Admin | Doctor | Nurse | Admin | Cashier | Inventory Personnel | Hospital Custodian |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Patient Registration** | Full | View | Full | Full | View | No Access | No Access |
| **Vitals & Triage Entry** | Full | View | Full | No Access | No Access | No Access | No Access |
| **Prescription & Consultation** | Full | Full | View | No Access | No Access | No Access | No Access |
| **Inventory Request / Return** | Full | View | View | Full | No Access | Full | Full |
| **Billing / Payment Processing**| Full | No Access | No Access | View | Full | No Access | No Access |
| **Fixed Assets Management** | Full | No Access | No Access | Full | No Access | View | Full |

---

## 3. Defect Lifecycle Strategy
1. **Discovery:** Tester executes test case, records actual result, and captures POT (Proof-Of-Testing screenshot/jam.dev video).
2. **Logging:** Defect logged with Severity (Critical, Major, Minor), System Module, Steps to Replicate, Expected Result, and Actual Result.
3. **Developer Hand-Off & Retest:** Once marked fixed by development, tester re-runs exact execution steps and updates status to `FIXED`, `CLOSED`, or `REOPENED`.
