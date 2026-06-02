# 📊 Power BI Data Model: Superstore Analytics

This repository contains the documentation for the data model and DAX formulas implemented in the **Global Superstore** Power BI project. The model has been optimized for clean organization and advanced time intelligence reporting.

---

## 🏗️ What I Have Done

### 1. Created a Centralized Measures Table (`_All Measures`)
* Built a dedicated, empty table exclusively to house DAX formulas.
* Hid the default blank column to transform it into a native measures folder. This groups all KPIs neatly at the very top of the fields pane with a calculator icon for easy navigation.

### 2. Built a Dynamic Calendar Table
* Generated a master date dimension using DAX to support seamless time intelligence.
* Established a **1-to-Many ($1:Point$) relationship** from the `Calendar[Date]` column to **both** date fields in the `Orders` fact table.

#### 🔗 Dual-Relationship Structure (Role-Playing Dimension):
* **Active Relationship:** `Calendar[Date]` $\rightarrow$ `Orders[Order Date]` (Drives all standard visuals and daily trend reports).
* **Inactive Relationship:** `Calendar[Date]` $\rightarrow$ `Orders[Ship Date]` (Used specifically to track shipping and fulfillment metrics).

### 3. Added a New Calculated Column
* Created a custom physical column directly within the `Orders` table .

---
