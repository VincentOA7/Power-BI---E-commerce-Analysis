# DAX Measures — Maven Fuzzy

## Overview

This document describes the main DAX measures used in the Maven Fuzzy e-commerce performance dashboard. The measures track revenue, order volume, profitability, refunds, website traffic, and conversion performance.

### Total Revenue

```dax
Total Revenue =
SUM(fact_orders[price_usd])
```

**Definition:** Total revenue recorded across orders.

**Business purpose:** Measures sales performance over the selected period.

### Total Orders

```dax
Total Orders =
DISTINCTCOUNT(fact_orders[order_id])
```

**Definition:** Number of unique orders.

**Business purpose:** Tracks order volume without counting an order more than once.

### Average Order Value (AOV)

```dax
Average Order Value =
([Total Revenue]/[Total Orders]
```

**Definition:** Average revenue per order.

**Business purpose:** Helps evaluate purchasing value and changes in customer spending.

### Total Cost of Goods Sold

```dax
Total Cost
SUM(fact_orders[cost_usd])
```

**Definition:** Total cost of goods sold recorded at order level.

### Gross Profit

```dax
Gross Profit =
[Total Revenue] - [Total Cost]
```

**Definition:** Revenue minus cost of goods sold.

**Business purpose:** Measures profit before other operating expenses.

### Gross Profit Margin

```dax
Gross Profit Margin =
[Gross Profit]/[Total Revenue]
```

**Definition:** Gross profit as a percentage of revenue.

**Business purpose:** Tracks profitability as sales change.

### Total Refund Amount

```dax
Total Refund Amount =
SUM(fact-order_item_refunds[refund_amount])
```

**Definition:** Total recorded refund amount.

**Business purpose:** Monitors the financial impact of refunds.

### Refund Count

```dax
Refund Count
DISTINCTCOUNT(fact_order_item_refunds[order_item_refund_id])
```

**Definition:** Number of unique refund records, not necessarily unique orders refunded.

**Business purpose:** Tracks refund activity.


### Total Sessions

```dax
Total Sessions =
DISTINCTCOUNT(fact_website_sessions[website_session_id])
```

**Definition:** Number of unique website sessions.

### Sessions with Orders

```dax
Sessions with Orders =
CALCULATE(
    DISTINCTCOUNT(orders[website_session_id]),
    NOT ISBLANK(orders[website_session_id])
)
```

**Definition:** Unique sessions linked to at least one order.

### Session Conversion Rate

```dax
Session Conversion Rate =
DIVIDE([Sessions with Orders], [Total Sessions], 0)
```

**Definition:** Sessions linked to an order divided by total sessions.

**Business purpose:** Measures how effectively website traffic converts into orders.



### Total Unit ordered 

```dax
Total Units Ordered=
COUNT(fact_order_item[product_id])
```

**Definition:** Number of order-item rows, assuming each row represents one unit.

**Business purpose:** Compares product sales volume.
