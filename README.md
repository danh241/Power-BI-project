# Project Report: Plant Co. Multi-Year Performance Trend Analysis

## 📝 Situation

Plant Co. is a global distributor of botanical products. Following a period of strong growth in 2022, leadership observed a concerning downturn in overall profitability. A preliminary look showed a cumulative Gross Profit decline of **$5.49M** over several years, but the specific timing and drivers of this reversal were unclear. The company needed to move beyond a single snapshot view and diagnose the root causes of this multi-year performance deterioration.

## 🎯 Task

My task was to build a comprehensive Power BI dashboard to analyze performance trends from 2022 to 2024. The goal was to provide a clear, data-driven narrative that answered critical strategic questions:

- How did the business's growth trajectory change over the last three years across Sales, Quantity, and Gross Profit?
- What was the inflection point where performance began to decline?
- What are the underlying drivers of the profit decline? Is it a volume problem, a pricing problem, or a margin problem?
- Which regions are most consistently contributing to the negative trend?

## 🚀 Action

To address this strategic task, I followed a comprehensive data analysis workflow:

#### 1. Data Modeling
Implemented a robust **Star Schema** in Power BI with a central `Fact_Sales` table and multiple dimension tables (`Dim_Accounts`, `Dim_Product`, `Dim_Date`) to ensure optimal performance and scalability.

#### 2. DAX & Data Transformation
- Developed time-intelligence measures (`TOTALYTD`, `SAMEPERIODLASTYEAR`) to enable year-over-year comparisons.
- **Key Feature:** Created a **Dynamic Measures selector** using a disconnected table and the `SWITCH` function. This allows stakeholders to seamlessly toggle the entire dashboard between Sales, Quantity, and Gross Profit views, empowering self-service analysis.

#### 3. Analytical Approach
The core of my approach was to slice the data by year. This allowed me to compare performance not just against the prior year, but to see the evolution of trends across multiple years, which proved crucial for uncovering the root cause.

#### 4. Data Visualization (Storytelling with Data)
The dashboard was designed to tell a clear story over time. The key visualizations—KPI cards, a waterfall chart for monthly variance, a treemap for regional impact, and a scatter plot for customer segmentation—can all be filtered by year to see the story unfold.

## 📊 Result & Recommendations

The multi-year analysis uncovered a clear and alarming narrative that was previously hidden in the aggregated data.

### Insight 1: A Strong 2022 Baseline Was Followed by a Sharp Reversal
The company experienced robust, across-the-board growth in 2022, establishing a strong baseline. However, this momentum reversed sharply in 2023.

### Insight 2: 2023 Was the Critical Inflection Point, Driven by Margin Erosion
The analysis of 2023 revealed the core of the problem. While unit quantity sold increased by **17k**, both Sales (**-512k**) and Gross Profit (**−265k**) declined. This points directly to a decline in average selling price or margin per unit, likely caused by heavy discounting, an unfavorable product mix shift, or rising costs.

### Insight 3: The Problem Escalated in 2024
The margin issues of 2023 appear to have evolved into a broader problem in 2024, with declines now seen across all key metrics: Quantity, Sales, and Gross Profit. This suggests the initial profitability issue was not contained and is now impacting overall sales volume.

### Updated Actionable Recommendations

1.  **Immediate Priority - Investigate 2023 Margin Erosion:** Launch a targeted investigation into the commercial activities of 2023. The key question is: **Why did we sell more for less?** This should involve a review of:
    - **Pricing & Discounting Strategy:** Were new, aggressive discount policies introduced?
    - **Product Sales Mix:** Did sales shift from high-margin "hero" products to low-margin "value" products?
    - **Cost of Goods Sold (COGS):** Did the cost of our key products increase without a corresponding price adjustment?

2.  **Conduct a Region-Specific "Then vs. Now" Analysis:** Since the underperforming countries shift each year (e.g., China in the total view, Canada/Germany in 2024), the problem is likely systemic, not isolated. I recommend using the dashboard to compare the product and customer mix in China in 2023 vs. Canada in 2024 to identify common patterns in these declining markets.

3.  **Refine Customer Segmentation Strategy:** The "High Revenue, Low Profit" customers identified in the scatter plot are now more critical than ever. In a declining margin environment, servicing these unprofitable accounts is especially damaging. A strategy must be developed to improve their profitability or, if necessary, de-prioritize them.
