# 01-Order-to-Cash (O2C): Mixed Fulfillment & Business Exceptions

## 📌 Project Overview
This project demonstrates a high-complexity **Order-to-Cash (O2C)** cycle within Microsoft Dynamics 365 Business Central. The scenario goes beyond a standard "Happy Path" to showcase how a Functional Consultant handles real-world business hurdles such as partial payments and sales returns.

### 🏢 Client Scenario: Dublin Office Solutions
* **The Deal:** A sale of 5x ATHENS Desks plus 5 hours of professional 'Office Setup' services.
* **The Complexity:** 1. **Service vs. Product:** Managing inventory items alongside non-stock service hours.
    2. **Partial Payment:** Handling a cash flow scenario where the customer pays £2,000 against a £4,949.38 invoice.
    3. **Sales Return:** Processing a 'Damaged in Transit' return for 1 unit and issuing a Credit Memo.

---

## 🛠 Step-by-Step Execution

### Step 0: Customer Master Data
Created the customer card for **Dublin Office Solutions**, ensuring all Irish VAT and Posting Groups were correctly aligned.
> ![Customer Creation](./images/00-Customer-Creation.png)

### Step 1: Service Item Configuration
Configured a **Service-Type Item** (Office Setup) to track professional labor hours without impacting physical stock.
> ![Service Item](./images/01-Service-Item-Card.png)

### Step 2: Sales Order Release
Converted the quote to a Sales Order and **Released** it, confirming the stock is allocated and the order is ready for the warehouse.
> ![Sales Order](./images/02-Sales-Order-Released.png)

### Step 3: Shipment & Logistics
Posted the **Shipment** for the 5 desks. The system tracks the physical movement of goods separately from the financial invoice.
> ![Shipment](./images/03-Sales-Order-Shipped.png)

### Step 4: Final Invoicing
Generated the **Posted Sales Invoice**. This recognizes the revenue and creates the initial Accounts Receivable entry.
> ![Posted Invoice](./images/04-Posted-Sales-Invoice.png)

### Step 5: Partial Payment Ledger
Recorded a **£2,000 payment**. The ledger shows the payment applied, leaving the remaining balance open for further settlement.
> ![Posted Payment](./images/05-Posted-Payment-Ledger.png)

### Step 6: Sales Return Order
Managed the return of 1 damaged unit. Used the **'Get Posted Document Lines to Reverse'** tool to ensure 100% audit traceability back to the original invoice.
> ![Return Order](./images/06-Sales-Return-Order.png)

### Step 7: Credit Memo Validation
Posted the return to generate a **Sales Credit Memo**, formally reducing the customer's debt.
> ![Credit Memo](./images/07-Posted-Credit-Memo.png)

### Step 8: Final Reconciled Statement
The comprehensive "Single Source of Truth" showing the full lifecycle: Invoice → Partial Payment → Credit Memo → Final Balance.
> ![Final Ledger](./images/08-Final-Ledger-Statement.png)

---

## 💡 Functional Skills Demonstrated
* **Financial Management:** Partial payment application and ledger reconciliation.
* **Logistics Handling:** Sales returns and inventory restocking procedures.
* **Traceability:** Maintaining document links across the O2C lifecycle.
* **Consulting Mindset:** Addressing the mix of physical products and intangible services.
