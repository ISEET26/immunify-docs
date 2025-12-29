# Vaccine Supply and Stock Management (VSSM)

## Overview
The Vaccine Supply and Stock Management (VSSM) module helps users record and track vaccine and immunization supply movements across stores and service delivery points, including:

- Receipts (incoming stock)
- Issues/dispatches (outgoing stock)
- Transfers between stores
- Adjustments (corrections, wastage, expiry)
- Stock balance and stock card history

> Tip: Always verify the **store**, **product**, **batch/lot**, and **expiry date** before saving any transaction.

---

## Who should use this module
Typical users include:
- Health Facility Storekeeper / Vaccinator (facility stock)
- District / Governorate Storekeeper (subnational stock)
- National EPI store users (central stock)

---

## Required data (before you start)
Make sure the following are available:
- You are assigned to the correct **administrative level** and **store**
- Vaccine / supply items exist in the **product catalog**
- Batch/Lot and expiry information is available (from packaging or shipping documents)

---

## Navigation
From the main menu, go to:

**VSSM → Stock Transactions**  
or  
**VSSM → Stock Balance / Stock Card**

![VSSM menu](../assets/images/vssm/vssm-menu.png)

---

## Main workflows

### 1) Record a vaccine receipt (Receive stock)
Use this when vaccines/supplies arrive from a higher-level store, supplier, or partner.

#### Steps
1. Go to **VSSM → Receive**
2. Select:
   - **Receiving Store** (your store)
   - **Source** (supplier / upstream store)
   - **Receipt Date**
   - **Document Reference** (invoice / waybill / delivery note)
3. Add item lines:
   - **Product**
   - **Batch/Lot**
   - **Expiry Date**
   - **Quantity Received**
   - (Optional) **VVM status / notes** if applicable
4. Review totals and click **Save**

![Receipt form](../assets/images/vssm/vssm-receipt-form.png)
![Receipt items](../assets/images/vssm/vssm-receipt-items.png)

#### Validation rules
- **Batch/Lot** is required for vaccines (and for supplies if configured)
- **Expiry Date** must be valid and not in the past
- Quantity must be a positive number
- The receiving store must match your assigned store/level

#### Common errors
- Wrong store selected (facility vs district store)
- Typo in batch/expiry (causes reporting issues later)
- Receiving the same document twice (duplicate receipt)

---

### 2) Issue vaccines (Dispatch / Issue stock)
Use this when you send stock to another store or issue stock for service delivery (depending on setup).

#### Steps
1. Go to **VSSM → Issue**
2. Select:
   - **Issuing Store** (your store)
   - **Destination** (downstream store / facility)
   - **Issue Date**
   - **Document Reference**
3. Add item lines:
   - **Product**
   - **Batch/Lot** (select from available batches)
   - **Quantity Issued**
4. Click **Save**

![Issue form](../assets/images/vssm/vssm-issue-form.png)
![Issue items](../assets/images/vssm/vssm-issue-items.png)

#### Validation rules
- System will not allow issuing **more than available balance** (unless configured otherwise)
- Batch must exist in your stock balance
- Quantity must be a positive number

#### Good practice
- Use FEFO: **First Expire, First Out** (issue the earliest expiry first)
- Record the correct document number for audit trail

---

### 3) Transfer stock between stores (Internal transfer)
Use this when stock moves between two stores under the same administrative authority (as per your setup).

#### Steps
1. Go to **VSSM → Transfer**
2. Select:
   - **From Store**
   - **To Store**
   - **Transfer Date**
   - **Reference**
3. Add item lines (product, batch, qty)
4. Click **Save**

![Transfer screen](../assets/images/vssm/vssm-transfer.png)

> Note: Depending on configuration, a transfer might require confirmation by the receiving store.

---

### 4) Record a stock adjustment (Wastage, expiry, correction)
Use adjustments only when needed, such as:
- Expired doses removed
- Breakage, VVM discard, cold chain incident loss
- Inventory reconciliation corrections

#### Steps
1. Go to **VSSM → Adjustment**
2. Select:
   - **Store**
   - **Adjustment Date**
   - **Reason** (e.g., Expiry, Breakage, Temperature Excursion, Inventory Correction)
3. Add item lines:
   - Product, batch, expiry
   - Quantity adjusted (as per form design)
4. Add notes (recommended)
5. Click **Save**

![Adjustment form](../assets/images/vssm/vssm-adjustment-form.png)

#### Validation rules
- Reason is mandatory
- Quantities must align with available stock (depending on configuration)

#### Good practice
- Always provide clear notes for adjustments (audit requirement)
- Attach supporting evidence if your SOP requires it (paper form, incident report)

---

## Stock balance and stock card

### View stock balance (current availability)
1. Go to **VSSM → Stock Balance**
2. Filter by:
   - Store
   - Product category (optional)
   - Product (optional)
3. Review balances by product and batch

![Stock balance](../assets/images/vssm/vssm-stock-balance.png)

What you can typically see:
- On-hand quantity
- Batch/Lot
- Expiry date
- Status flags (near expiry, expired)

---

### View stock card (transaction history)
1. Go to **VSSM → Stock Card**
2. Select:
   - Store
   - Product
   - (Optional) Batch
3. Review all transactions affecting the item

![Stock card](../assets/images/vssm/vssm-stock-card.png)

Use stock card to:
- Verify receipt and issue history
- Investigate discrepancies
- Support audits and reporting

---

## Recommended routine (daily / weekly)
- **Daily**: record receipts and issues immediately (same day)
- **Weekly**: review stock balance and near-expiry items
- **Monthly**: reconcile physical stock vs system and record adjustments if required

---

## Troubleshooting (quick)
**I cannot see a product in the list**
- The item may not be enabled for your store level, or it’s missing in the catalog. Contact your Admin.

**I cannot issue stock**
- You may not have enough balance for the selected batch, or you selected the wrong store.

**Batch not selectable**
- Batch may not exist in your store balance. Check if it was received correctly.

---

## Related pages
- [User Roles & Access](../user-roles.md)
- [Reports](reports.md)

