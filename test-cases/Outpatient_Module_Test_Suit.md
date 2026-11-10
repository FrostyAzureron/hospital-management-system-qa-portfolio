# Test Suite: Outpatient Department & Nurse Role Integration

## Module Overview
Validates patient filtering, consultation view rendering, search/reset functionality, and permission boundaries for the Nurse and Doctor roles in the Outpatient module.

| Test Case ID | Feature / Description | User Role | Preconditions | Steps to Execute | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-OPD-001** | Verify Nurse role visibility for Outpatient queue | Nurse | Active Nurse login session | 1. Navigate to Left Sidebar.<br>2. Select 'Outpatient Module'. | Outpatient queue table loads with assigned patients for the current shift. | Table renders successfully with shift patients. | **PASS** |
| **TC-OPD-002** | Verify table filter reset button behavior | Nurse | OPD table filtered by date range | 1. Apply date filter.<br>2. Click 'Reset Filter' button. | Date filter clears and table returns to default unfiltered view. | Reset button does not clear filters; table remains filtered. | **FAIL** |
| **TC-OPD-003** | Verify PDF summary generation for patient record | Doctor | Patient consultation complete | 1. Open patient summary.<br>2. Click 'Export PDF'. | System downloads clean single-page PDF record with header details. | System outputs blank 500 server error screen upon click. | **FAIL** |
| **TC-OPD-004** | Verify navigation back button on Edit Consultation view | Doctor | Doctor editing consultation note | 1. Open record.<br>2. Click 'Edit'.<br>3. Click top-left 'Back' button. | User returns to previous patient consultation list without losing state. | Back button missing; user trapped on edit screen. | **FAIL** |
