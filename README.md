# ☕ Monday Café Sales Dashboard

## 📘 Project Overview
The **Monday Café Sales Dashboard** analyzes weekly performance (Monday → Sunday) for a **UAE-based café chain** operating across **four branches**.  
It provides actionable insights into **Sales**, **Profit**, and **Quantity Sold**, dynamically comparing **current vs previous weeks**.  

Built using **Power BI + DAX**, the dashboard automatically displays the **most recent completed week (Oct 20–26, 2025)** and updates interactively when users select other week ranges.

---

## KPI Summary (Oct 20–26, 2025)

| KPI | Current Week | % vs Previous Week | Trend |
|------|---------------|--------------------|--------|
| 💰 **Total Sales** | ₹5.87K | 🔻 -6.5% | ↓ |
| 📈 **Total Profit** | ₹718.87 | 🔻 -4.3% | ↓ |
| 🛒 **Total Quantity Sold** | 404 | 🔻 -10.6% | ↓ |

---

## Insights

### 🏙️ Branch-Wise Sales Contribution
| Branch | % of Total Sales |
|---------|------------------|
| **Dubai** | 42.29% |
| **Abu Dhabi** | 28.55% |
| **Sharjah** | 22.13% |
| **Ajman** | 7.02% |

**Observation:** Dubai leads in total sales, while Ajman needs targeted marketing or promotional campaigns.

---

###  Product-Wise Performance

#### By Quantity Sold
1️⃣ **Cappuccino — 56**  
2️⃣ **Latte — 41**

#### By Sales Value
1️⃣ **Chicken Sandwich — ₹832**  
2️⃣ **Cappuccino — ₹785**

**Observation:** Hot beverages dominate sales volume, while sandwiches contribute more to revenue value.

---

## Visuals in Dashboard

- **KPI Cards** — Weekly totals & % change vs previous week  
- **Line Chart** — Weekly Sales Trend  
- **Pie Chart** — Branch-wise Sales Distribution  
- **Bar Chart 1** — Product-wise Quantity Sold  
- **Bar Chart 2** — Product-wise Sales Contribution  
- **Slicer** — Monday–Sunday Week Range for filtering  

---

## Technical Details

**Tools Used:**  
- Power BI  
- Power Query  
- DAX  

**Logic Implemented:**
1. Created a **Calendar Table** with `WeekStart` and `WeekEnd` (Monday–Sunday logic).  
2. Used **DAX measures** to calculate week-over-week performance.  
3. Added **conditional formatting** to highlight KPI trends in green (↑) or red (↓).  

**Example DAX Formula (Profit % Change):**
```DAX
Profit % Change =
VAR CurrentProfit = [Total Profit]
VAR PrevProfit =
    CALCULATE([Total Profit], DATEADD(Calendar[Date], -7, DAY))
RETURN
DIVIDE(CurrentProfit - PrevProfit, PrevProfit, 0) * 100


Key Takeaways

Sales declined slightly this week (-6.5%)

Profit margins remain stable (~12–15%)

Strongest categories: Coffee and Sandwiches

Focus area: Ajman branch for performance improvement

Learning Outcomes

Week-over-week analysis using DAX time intelligence

KPI conditional formatting with color indicators

Data storytelling and visual alignment in Power BI

Implemented Monday–Sunday weekly logic for slicer filtering

Created by: Sandip Shrestha

Completed on: October 2025
Built with: Power BI, Power Query, DAX
