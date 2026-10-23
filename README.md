# Maven Fuzzy | E-commerce Analysis

**An end-to-end e-commerce analytics project using Power BI, Power Query, DAX, and data modeling.**

## Project Overview

This project analyzes Maven Fuzzy's e-commerce performance using transactional and website analytics data. The Power BI dashboard brings together sales, orders, product performance, website traffic, and refunds to identify business trends and opportunities for improvement.

The primary objective is to transform raw data into actionable insights that support data-driven decisions around revenue growth, marketing performance, and refund management.

## Headline Finding: Refunds Spiked in Q3 2014

One of the most significant findings was a sharp increase in refunds during the third quarter of 2014.

* **Q2 2014 refunds:** $12,839.33
* **Q3 2014 refunds:** $29,582.00
* **Increase in refund amount:** Approximately 130%
* **Q2 2014 revenue:** $247,771.95
* **Q3 2014 revenue:** $260,237.12
* **Refunds as a percentage of revenue:** Increased from approximately 5.18% to 11.37%

Revenue increased by only about 5.03% between Q2 and Q3, while the refund amount more than doubled. This indicates a period when refunds increased disproportionately to revenue generated.

### Business Recommendation

Investigate the products, orders, and customer experiences associated with the Q3 2014 refund spike. Where data is available, examine refund reasons, product quality, shipping and fulfillment issues, and changes in marketing or product mix.

Monitor refund amounts, refund counts, and refunds as a percentage of revenue each quarter to identify unusual changes early and support timely corrective action.

## Tools and Technologies 

• **Microsoft Power BI** — Interactive dashboards and visual analytics

• **Power Query** — Data cleaning and transformation

• **DAX** — Measures, KPIs, and time-based calculations

• **Data Modeling** — Relationships between transactional and website analytics tables

## Dashboard Features 

The report is organized into the following analytical sections:

• KPI Overview: Displays essential business metrics, including Total Revenue, Total Orders, Average Order Value, Total Costs, Gross Profit, Total Refund Amount, and Session Conversion Rate.

• Revenue and Orders Trend: Visualizes quarterly revenue and order volume trends to identify growth patterns and sales performance over time.

• Refund Analysis: Tracks refund amounts and refunded order items to highlight refund trends and potential product or operational issues.

• Revenue vs. Refund Analysis: Compares annual revenue against refund amounts to evaluate sales performance and refund impact.

• Device Performance: Analyzes total orders by device type, including desktop and mobile, to understand customer purchasing behavior across devices.

• Product Sales Analysis: Identifies top-performing products based on total revenue, enabling comparisons of product contributions to overall sales.

• Traffic Source Analysis: Visualizes website sessions by traffic source, helping assess the effectiveness of search, social, and other acquisition channels.

• Marketing Campaign Analysis: Evaluates website sessions across marketing campaigns to understand traffic distribution and campaign reach.


• Products by Units Sold: Provides a tabular breakdown of products by order count to support product performance tracking and inventory planning.


## Additional Business Insights

### 1. Significant Revenue Growth

Monthly revenue increased substantially over the reporting period, reaching approximately $214,665 in December 2014.

**Recommendation:** Analyze order volume, average order value, product mix, and marketing activity to understand the drivers of revenue growth. Compare equivalent periods across years to account for potential seasonality.

### 2. Revenue Recovered in Q4 2014

Revenue increased from approximately $388,614 in Q3 2014 to $561,828 in Q4 2014, an increase of about 44.6%. Over the same periods, recorded refunds declined from $29,582 to $18,940.

**Recommendation:** Investigate changes in product mix, campaign performance, and fulfillment during this period to determine whether any improvements can be sustained. The observed relationship does not by itself establish causation.

### 3. Website Conversion and Device Performance

The dashboard reports a session conversion rate of approximately 6.83%, with desktop accounting for substantially more orders than mobile.

**Recommendation:** Compare conversion rates by device rather than order counts alone. Investigate the mobile shopping journey, including product-page usability, checkout friction, and payment options.

### 4. Marketing Performance

Nonbrand campaigns appear to account for a substantial share of website sessions.

**Recommendation:** Evaluate traffic sources and campaigns using conversion rate, revenue, and profitability—not traffic volume alone—to identify the channels that deliver the most valuable visitors.

## Business Recommendations Summary

Based on the analysis, the main recommended actions are:

1. Investigate the Q3 2014 refund spike to identify its underlying drivers.
2. Monitor refunds relative to revenue and order volume.
3. Analyze the factors behind revenue growth and the Q4 2014 recovery.
4. Evaluate marketing channels using conversion and commercial performance.
5. Compare device-level conversion rates to identify website improvement opportunities.
6. Validate product-level sales before making inventory and promotional decisions.

## Dashboard Preview
![image alt](https://github.com/VincentOA7/Power-BI---E-commerce-Analysis/blob/427a154086072512bdae41311dcaf4e5539d4f65/Screenshot/Maven%20Fuzzy%20Dashboard.png)

## Conclusion

This project demonstrates how Power BI can be used to combine e-commerce transactions and website analytics into a single business reporting solution.

The Q3 2014 refund spike provides a focused example of how data analysis can reveal a potential business issue, quantify its significance, and guide further investigation. By combining performance monitoring with data validation and actionable recommendations, the dashboard supports more informed business decision-making.

## Disclaimer

This project is intended for analytical and portfolio purposes. Findings and recommendations are based on the available data and should be interpreted in the context of the dataset's limitations.
