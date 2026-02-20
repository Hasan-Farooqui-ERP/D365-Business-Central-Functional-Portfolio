# Project 03: Apparel Inventory Architecture & Logistics Optimization

## 1. Project Overview
This project showcases a comprehensive inventory and logistics re-engineering for **Irish Heritage**, a premium apparel retailer based in Dublin. The goal was to transform a basic "flat" inventory list into a high-performance **Dynamics 365 Business Central** environment capable of managing retail variants, warehouse bins, and B2B bulk fulfillment.

---

## 2. Business Challenges & Objectives
The legacy system at Irish Heritage caused several operational "blind spots":

* **Granularity Issues:** Stock was tracked as single SKUs, making it impossible to see availability by **Size, Gender, or Color**.
* **Warehouse Inefficiency:** Lack of Bin logic led to picking errors and "lost" stock in the Dublin Warehouse.
* **Fulfillment Risks:** Large B2B orders (e.g., 500 units for Trinity College) would often accidentally deplete retail store stock.

---

## 3. Technical Solutions (Functional Architecture)

### A. Multi-Dimensional Item Governance
I architected a **Variant Matrix** for the apparel line. By using **Item Attributes & Categories**, we ensured that a single Item Card could manage dozens of size/color combinations without cluttering the Master Data.

### B. Warehouse Precision (Bin Mandatory)
I configured the **Dublin Warehouse (DUB-WH)** as a "Directed" location. By making **Bins Mandatory**, the system now requires staff to record the exact shelf location for every item, ensuring 100% stock visibility.

### C. B2B & Assembly Logic (Kitting)
To handle large orders, I implemented:
* **Special Order Linking:** Links Sales Orders directly to Purchase/Supply orders to "lock" stock for specific clients.
* **Assembly BOMs:** Created "Gift Set" kits that combine physical items with **Labor Resources** (Packing Hours), allowing the client to see the true landed cost of fulfillment.

---

## 4. Implementation Evidence (Visuals)

* **Master Data Setup:** [Functional Data Schema & Attributes](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/01-Functional-Data-Schema-Attributes.JPG)
* **Category Hierarchy:** [Item Category Setup](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/02-Item-Category-Hierarchy-Setup.JPG)
* **Inventory Architecture:** [Multi-Dimensional Variant Matrix](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/04-Multi-Dimensional-Variant-Matrix.JPG)
* **Warehouse Control:** [Greenfield Location & Bin Mandatory Setup](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/05-Greenfield-Location-Setup-Bin-Mandatory.JPG)
* **Financial Mapping:** [Inventory Financial Posting Groups](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/08-Inventory-Financial-Posting-Groups.JPG)
* **Audit Trail:** [Item Ledger Audit Verification](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/10-Item-Ledger-Audit-Trail.JPG)

---

## 5. Project Outcomes
* **100% Visibility:** Eliminated stock "blind spots" by tracking at the Variant and Bin level.
* **Accurate Costing:** Integrated labor and packaging costs into the final product cost via Assembly Orders.
* **Operational Scale:** The system is now ready to support Dublin-wide B2B expansion.
