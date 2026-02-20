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
I architected a **Variant Matrix** for the apparel line. By using **Item Attributes & Categories**, we ensured that a single Item Card (e.g., Guinness Heritage T-Shirt) could manage dozens of size/color combinations without cluttering the Master Data.

### B. Warehouse Precision (Bin Mandatory)
I configured the **Dublin Warehouse (DUB-WH)** as a "Directed" location. By making **Bins Mandatory**, the system now requires staff to record the exact shelf location for every item, ensuring 100% stock visibility.

### C. B2B & Assembly Logic (Kitting)
To handle large orders, I implemented:
* **Special Order Linking:** Links Sales Orders directly to Purchase/Supply orders to "lock" stock for specific clients.
* **Assembly BOMs:** Created "Gift Set" kits that combine physical items with **Labor Resources** (Packing Hours), allowing the client to see the true landed cost of fulfillment.

---

## 4. Implementation Evidence (Visuals)

* **Master Data Setup:** [Item Attributes & Categories](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/11-Item-Attributes.JPG)
* **Inventory Architecture:** [Multi-Dimensional Variant Matrix](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/01-Item-Variants-Setup.JPG)
* **Warehouse Operations:** [Bin Content & Stock Visibility](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/02-Bin-Content-Tracking.JPG)
* **Financial Mapping:** [Inventory Posting Groups & G/L Setup](https://github.com/Hasan-Farooqui-ERP/D365-Business-Central-Functional-Portfolio/blob/main/03-Apparel-Inventory-Optimization/images/04-Inventory-Posting-Setup.JPG)

---

## 5. Project Outcomes
* **100% Visibility:** Eliminated stock "blind spots" by tracking at the Variant and Bin level.
* **Accurate Costing:** Integrated labor and packaging costs into the final product cost via Assembly Orders.
* **Operational Scale:** The system is now ready to support Dublin-wide B2B expansion.
