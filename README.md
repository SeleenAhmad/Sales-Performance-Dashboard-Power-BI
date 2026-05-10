# Sales-Performance-Dashboard-Power-BI
A fully interactive sales analytics dashboard built in Power BI Desktop, featuring regional performance analysis, channel breakdowns, product insights, and KPI tracking across a 12-month period.
# 📊 Sales Performance Dashboard — Power BI

A fully interactive sales analytics dashboard built in Power BI Desktop, featuring regional performance analysis, channel breakdowns, product insights, and KPI tracking across a 12-month period.

---


## 📁 Project Structure

```
sales-dashboard-powerbi/
│
├── sales dashboard.pbix                  # Power BI report file
├── Dashboard_Dataset.xlsx      # Source data (3 sheets, 500 rows)
├── CleanDashboard_Theme.json   # Custom Power BI theme
├── PowerBI_Banner.png          # Dashboard header banner
└── README.md
```

---

## 📋 Dataset Overview

The dataset was purpose-built for this project and contains realistic sales data across the Middle East region.

| Sheet | Rows | Description |
|---|---|---|
| `Sales_Data` | 500 | Transaction-level data with date, region, product, channel, revenue |
| `Monthly_Summary` | 12 | Aggregated monthly KPIs |
| `Product_Performance` | 30 | Per-product units, revenue, rating, return rate |

**Key fields:** Date · Region · Country · Category · Product · Channel · Customer Segment · Salesperson · Units Sold · Revenue · Net Revenue · Discount · Rating

**Regions covered:** Riyadh · Jeddah · Dammam · Amman · Cairo · Dubai · Beirut · Kuwait City

---

## 📊 Dashboard Pages

### Page 1 — Overview
- KPI cards: Total Revenue, Net Revenue, Units Sold, Avg Rating
- Area chart: Monthly Revenue vs Net Revenue trend
- Donut chart: Units Sold by Channel
- Horizontal bar chart: Revenue by Region
- Custom header banner

### Page 2 — Details *(in progress)*
- Product performance breakdown
- Salesperson analysis
- Category comparison

---

## 🎨 Theme & Design

A custom JSON theme was built for this project — **"Clean Professional: Teal & Coral"**

| Role | Color | Hex |
|---|---|---|
| Primary accent | Teal | `#2A9D8F` |
| Secondary accent | Coral | `#E76F51` |
| Base/navy | Dark slate | `#264653` |
| Background | Soft gray | `#F0F2F5` |
| Card background | White | `#FFFFFF` |

To apply the theme in Power BI:
```
View → Themes → Browse for themes → select CleanDashboard_Theme.json
```

---

## 🔧 Features

- ✅ Custom JSON theme imported into Power BI
- ✅ Interactive slicers: Quarter/Month · Category · Channel · Region
- ✅ Slicers synced across pages
- ✅ KPI cards with targets and goal tracking
- ✅ Gauge visual with rating goal (5.00 target)
- ✅ Map visual with bubble size = Revenue
- ✅ Month sorting fixed via Power Query custom column
- ✅ Dual-axis area chart for Revenue vs Net Revenue
- ✅ Custom banner image with embedded KPI preview

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Power BI Desktop | Report building & visualization |
| Power Query (M) | Data transformation & month sorting |
| DAX | KPI measures & calculated columns |
| Excel (.xlsx) | Source data |
| JSON | Custom theme file |
| Python (openpyxl) | Dataset generation |

---

## 🚀 How to Use

1. Clone or download this repository
2. Open `sales dashboard.pbix` in **Power BI Desktop** (free download at [powerbi.microsoft.com](https://powerbi.microsoft.com))
3. If the data source path breaks, go to **Home → Transform data → Data source settings** and repoint to `Dashboard_Dataset.xlsx`
4. The theme is already embedded — no need to reimport

---

## 📈 DAX Measures Used

```dax
-- Month sort column (created in Power Query)
Month_Number = if [Month] = "Jan" then 1
else if [Month] = "Feb" then 2
...
else 12

-- KPI Targets
Target_Revenue = 1800000
Target_Units = 25000
Target_Rating = 5.0
```

---

## 👩‍💻 Author

**Seleen Eshtayah**  
Physics BSc · Data Analytics · Power BI  
[LinkedIn](https://linkedin.com/in/seleen-eshtayah) · [GitHub](https://github.com/SeleenAhmad)

---

## 📄 License

This project is open for portfolio and educational use.
