# Data Dictionary — Maven Fuzzy E-commerce Analytics

## Overview

This document describes the tables and key columns used in the Maven Fuzzy Power BI dashboard. It provides definitions, data-grain information, and notes relevant to analysis and reporting.

## 1. Orders

**Purpose:** Stores order-level information.

**Grain:** One row per order.

| Column               | Meaning                                   | Key / Notes                      |
| -------------------- | ----------------------------------------- | -------------------------------- |
| `order_id`           | Unique identifier for an order            | Primary key                      |
| `order_date          | Date the order was created                | Order date                       |
| `website_session_id` | Website session associated with the order | Foreign key to sessions          |
| `user_id`            | Customer who placed the order             | Foreign key to users|
| `product_id`         | Primary product associated with the order | Product identifier               |
| `items_purchased`    | Number of items purchased in the order    | Order-level quantity             |
| `price_usd`          | Total order revenue n USD                 | Order-level amount               |
| `cost_usd`           | Total cost of goods sold for the order    | Order-level amount               |
|’profit’              |Total profit for the order.                |order-level amount|


## 2. Order Items

**Purpose:** Stores individual product-item records associated with orders.

**Grain:** One row per order item.

| Column            | Meaning                                                     | Key / Notes                         |
| ----------------- | ----------------------------------------------------------- | ----------------------------------- |
| `order_item_id`   | Unique identifier for an order item                         | Primary key                        
| `order_id`        | Order associated with the item                              | Foreign key to Orders               |
| `product_id`      | Product associated with the item                            | Foreign key to Products |
| `is_primary_item` | Indicates whether the item is the primary item in the order | 1 = primary item                    |
| `user_id`         | Customer who placed the order                               | Foreign key to users||



## 3. Order Item Refunds

**Purpose:** Stores refund records associated with order items.

**Grain:** One row per refund record.

| Column                 | Meaning                               | Key / Notes                              |
| ---------------------- | ------------------------------------- | ---------------------------------------- |
| `order_item_refund_id` | Unique refund-record identifier       | Primary key                              |
| `refund_amount_USD     | Amount refunded in USD                | Refund-level amount                      |
| `refund_date`          | Date the refund was recorded          | Refund date                              |
| `user_id`              | User associated with the refund       | Customer identifier                      |
| `product_id`           | Product associated with the item      | Foreign key to Products |





## 4. Website Sessions

**Purpose:** Records website visits and associated traffic information.

**Grain:** One row per website session.

| Column               | Meaning                                        | Key / Notes                       |
| -------------------- | ---------------------------------------------- | --------------------------------- |
| `website_session_id` | Unique website session identifier              | Primary key                       |
| `user_id`            | User associated with the session               | Customer identifier               |
| ‘utm_id              | Tracking module associated with the session    | Foreign key to UTM |
| is_repeat_session    | Indicates whether a session is a repeat visit  | Repeat session flag       |
| session_date         | Date of the session                            | Session date        |



## 5. Website Pageviews

**Purpose:** Records pages viewed during website sessions.

**Grain:** One row per pageview.

| Column                | Meaning                                | Key / Notes                     |
| --------------------- | -------------------------------------- | ------------------------------- |
| `website_pageview_id` | Unique pageview identifier             | Primary key                     |
| `website_session_id`  | Session in which the pageview occurred | Foreign key to Website Sessions |
| Pageview date         | Date of the pageview                   | Pageview date                   |
| `user_id`             | User associated with the pageview      | Customer identifier             |
| utm_id                | Tracking module associated with the pageview  | Foreign key to UTM.      |

6. Dim_product — Product Dimension
Purpose: Stores product identifiers and product names to support product-level sales and performance analysis.
Grain: One row per pageview.
Column
Meaning
Key/notes
product_id
Unique identifier for each product
Primary key
product_name
Name of the product
7. Dim_user — User Dimension
Purpose: Stores user identifiers and device information to support analysis of customer activity across devices.
Grain: One row per pageview.
Column
Meaning
Key/notes
user_id
Unique identifier for each user
Primary key
device_type
Type of device associated with the user
8. Dim_utm — Marketing Attribution Dimension
Purpose: Stores UTM tracking attributes used to identify marketing traffic sources, campaign names, and content variations.
Grain: One row per pageview.
Column
Meaning
Key/notes
utm_id
Unique identifier for each UTM record
Primary key
utm_content
Identifies the specific ad, creative, or link variation used in a campaign.
utm_campaign
Identifies the marketing campaign associated with website traffic.
utm_source
Identifies the platform or source that referred traffic.
