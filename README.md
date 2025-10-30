# monday-cafe-sales-dashboard
📋 Project Overview

The Monday Café Dashboard analyzes weekly performance (Monday → Sunday) for a UAE-based café chain operating 4 branches.
It provides actionable insights on Sales, Profit, and Quantity, dynamically comparing current vs. previous weeks.

📊 Built using Power BI + DAX, this dashboard automatically displays the last completed week (Oct 20–26, 2025) and updates when users select other week ranges.

🎯 KPI Summary (Oct 20–26, 2025)
KPI	Current Week	% vs Previous Week	Trend
💰 Total Sales	₹5.87K	🔻 -6.5%	↓
📈 Total Profit	₹718.87	🔻 -4.3%	↓
🛒 Total Quantity Sold	404	🔻 -10.6%	↓
☕ Insights
🏬 Branch-Wise Sales Contribution
Branch	% of Total Sales
Dubai	42.29%
Abu Dhabi	28.55%
Sharjah	22.13%
Ajman	7.02%

Observation: Dubai leads in total sales; Ajman needs marketing or promotions.

Product-Wise Performance

By Quantity Sold
1️⃣Cappuccino — 56
2️⃣ Latte — 41

By Sales Value
1️⃣ Chicken Sandwich — ₹832
2️⃣ Cappuccino — ₹785

 Observation: Hot beverages dominate volume, while sandwiches drive high-value sales.

Visuals in Dashboard

KPI Cards — Weekly totals & % change vs previous week

Line Chart — Weekly Sales Trend

Bar Chart 1 — Product-wise Quantity Sold

Bar Chart 2 — Product-wise Sales Contribution

Pie Chart — Branch-wise Sales Distribution

Slicer — Monday–Sunday Week Range

⚙️ Technical Details

Tools Used: Power BI, Power Query, DAX
Logic:

Created a Calendar Table with WeekStart and WeekEnd (Mon–Sun)

Used DAX to compare current week vs previous week

Added conditional formatting for color-coded KPI trends

Example DAX for Profit % Change:

Profit % Change =
VAR CurrentProfit = [Total Profit]
VAR PrevProfit =
    CALCULATE([Total Profit], DATEADD(Calendar[Date], -7, DAY))
RETURN
DIVIDE(CurrentProfit - PrevProfit, PrevProfit, 0) * 100

🎨 Design Theme

Used a café-inspired palette:
☕ Coffee Brown #4A3F35
✨ Caramel Gold #C58940
🥛 Latte Beige #F1DEC9
🍦 Cream White #F9F5F0
🌰 Dark Mocha #6A4021

💡 Key Takeaways

Sales declined slightly this week (-6.5%)

Profit margins stable at ~12–15%

Strongest product categories: Coffee & Sandwiches

Focus improvement on Ajman branch for better reach

🧠 Learning Outcomes

Week-over-week comparison using DAX


Conditional formatting for KPI visuals

Data storytelling through Power BI
