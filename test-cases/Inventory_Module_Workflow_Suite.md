# Test Suite: Inventory Request, Approval, and Return Workflows

## Module Overview
Validates supply requisition, approval/denial routing, return tracking, and role permission enforcement between Hospital Custodian and Inventory Personnel.

| Test Case ID | Feature / Description | User Role | Preconditions | Steps to Execute | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-INV-001** | Submit stock request for medical supplies | Custodian | Valid item in catalog | 1. Select item 'Syringe 10ml'.<br>2. Set Qty: 50.<br>3. Click 'Submit Request'. | Request status updates to 'Pending Approval'. | Request logged as 'Pending Approval'. | **PASS** |
| **TC-INV-002** | Approve inventory request as Inventory Manager | Inventory Personnel | Pending request exists | 1. Open Inventory Requests.<br>2. Click 'Approve'. | Status updates to 'Approved'; stock quantity decrements. | Status updates and stock updates correctly. | **PASS** |
| **TC-INV-003** | Verify conflicting toast notification on Denial flow | Inventory Personnel | Pending request exists | 1. Open Pending Request.<br>2. Click 'Deny Request'. | Single notification toast appears: "Request Denied Successfully". | System displays conflicting double toasts: "Request Denied" AND "Approved Successfully". | **FAIL** |
| **TC-INV-004** | Pagination table boundary test on Item Masterlist | Custodian | >50 items in list | 1. Scroll to bottom of list.<br>2. Click 'Next Page' (Page 2). | Page 2 items load cleanly with updated row count. | Page number changes to 2 but table items remain frozen on Page 1. | **FAIL** |
