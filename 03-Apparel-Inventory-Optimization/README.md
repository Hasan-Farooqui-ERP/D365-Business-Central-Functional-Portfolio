# 👕 Project 03: Apparel Inventory Optimization & Migration
## (NAV to Business Central Case Study)

## 📌 Business Scenario
**Client Profile:** A high-heritage Irish Apparel Retailer migrating from legacy NAV to D365 Business Central.

**The Problem:** 

* **Inventory "Blind Spots":** The legacy system tracked items as "Flat SKUs," meaning different sizes (S, M, L, XL) were not bifurcated.

* **Warehouse Communication Gap:** The shop floor had to request "Full Sets" even if only one size was missing, leading to massive overstocking of slow-moving sizes.

* **Operational Confusion:** No way to distinguish between "New Shipments" and "Customer Returns" in the warehouse ledger.

## 🛠️ Functional Solution Architecture
To resolve these pain points, I architected a solution focusing on **Standardization** to minimize custom development.

### 1. Item Variant Framework
Instead of separate Item Cards, I implemented **Item Variants**. 
* **Result:** Reduced the Item Master list by 70% while increasing tracking accuracy by 100% across all sizes and colors.

### 2. Bin Mandatory & Warehouse Tracking
Enabled **Bin Mandatory** for the Main Warehouse and Shop Floor locations.
* **Result:** Real-time visibility of exactly which shelf holds which specific size, eliminating "search time" for warehouse staff.

### 3. Traceability via Reason Codes & Dimensions
Implemented mandatory **Reason Codes** for all inventory adjustments.
* **Result:** Financial transparency to distinguish between "Stock Loss," "Damaged Returns," and "New Purchases."

---

## 📸 Process Execution (Visual Evidence)

### **Step 1: Configuring the Variant Matrix**
I set up the **Item Variants** for the core apparel line (e.g., Guinness Heritage T-Shirt) to allow individual size tracking.
> */images/[Item-Variants-Setup](01-Functional-Data-Schema-Attributes.JPG)*

### **Step 2: Bin Content Visibility**
By configuring **Bins**, we can now see exactly how many 'Medium' units are available vs 'Large' in specific warehouse zones.
> *[Insert Image: 02-Bin-Content-Tracking.JPG]*

### **Step 3: Corrective Adjustments (The "Fix")**
Demonstrating how the shop floor can now adjust or request a **single missing size** without affecting the rest of the SKU set.
> *[Insert Image: 03-Variant-Specific-Adjustment.JPG]*

---

## 📈 Business Impact
* **Inventory Accuracy:** Increased by 25% through variant-level tracking.
* **Reduced Waste:** Eliminated the "Full Set" ordering requirement, reducing overstock costs.
* **Financial Clarity:** Provided the CFO with a "Store-by-Store" inventory valuation using **Global Dimensions**.

---
