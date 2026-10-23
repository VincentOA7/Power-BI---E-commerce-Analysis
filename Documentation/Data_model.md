# Maven Fuzzy — Data Model Relationships

## Overview

This document describes the relationships between dimension tables and fact tables in the Maven Fuzzy dataset. These relationships support analysis of orders, product sales, refunds, website sessions, pageviews, and marketing traffic sources.

## Data Model Relationships

| From Table    | Key Column   | To Table                  | Key Column      | Relationship Purpose                 |
| ------------- | ------------ | ------------------------- | --------------- | ------------------------------------ |
| `dim_date`    | `Date`       | `fact_order`              | `order_date`    | Filters orders by order date         |
| `dim_date`    | `Date`       | `fact_website_pageview`   | `pageview_date` | Filters pageviews by date            |
| `dim_date`    | `Date`       | `fact_website_sessions`   | `session_date`  | Filters sessions by session date     |
| `dim_date`    | `Date`       | `fact_order_item_refunds` | `refund_date`   | Filters refunds by refund date       |
| `dim_product` | `product_id` | `fact_order`              | `product_id`    | Analyzes orders by product           |
| `dim_product` | `product_id` | `fact_order_item`         | `product_id`    | Analyzes item-level sales by product |
| `dim_product` | `product_id` | `fact_order_item_refunds` | `product_id`    | Analyzes refunds by product          |
| `dim_user`    | `user_id`    | `fact_order`              | `user_id`       | Analyzes orders by user              |
| `dim_user`    | `user_id`    | `fact_order_item`         | `user_id`       | Analyzes item purchases by user      |
| `dim_user`    | `user_id`    | `fact_order_item_refunds` | `user_id`       | Analyzes refunds by user             |
| `dim_user`    | `user_id`    | `fact_website_sessions`   | `user_id`       | Analyzes sessions by user            |
| `dim_user`    | `user_id`    | `fact_website_pageview`   | `user_id`       | Analyzes pageviews by user           |
| `dim_utm`     | `utm_id`     | `fact_website_sessions`   | `utm_id`        | Analyzes sessions by traffic source  |
| `dim_utm`     | `utm_id`     | `fact_website_pageview`   | `utm_id`        | Analyzes pageviews by traffic source |




Cardinality   - One-to-many (`1:*`)                                 
Dimension table  - One side                                            
Fact table        - Many side                                           
Cross-filter direction  -  Single                                              
Filter direction     -  Dimension to fact                                   
Relationship status   -  Active                                              

