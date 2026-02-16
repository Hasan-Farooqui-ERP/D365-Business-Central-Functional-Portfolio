# Case Study: Complex Procure-to-Pay (P2P) Lifecycle & Financial Reconciliation
**Platform:** Microsoft Dynamics 365 Business Central
**Vendor:** Galway Supplies (V00030)

## 📌 Business Scenario
This project demonstrates a non-linear procurement cycle involving inventory receipt, partial financial settlement, exception handling (damaged goods return), and complex sub-ledger reconciliation to achieve a zero-balance audit trail.

---

## 📊 Process Flow (Mermaid.js)

```mermaid
graph TD
    A[<b>GRN</b><br/>Posted Receipt: 10 Units] --> B[<b>Purchase Invoice</b><br/>€6,332.50 Posted]
    B --> C[<b>Partial Payment</b><br/>€2,000.00 Applied]
    C --> D[<b>Purchase Return</b><br/>2 Damaged Units]
    D --> E[<b>Credit Memo 109001</b><br/>€1,266.50 Posted]
    E --> F[<b>Manual Application</b><br/>Set Applies-to ID: ADMIN2]
    F --> G[<b>Final Settlement</b><br/>€3,066.00 Payment]
    G --> H{<b>Net Balance: €0.00</b>}
    style H fill:#2ecc71,stroke:#27ae60,stroke-width:4px,color:#fff
```

---

## 🛠️ Step-by-Step Execution & Troubleshooting


### Step 0: Goods Receipt Note (GRN)
![GRN](00_Posted_Purchase_Receipt_GRN.JPG)
* **Functional Insight:** Documented the physical receipt of 10 ATHENS Desks.
* ***Troubleshooting:** Resolved location-based posting errors to update inventory.*

### Step 1: Posted Purchase Invoice
![Invoice](01_Posted_Purchase_Invoice.jpg)
* **Functional Insight:** Posted Invoice 108212 for €6,332.50.

### Step 2: Partial Payment Application
![Partial Payment](02_Partial_Payment_Applied.jpg)
* **Functional Insight:** Recorded a €2,000 partial payment.

### Step 3: Purchase Return (Credit Memo)
![Credit Memo](03_Posted_Credit_Memo_Return.jpg)
* **Functional Insight:** Processed a return for 2 damaged units.

### Step 4: Sub-Ledger Manual Reconciliation
![Manual Application](04_Manual_Ledger_Application.jpg)
* **Functional Insight:** Linked Credit Memo to Invoice using 'Applies-to ID'.

### Step 5: Detailed Vendor Ledger (Audit Trail)
![Detailed Ledger](05_Detailed_Vendor_Ledger_Entries.JPG)
* **Functional Insight:** Full history of ledger movements.

### Step 6: Final Settlement & Verification
![Final Balance](06_Final_Vendor_Balance_Zero.jpg)
* **Functional Insight:** Verified the final Vendor Card balance as 0.00.

---
**Author:** Hasan Farooqui
