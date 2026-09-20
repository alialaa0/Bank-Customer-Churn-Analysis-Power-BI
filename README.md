# 🏦 Bank Customer Churn Analysis — Power BI 

An interactive **Power BI Executive Dashboard** built to analyze customer churn, customer segments, and financial impact across different regions.

The project covers the complete workflow from **Excel data preparation and cleaning** to **data modeling, DAX analysis, dashboard design, and interactive filtering**.

---

## 📊 Dashboard Preview

### Executive Dashboard

<p align="center">
  <img src="assets/Screenshot%202026-09-20%20032829.png" alt="Executive Dashboard" width="100%">
</p>

### Interactive Filter Panel

<p align="center">
  <img src="assets/Screenshot%202026-09-20%20032846.png" alt="Interactive Filter Panel" width="100%">
</p>

---

## 🎯 Business Objective

The goal is to provide an executive-level view of **customer churn and its financial impact**, with analysis across:

- 🌍 Geography
- 👥 Gender
- 🎂 Age Groups
- 💳 Credit Score
- 👤 Active Membership
- 💰 Customer Balance
- 🚪 Customer Exit / Churn

---

## 🔄 Project Workflow

```text
Excel Source Files
        ↓
Data Cleaning & Transformation
        ↓
Data Quality Validation
        ↓
Data Integration & Modeling
        ↓
DAX Measures & Calculated Columns
        ↓
Dashboard UI Design
        ↓
Power BI Implementation
        ↓
Interactive Executive Dashboard
```

---

## 📁 Data Sources

The analysis started with two Excel files:

- `Account_Info`
- `Customer_Info`

The tables were connected using:

```text
CustomerID
```

A **1-to-1 relationship** was established between the two datasets, and the integrated data was used as the main analytical table:

```text
All_Data
```

---

## 🧹 Data Cleaning & Preparation

Several data-quality issues were identified and resolved during the transformation stage.

### Currency & Data Types

Converted text-based financial fields into numeric values:

- `EstimatedSalary`
- `Balance`

Both fields contained **Euro (€) symbols and text formatting** that prevented direct numerical analysis.

### Geography Standardization

Inconsistent geography values were standardized:

```text
FRA     → France
French  → France
France  → France
```

### Duplicate Records

| Dataset | Duplicate Rows |
|---|---:|
| `Account_Info` | 2 |
| `Customer_Info` | 1 |

### Missing & Invalid Values

- **3 invalid negative values** were identified in `EstimatedSalary` after numeric conversion and replaced with the **mean**.
- Unknown age values were replaced with the **median age**.

These transformations ensured consistent data types and cleaner analytical categories.

---

## 🧩 Data Modeling

The cleaned datasets were integrated through `CustomerID`:

```text
Account_Info ───── 1 : 1 ───── Customer_Info
                     │
                     ↓
                  All_Data
```

The resulting `All_Data` table was used for the Power BI analysis and visualization layer.

---

## 🧮 DAX Analysis

The dashboard uses DAX measures for the main business KPIs:

- Total Customers
- Total Balance
- Churned Customers
- Churned Balance
- Churn Rate
- % of Churned Balance
- Average Credit Score

### Calculated Columns

Two analytical categories were created:

**Age Group**

```text
< 30
31 - 40
41 - 50
51 - 60
+65
```

**Credit Score Category**

Credit scores were grouped into categories using conditional logic with `SWITCH`.

---

## ⚡ Interactive Dashboard Features

### Dynamic Filter Panel

The dashboard uses buttons and bookmarks to create a clean filter experience.

```text
Filter Icon
     ↓
Display Slicers
     ↓
Apply Filters
     ↓
Close Filter Panel
```

Available filters include:

- IsActiveMember
- Geography
- Gender
- Age Group
- Exited

### Dynamic Title

`SELECTEDVALUE()` and variables were used to dynamically update the dashboard title according to the selected geography.

Example:

```text
Executive Dashboard & Overview Churn - All Regions
```

The title can dynamically reflect the selected region.

---

## 📈 Key Dashboard KPIs

| KPI | Value |
|---|---:|
| Total Customers | **10K** |
| Churned Customers | **2K** |
| Churned Balance | **185.59M** |
| Churn Rate | **20.37%** |

---

## 📊 Main Visualizations

The dashboard provides a visual breakdown of churn across:

- **Churn Rate by Geography**
- **Churn Rate by Age Group**
- **Churn Rate by Gender**
- **Churn Rate by Number of Products**
- Customer and balance KPIs
- Interactive demographic filtering

### Churn Rate by Geography

| Geography | Churn Rate |
|---|---:|
| Germany | **32.44%** |
| Spain | **16.67%** |
| France | **16.15%** |

---

## 🎨 Dashboard Design

The dashboard interface was designed before being implemented in Power BI.

Design elements include:

- Dark executive-style theme
- Gradient header
- Rounded KPI cards
- High-contrast KPI values
- Custom visual containers
- Icons
- Shadow effects
- Interactive filter panel
- Consistent visual hierarchy

The layout was initially designed using **PowerPoint** and then recreated in **Power BI**.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Source data |
| **Power Query** | Data cleaning & transformation |
| **Power BI** | Modeling & visualization |
| **DAX** | Measures & calculated columns |
| **PowerPoint** | Dashboard UI design |

---

## 📂 Project Structure

```text
Bank-Customer-Churn-Analysis-Power-BI/
│
├── assets/
│   ├── Screenshot 2026-09-20 032829.png
│   └── Screenshot 2026-09-20 032846.png
│
├── data/
│   ├── Account_Info.xlsx
│   └── Customer_Info.xlsx
│
├── Bank Customer Churn Analysis.pbix
│
└── README.md
```

---

## 🚀 Skills Demonstrated

```text
Excel
  ↓
Power Query
  ↓
Data Cleaning
  ↓
Data Modeling
  ↓
DAX
  ↓
KPI Development
  ↓
Dashboard UI/UX
  ↓
Interactive Power BI Reporting
```

**End-to-end Power BI project focused on customer churn analysis, data quality, business KPIs, and executive dashboard design.**
