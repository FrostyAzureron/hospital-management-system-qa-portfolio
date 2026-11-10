# Sanitized Defect Log — HIS Regression Cycle

| Bug ID | Module | Severity | Summary / Headline | Steps to Replicate | Expected Result | Actual Result | Retest Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **DEF-014** | Billing / Cashier | **Critical** | PDF Invoice generation fails with server error | 1. Log in as Cashier.<br>2. Open settled invoice.<br>3. Click 'Print Receipt PDF'. | PDF document generates and opens print dialog. | Blank screen rendered with console exception 500. | **FIXED** |
| **DEF-022** | Access Control (ACL) | **High** | Nurse role granted unauthorized write access to Doctor consultation notes | 1. Log in as Nurse.<br>2. Open Patient Record.<br>3. Locate consultation notes block. | Notes are read-only for Nurse role. | 'Edit Notes' button active and changes save to DB. | **FIXED** |
| **DEF-029** | Outpatient / UI | **Medium** | Conflicting success and error notifications on patient status update | 1. Open OPD Queue.<br>2. Update patient status to 'Completed'. | Single banner: "Status updated". | Green banner "Updated" and Red banner "Failed to save" display simultaneously. | **FIXED** |
| **DEF-031** | Inventory | **Medium** | Search & Reset buttons fail to reset filtered list state | 1. Filter inventory by Category = 'PPE'.<br>2. Click 'Reset Filters'. | Search inputs clear and list updates to show all items. | Inputs clear visually but filtered result set stays active. | **RETEST READY** |
| **DEF-032** | General UI | **Low** | Missing back navigation button on View/Edit details screen | 1. Navigate to Fixed Assets.<br>2. View Item Details. | Visible top-bar 'Back' button returns to asset list. | 'Back' button missing; user forced to re-click sidebar menu. | **FIXED** |
